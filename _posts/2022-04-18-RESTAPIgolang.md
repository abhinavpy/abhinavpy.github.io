---
title: 'RESTful API Golang 18 April 2022'
date: 2022-04-18
permalink: /posts/2022/04/resp-api-golang/
tags:
  - RESTful API
  - Golang
---


```
package main

import(
	"encoding/json"
	"fmt"
	"io/ioutil"
	"log"
	"net/http"
	"github.com/gorilla/mux"
)

type event struct {
	ID string `json: "ID"`
	Title string `json: "Title"`
	Description string `json: "Description"`
}

type allEvents []event

var events = allEvents{
	event{ID : "1", Title: "Title1", Description: "Desc1"},
	event{ID : "2", Title: "Title2", Description: "Desc2"},
}

func homePage(w http.ResponseWriter, r *http.Request) {
	fmt.Fprintf(w, "Welcome to the homepage!!!")
	fmt.Println("Endpoint Hit: homePage")
}

func returnAllEvents(w http.ResponseWriter, r *http.Request) {
	fmt.Fprintf(w, "The events are as follows: ")
	json.NewEncoder(w).Encode(events)
	fmt.Println("Endpoint Hit: returnAllEvents")
}

func getSingleEvent(w http.ResponseWriter, r *http.Request) {
	eventID := mux.Vars(r)["id"]

	for _, singleEvent := range events {
		if singleEvent.ID == eventID {
			fmt.Fprintf(w, "Successfully found required event: ")
			json.NewEncoder(w).Encode(singleEvent)
		}
	}
	fmt.Println("Endpoint Hit: getSingleEvent")
}

func createSingleEvent(w http.ResponseWriter, r *http.Request) {
	var newEvent event
	reqBody, _ := ioutil.ReadAll(r.Body)

	json.Unmarshal(reqBody, &newEvent)
	events = append(events, newEvent)
	
	fmt.Fprintf(w, "The newly entered data is as follows: ")
	json.NewEncoder(w).Encode(newEvent)
}

func deleteSingleEvent(w http.ResponseWriter, r *http.Request) {
	eventID := mux.Vars(r)["id"]
	for i, singleEvent := range events {
		if singleEvent.ID == eventID {
			events = append(events[:i], events[i+1:]...)
			fmt.Fprintf(w, "The event with ID %v has been deleted successfully", eventID)
		}
	}
}

func updateSingleEvent(w http.ResponseWriter, r *http.Request) {
	eventID := mux.Vars(r)["id"]
	var updatedEvent event

	reqBody, _ := ioutil.ReadAll(r.Body)
	
	json.Unmarshal(reqBody, &updatedEvent)

	for i, singleEvent := range events {
		if singleEvent.ID == eventID {
			singleEvent.Title = updatedEvent.Title
			singleEvent.Description = updatedEvent.Description
			events = append(events[:i], singleEvent)
			fmt.Fprintf(w, "Successfully updated event %v", eventID)
		}
	}
	fmt.Println("Endpoint Hit: updateSingleEvent")
}

func main() {
	router := mux.NewRouter().StrictSlash(true)
	router.HandleFunc("/", homePage).Methods("GET")
	router.HandleFunc("/events", returnAllEvents).Methods("GET")
	router.HandleFunc("/event/{id}", getSingleEvent).Methods("GET")
	router.HandleFunc("/event", createSingleEvent).Methods("POST")
	router.HandleFunc("/event/{id}", deleteSingleEvent).Methods("DELETE")
	router.HandleFunc("/event/{id}", updateSingleEvent).Methods("PATCH")
	log.Fatal(http.ListenAndServe(":8080", router))
}
```

---
title: 'Daily Blog Post 1 May 2022'
date: 2022-05-01
permalink: /posts/2022/05/daily-post/
tags:
  - CSS
  - ReactJS
  - API Kong Gateways
  - OAuth2.0
  - COA
---

## ReactJS - Started Day 1 of 100DaysOfCode of ReactJS
Studied about react components.
hen it comes to React it is all about components. 
You can think of components as independent chunks of user interfaces.
Components can be as small as one HTML element or you can be a rebel, and jam your entire facebook clone in one component. 
At the end of the day, a lot of it depends on your needs and wants. In reality though you will probably
avoid the one component route because it defeats the purpose of using React. 

You see the benefit of component is you can build a bunch of independent isolated, and most importantly reusable user interfaces that you can run and piece together just like lego blocks. 

And as a result, build even super complex apps without going insane. 

While your app can have as many components as you'd like, it will always have atleast one called 
root component. 

We already glossed over it a bit, but just to reiterate the major benefits of using components and essentially, react, develop your next app or phone, you can build independent pieces of user interfaces, meaning 
changing logic, or layout in one component will not break your OLAP once component is ready to go, you can reuse it all
throughout your app.

But component code is still stored in one place. 

So if you ever need to make some changes, you don't have to run around like a headless chicken, simply locate the component, apply the changes, and all the instances will be automatically updated. 

And of course, let's also not forget about speed. 

You see behind the scenes, React is using something called virtual DOM, where only the component that needs to be updated, is affected. 

And what's really cool, it's done without rerendering the whole app, which in turn, of course, increases the speed of your final product. 

And as a result the user experience as well. 

Before we go, let's look at a typical example of React that everyone uses to show React Components in Action. 
And that is no other than our beloved Twitter. 

So as we are looking at the screen, on the left hand side of the homescreen we see various React Components. 
So you will see a bunch of words, however you probably notice that each link has pretty much the same structure, where there is some kind of icon and associated text.

So essentially what we could do is set this up as one component. And what that means is we will just set up a structure,
and everywhere where we would want to use it, we will just need to pass in the data. 

And by data of course I mean, the specific icon that is going to be rendered. And then of course the text.

And as a result, what that also means that I can reuse that component, all throughout my application, however I would like.

But if I would want to make some changes, for example if I would want to add something here, I can change it in one place, and then all the instances will be automatically updated. so that would be a links example. 

And you can probably already guess, the same, for example, would work with a post. Because when we are
looking at the post, what do we have, we have some kind of picture, we have the name, of course, we have 
the text, we have all the retweet options, as well as likes and comments, but the only thing that is 
changing is the data. So the person who is posting and how many likes, and that sort of thing. The point that 
I am trying to make is that as you are looking at the application, you can see a bunch of places where we can 
set up a react component, and then use all the awesome benefits the components provide. 

Before we go futher, let's cover the main goals of this course, and honestly there is only one:
By the end of the course I should be comfortable with React. 
Now what that means is you can do two things. First, you are aware of external resources. And more 
importantly, you're comfortable with using them. When you'd want to learn something new. Essentially
you know where to find useful info. And second, you are comfortable applying theory to practice by 
building your own project using React. 

While the Core API of react is essentially quite small, since it is by far the most popular framework out there,
the ecosystem surrounding react is as vast as you can imagine. What that means is that essentially, there 
will always be something new to learn about React.

That's why I would suggest adopting a student mindset instead, where you are always open to expanding your
React knowledge. In my experience, the best way to learn and get comfortable with language and framework is 
by building a bunch of projects. So that is exactly what we will do during this course, we'll start small, 
our first project will be somewhat silly, but slowly and surely, we will expand on our knowledge. And by the end
of the course, you will be comfortable building your own complex React apps.

Structure
- Dev Environment
- Tutorial
- Projects
- Redux

Course Requirements
- HTML
- CSS
- JavaScript (ES6)
- Coding Addict - JavaScript Nuggets

The more javascript you know the easier it is going to become. Because at the end of the day 
React is just javascript. 
So if you are familiar with things like spread operator, ro functions, destructuring etc. 
you will be in good shape. 

Dev Environment
- Node
- Browser = Chrome
- VSCode
- React Developer Tools

## CSS - 100DaysOfCode Day - 1
- Box Model - Extrinsic and Intrinsic Sizing.
- Content Sizing
- The area of the box model
- A useful analogy
- Debugging the box model
- Controlling the box model
- Resources

Content Sizing - Extrinsic sizing, Intrinsic sizing.

The areas of the box model - margin box, border box, padding box, content box.

The border box surrounds the padding box and its space is occupied by the border value. The border box is the bounds of your box and the border edge is the limit of what you can visually see. The border property is used to visually frame an element.

The final area, the margin box, is the space around your box, defined by the margin rule on your box. Properties such as outline and box-shadow occupy this space too because they are painted on top, so they don't affect the size of our box. You could have an outline-width of 200px on our box and everything inside and including the border box would be exactly the same size.

Every browser applies a user agent stylesheet to HTML documents. The CSS used varies between each browser, but they provide sensible defaults to make content easier to read. They define how elements should look and behave if there's no CSS defined. It is in the user agent styles where a box's default display is set, too. For example, if we are in a normal flow, a <div> element's default display value is block, a <li> has a default display value of list-item, and a <span> has a default display value of inline.

An inline element has block margin, but other elements won't respect it. Use inline-block, and those elements will respect the block margin, while the element maintains most of the same behaviors it had as an inline element. A block item will, by default, fill the available inline space, whereas a inline and inline-block elements will only be as large as their content.

Alongside an understanding of how user agent styles affect each box, you also need to understand box-sizing, which tells our box how to calculate its box size. By default, all elements have the following user agent style: box-sizing: content-box;.

Having content-box as the value of box-sizing means that when you set dimensions, such as a width and height, they will be applied to the content box. If you then set padding and border, these values will be added to the content box's size.

## OAuth 2.0 
YouTube Link: https://youtu.be/Aj143QiiQPY
  
## API Kong 
Wrote slides : https://docs.google.com/presentation/d/1WVtuhszW1a7pJk109EFxMZWOGhMQyUvIsMSl0yP9vUU/edit?usp=sharing
  
## Computer Organization and Architecture 
Read Chapter - 1 of William Stallings COA Book.
  
## Dynamic Programming - 100DaysOfCode - Day 1
https://leetcode.com/tag/dynamic-programming/discuss/662866/DP-for-Beginners-Problems-or-Patterns-or-Sample-Solutions

  
The above problem list will be followed:

Problem for Day - 1 : Longest Increasing Subsequence Variant : 
  Longest Increasing Subsequence: https://leetcode.com/problems/longest-increasing-subsequence/
  
Sample Solution for LIS:
  ```
  int lengthOfLIS(vector<int>& nums) {
    int n = nums.size();
  
    vector<int>LIS(n+1, 1);
    for(int i = 0; i < n; i++) {
      for(int j = 0; j < i; j++) {
        if(nums[i] > nums[j]) {
          LIS[i] = max(LIS[i], 1 + LIS[j]);
        }
      }
    }
  
    int ans = 0;
    for(i = 0; i < n; i++) {
      ans = max(ans, LIS[i]);
    }
    return ans;
  }
  ```
  




---
layout: post
title:      "Sinatra CRUD application "
date:       2018-05-14 00:20:44 +0000
permalink:  sinatra_crud_application
---


Sinatra is a simple yet powerful framework for building web applications with Ruby. This project utilized Ruby, Activerecord,  Sinatra, HTML and CSS. 

My application is called Vin-Tracker, and it is a web app for friends to create and share their favorite types of wine with each other. A user creates an account, and can add types of wine to a list, and can then click on any wine on the list and see which one of their friends added that wine. Great for planning parties or for that serious group of wine drinkers! 

Ruby, Activerecord and  Sinatra were used to build out the routes, create the models and establish the relationships between them. There is so much added functionality with Activerecord for example, I utilized the has_many/belongs_to relationship, though just a simple keyword adds great amounts of flexibility and functionality to the Ruby models. 

I also utilized an MVC pattern as well as RESTful. MVC is simply a way of approaching the layout of parts to an application. RESTful conventions are using HTTP verbs(GET, POST, PATCH, DELETE) as they were intended (to create, read, update and delete) A few thoughts on being RESTful; First,  GET requests should never be used for updating information. For example, a GET request for adding an item to a list

http://myserver.com/addToList?List=314159&item=1729
would not be appropriate. GET requests should be *idempotent*. That is, issuing a request multiple times should be no different from issuing it once - that is what makes the requests cacheable. An "add to list" request is not idempotent—issuing it twice adds two copies of the item to the list. A POST request is clearly appropriate in this context.

I used HTML and CSS on the front end, I mostly just borrowed from existing libraries (including my favorite site, Google Fonts!) I enjoyed every bit of this project, and felt comfortable working on the routes and controller actions, as well as combining fonts and colors and building forms in the views folder. 

I hope you take the time to check it out, it is a fun little app! 


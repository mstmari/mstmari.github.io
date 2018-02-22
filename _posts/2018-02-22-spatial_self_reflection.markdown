---
layout: post
title:      "Spatial Self Reflection"
date:       2018-02-22 17:37:41 -0500
permalink:  spatial_self_reflection
---


Spatial metaphors are important to understanding the role of the default object, self as well as the scoping rules for local, global and class variables. 

As ruby operates on code, things are constantly shifting, and different objects are being addressed which impacts which code gets run and how its output is interpreted. However, there are a few objects that stay the same; integers mean what they mean regardless of where they are in your program,  the keywords def and class can’t be used as variable names, so when you see these you can easily understand what they mean and symbols remain the same regardless of their use in the program. Below is an example taken from ruby-doc.org

	 if Fred is a constant in one context, a method in another, and a class in a third, the Symbol :Fred will be the same object in all three contexts.

The meaning of most elements in Ruby depends on its context and is place and time in the program. That is why it is important to stay aware of your surroundings and where you are in the program when writing code. If you understand what can change from one context to another and also what triggers a change in context (for example, entering a method definition block) you can always get your bearings in a Ruby program (David A. Black – The Well Grounded Rubyist p.116)
 
Class definition blocks, module definition blocks, and method definition blocks are basically the only three contexts in which self exists. The most important thing is to understand at a given time in which object you are currently operating. (class and module definitions are very similar)

Self is the current object and the default receiver of method calls when no other receiver is given. Remember, in a method, the object on which the method was called is self. In a class, self is the class object being defined. 

Now, let us further explore the ideas spatiality in our programs. It is vitally important to always know where you are (read; what scope you are in) so you can easily tell what your variables are referring to and to not confuse them with variables from other scopes that possess similar names or with similarly named methods.

Just a quick side note and something that has stumped me several times recently, one easy way to help not get confused here is to use as descriptive naming for variables and methods as possible, even if it makes for more verbose code, the ease of being able to quickly recognize what is happening and where is likely worth the extra visual clutter. 

Global scope is scope that covers the entire program. Global variables are available everywhere, regardless of what self is global variables are still available. Local scope is a basic layer of the fabric of every ruby program, at any given moment your program is in a particular local scope, the main thing that changes from one local scope to another is the availability of local variables.  

Each time you type Class, module of def you create a new space inside your program by defining a new local scope. 

When someone mentions scope, think of 2 words: variables and visibility. Scope is all about where something is visible. It’s about what (variables, constants, methods) is available to you at a given moment. If you understand scope well enough, you should be able to point at any line of your Ruby program and tell which variables are available in that context, and more importantly, which ones are not.


![](https://ibb.co/gf9ZoH)

I am working on illustrating some of the diagrams in The Well Grounded Rubyist, this is a mashup of the scope and self diagram from pages 118 and 129. 


https://ruby-doc.org/core-2.2.0/Symbol.html

https://www.sitepoint.com/understanding-scope-in-ruby/

The Well Grounded Rubyist, by David A. Black




---
layout: post
title:      "The 10 day daily-tree"
date:       2018-03-23 05:04:15 +0000
permalink:  the_10_day_daily-tree
---

Introduction to the project

My data gem CLI project is called daily-tree and it is a botanists dream!  It allows you to search a database and can provide information on up to 50 plant species. 
![](https://imgur.com/U0r7DiZ)
*Brief walkthrough*

It scrapes a database of different plant varieties, it returns formatted menu containing 50 trees with their scientific name and their common name and an index number.  It then prompts the user to enter the index of the plant they would like to learn more information on and returns a list of all those attributes, and repeats this step until the user types ‘exit’. 
![](https://imgur.com/ANoJftm)
![](https://imgur.com/XSOpCLK)
 *About the plant database*

Many technical universities that have biology or horticulture departments will have a database of information on regional plants. It helps the schools keep track of different species while making it simple for people to learn about different species and their characteristics and growth behavior, as well as other things like their size, shape and hardiness zone. My program uses North Carolina State University database ([here](https://plants.ces.ncsu.edu/plants/category/trees/)). 

*Inspiration for the project *

I have always had an interest in botany and have used these databases before. I learned a ton about classification and how plants are divided up by their characteristics. As I was going through the OO section of the program I began to notice corollary patterns between how plants are categorized and relate to one another the relationships between objects and classes. I used this project to test that out and I was not disappointed! 

*Issues I encountered*

One of the initial issues I faced was setting up the load path and knowing where to use require or require_relative and what gems I needed to install, once I got something to return in the command line I progressed only to realize that one file was not talking to the other. In the end, it just took basically mimicking what I had seen in other labs and a ton of googling and reading about load paths. I think this was the thing I knew the least about, and ended up learning the most about. 

Another issue I had was getting my different methods to talk to each other, this gave me the most trouble including a solid two days of work only to realize the importance of where you call methods. 

*What did you learn?* 

Overall, this was a great project to tie all that we have learned together. It forced me to become very familiar with the built in ruby methods and especially the way the idderent objects and classes communicate with each other. My favorite part, was using Nokogiri for parsing the html raw data – it was like a sodoku puzzle getting it to return the right thing and actually work! I’ve greatly enjoyed working in Ruby, but at this point I’m looking forward moving on. 




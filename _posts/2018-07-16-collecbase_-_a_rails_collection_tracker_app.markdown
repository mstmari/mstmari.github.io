---
layout: post
title:      "Collecbase - A Rails Collection Tracker App"
date:       2018-07-16 13:26:07 +0000
permalink:  collecbase_-_a_rails_collection_tracker_app
---


	My Rails portfolio project is called Collecbase, it is a collection tracker for people who collect books. It was originally designed with the idea of using comic books, but I started using classic books and it stuck. However, it could be easily adapted to track any type of collection (Also, I don’t know that much about comic books)
The project has a Book, User and UserBook models, with the Book and User joined on the UserBook. The book is a canonical object, just something that is accepted as original and cannot be changed, the UserBook represents the user’s copy of the book. 

Technical challenges & solutions:

	The main problem came from trying to associate the models without fully understanding how their associations function, what rails methods came with the associations and what was needed to make them function how I wanted. I knew how a join table works and theoretically what that means, but I was not using it the way it was meant to be used. Essentially, I was building an object off of another object, in order to automatically associate them then mass assigning all the attributes in the parent object controller. Of course, in retrospect its clear to see this violates the rule of separation of concerns, and was the source of most of my problems.  

	This caused major issues in my edit/update feature because I wanted a user to be able to edit a book if they added it, but not if they didn't own it but also be able to edit their own copy of that book (or multiple copies) in their collection.  

	 I ended up creating an admin account and allowing users to choose from a pre-set index of books for their collection. I think this is how it would work in the world of collectors anyways, there are only the SpiderMan comic books Marvel produces and no others, therefore the user doesn't need to add his own books, only add books to his collection. Therefore, I created an admin account and then built out the user_book views/controller and everything makes sense now! 

Another issue I encountered was with the naming of my routes. My models are User, Book and UserBook, when rails creates routing methods it appends the names of the models together, in my case that made matters very confusing, it combined them into my other class name, or even worse gave me the edit_user_user_book instead, what I did was aliased the name of my user_books as books in order to keep the routes restful:

```
resources :users do
    resources :user_books, :path => "books", :as => :books
  end
```

this was did not make things necessarily easier for me, but would make things easier for the user to navigate the site through the URL which is ultimately the end goal of restful conventions. 

	Ultimately this was a fun project to work on, I encountered substantial challenges that pushed me to grow as a developer. In the future, I think having a better picture of how users interact with the site from the offset would help me to know exactly what needs to go where. I learned far more about rails through troubleshooting and reading extensive amounts of documentation than I would have if everything had worked correctly the first time. However, In the future I will make sure to fully understand the relationships between my objects and the inherent methods that come through associations. 
Also, I got to test the resilience and grit it takes get a program working and am happy that I persevered and got my original idea off the ground!
 



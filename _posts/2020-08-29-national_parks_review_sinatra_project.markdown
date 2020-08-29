---
layout: post
title:      "National Parks Review: Sinatra Project"
date:       2020-08-29 23:32:46 +0000
permalink:  national_parks_review_sinatra_project
---

Before Sinatra Project Week I took a family trip to Maine to visit Bar Harbor and Acadia National Park. This inspired me to create an app allowing a user to view information on as well as leave and read reviews for every U.S. National Park.

My project has 3 models-- User, Park, and Review. The relationships between the models are as follows: 

* A User has many reviews, and has many parks through reviews. 
* A Review, the join table, belongs to both a park and a user. 
* A Park has many reviews and has many users through reviews.

The parks are pre-loaded through the db:seeds file and the route for each park is created dynamically. The parks can be viewed in alphabetical order or organized by the state that they're in. Users, once logged in, can visit the route for a particular park, and leave a review. Reviews have full CRUD functionality for the user that created them. Reviews have a rating attribute on a 0-5 scale, and also have an upvote/downvote attribute. Each upvote has a +2 value and each downvote a -1 value. Reviews are sorted by highest value first when the park page is loaded.

Users can also visit each others' profiles. User profile routes are created dynamically using a user's user_id attribute which is guaranteed to be unique. Users are able to add and edit a personal bio on their profile. User profiles also have something called "Charisma Points" which is the aggregate upvote/downvote value.

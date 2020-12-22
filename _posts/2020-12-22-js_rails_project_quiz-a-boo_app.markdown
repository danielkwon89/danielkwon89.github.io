---
layout: post
title:      "JS/Rails Project: Quiz-A-Boo App"
date:       2020-12-22 18:59:59 +0000
permalink:  js_rails_project_quiz-a-boo_app
---


For my JS/Rails project, I created a quiz app tailored to anime and manga fans.

The app sends fetch requests to the Open Trivia Database API to get quiz questions and answers in JSON format. Using this JSON, my frontend renders the quizzes and leaderboard. For my project MVP I've limited the quiz category to only anime and manga. My stretch goal is to include 9-12 categories for the users to choose from.

My app has users and validations but no authentication. You simply put in a username (with some restrictions) and then choose the difficulty level of the quiz. If you score high enough, the username is placed on a leaderboard.

My biggest challenge for this project was getting Rails to communicate with my frontend and structuring the JSON the way I needed it. Once these steps were completed, it became easier to complete the rest of the project.

Refactoring my project as OO JS is also not the most intuitive but I was able to create a Question class to construct the quiz questions. After submitting my MVP I'd like to work on some more refactoring so I can extend the app to include more quiz categories.

---
layout: post
title:      "My Sinatra Project and What I've Learned"
date:       2017-12-16 19:20:00 +0000
permalink:  my_sinatra_project_and_what_ive_learned
---


I have finally finished my Sinatra Project and what an adventure!  My Sinatra application is [Knitting Patterns](https://github.com/Christy743/knitting-patterns).  I tried not to compare myself with others in that I watched in Learn and Slack that others were breezing by with their projects and lessons from my perspective. I kept telling myself that I can go at my pace and it's okay.  And you know what?  It is okay because I do want to understand the concepts and how it works 'under the hood'.  I learned a lot with this project such as active records and how to migrate data to the database and how to delete a whole table by running rake db:create_migration NAME=drop_materials.rb. I learned a lot about routes and how they work with get, post, patch, etc.

The steps I've learned and took are below that have helped me complete my app in Sinatra:

1. Write out what you will need for your MVC and what to include such as users, project, tables to migrate, and the has_many or belongs_to relationships.  Thinking about the associations between your classes.

2.  Write out on paper your view pages.  You want to visualize how your application will look like on the internet. I drew out five pages and included my welcome page, sign up or register page, log in or sign in page, new pattern or project page and the individual project or pattern page.  After starting up everything and putting in my code, I added an index page where the user can see a list of all patterns and a list of their patterns.

3.  I started writing out my models and making my tables to reflect the class associations in my schema and models of what belongs to who and who has many.  I have learned how to fix these associations when my app was not working.

4.  I worked on my routes and view pages while running the shotgun gem in my terminal.  It was a challenge at first because I mistakenly used the tux gem to find my parameters.  Tux is not the gem to do that, but it is helpful in trying to figure out if you can make a new instance of one of your classes.  Say you want to make a new project.  Tux will be helpful in that task and it does manipulate your data in the database.  If you want to delete an instance of a class, tux is a useful tool.  'Binding.pry' is very useful and when I remembered that it is my friend, I used the heck out of it!  Use binding.pry because it will help you complete your project a bit quicker.

5.  When I got everything running, I made sure every link and every page worked.  Then I cleaned up my code and went through every page and link to make sure it all worked.  
 
I know it's a pretty simple application, but I worked hard on it and I am proud that I got this far in the curriculum.  I look forward to my assessment and learning more from my assessment and continuing on learning.  

“Life is a journey, not a destination.”  - Ralph Waldo Emerson






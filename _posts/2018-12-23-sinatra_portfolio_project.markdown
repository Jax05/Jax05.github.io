---
layout: post
title:      "Sinatra Portfolio Project"
date:       2018-12-23 20:29:03 -0500
permalink:  sinatra_portfolio_project
---


# Overview

The second project in the Full Stack Web Development course at [Flatiron School](http://www.flatironschool.com) is based on [Sinatra](http://rubygems.org/gems/sinatra/versions/1.4.7). The task is to create a basic application centered around a topic of our own interest. It should include MVC architecture and allow users to create, read, update, and delete resources. The requirements are simple:

* Use ActiveRecord with Sinatra
* Use multiple models
* Use at lease one has_many relationship on a User model and one belongs_to relationship on another model
* Must have user accounts - users must be able to sign up, sign in, and sign out
* Validate uniqueness of user login attribute (username or email)
* Once logged in, a user must have the ability to create, read, update, and delete the resource that belongs_to user
* Ensure that users can edit and delete only their own resources - not resources created by other users
* Validate user input so bad data cannot be persisted to the database
* BONUS: Display validation failures to user with error messages

# Meet CRUD Pokedex
The concept behind my application is to allow users to create and add Pokemon to a global Pokedex. It's simply dubbed CRUD Pokedex. My inspiration was due partly to the Detective Pikachu trailer and mostly to the long hours I spent playing Pokemon Crystal Version on my bright green Game Boy Color.

CRUD Pokedex uses a SQLite3 database paired with ActiveRecord for object relational mapping. Since users must create an account to interact with the app, authentication is necessary. We achieve this with Sinatra sessions and [bcrypt](http://rubygems.org/gems/bcrypt), a password hashing gem. Sinatra also handles routing for our web application.

The application employs the use of validations for all form data submitted. This means that it will not allow any blank inputs, and all user accounts must be created with a unique username and password combination. If these validations fail, the form will not submit and an error message will appear at the top of the page detailing exactly what went wrong.

# Future Improvements
In order to pass the Sinatra project lab, all functionality listed in the requirements must be present - but this still leaves a lot of room for improvement. Specifically when it comes to application design. CRUD Pokedex is styled using a very basic CSS framework called [Spectre.css](http://picturepan2.github.io/spectre/), but it needs to be polished to achieve a more cohesive, professional look.

Think of it as an alpha prototype. It includes basic functionality but needs a number of features in order to become a seriously engaging application for users. The addition of images, more user interaction, and detailed Pokemon information would help make it appealing for long-time use.

These improvements are in the works! Check out the Github repo for [CRUD Pokedex](http://github.com/jax05/crud-pokedex), give it a star, and feel free to submit your own pull requests. Your feedback and contributions are appreciated.

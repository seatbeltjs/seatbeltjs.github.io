---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: page
permalink: /
---
# About

Seatbelt is a web framework designed to help simplify the creation and management of routes while adding typescript support.  This is a framework for making API's easier to create. If you are trying to create a front end app, there are better solutions available.  If you need a back end to connect to your angular/react/backbone app, then this may be a good solution for you.

#### Warning

Seatbelt is currently in alpha.  This text will be erased once a full version is released.  Expect lots of changes before its finished.

#### Documentation

In depth documentation will be located at [https://seatbelt.readthedocs.io](https://seatbelt.readthedocs.io)

## Why another node MVC framework?

 After having used the sails framework for a couple years I have realized many of the frameworks benefits and flaws.  Seatbelt uses some of the good concepts of the sails framework and fixes the bad parts.

### What problems does this MVC solve?

**Problem**: In sailsJS, seatbelt has an automatic file import feature.  An excellent feature that cuts down a lot on import/export statements.  However, it is easy to create giant mega files due to the include all nature of the framework.  It pulls in every file in each folder and subfolders into the application and uses them regardless if you want it to.
<br>**Solution**: Keep the automatic importing(it helps cut down on lots of import/export statements) and only include files exported with a seatbelt wrapper.

**Problem**: In sailsJS has specific file directories you are forced to use for different file types
<br>**Solution**: Files can be placed anywhere.  As long as you export your class after you create or initialize it, it will be imported into the project, regardless of where it is located.  I don't recommend it but you could put every single file in a single folder.

**Problem**: In sailsJS only express server is used
<br>**Solution**: Any server can be used: hapi, express, koa, restify

**Problem**: In sailsJS Only waterline can be used as an orm
<br>**Solution**: Any orm can be used: waterline, bookshelf, etc

#### Implemented Features

- [X] Allows the use typescript in node
- [X] Allows the use of any server: Koa, Express, Hapi, or Restify
- [X] Allows the use of any ORM: Waterline, Bookshelf, etc
- [X] Any class decorated with a seatbelt class will automatically be included in the project
- [X] CLI Tool to create new projects
- [X] Class Decorator to allows creation's of policies to control access to each route
- [X] Method Decorator that wraps controller and allows access of created policies
- [X] Class Decorator to create new Services
- [X] Property Decorator to import created services into any class
- [X] Method Decorator that wraps controller that validates(via hapi js) all params sent to the route

#### Planned Features
- [ ] Dynamic Module imports without the need to import them into the project
- [ ] Unit testing without booting server
- [ ] Allow dynamic importing of types, live server reloads
- [ ] CLI tool can create routes and models

# README

## What I did

### Setup

```
1) First created the rails files by using rails new **file name**

2) Folders that we will frequently use are: apps (assets, controllers, models, views), config (routes), db(migrate and schema)

3) Then created a home page and you can generate all the relevant files by using rails generate controller home index (this creates a controller,route, view, web page, test file and ruby file)
4) Changed the routes in the config file

5) run rails s to view the server

6) The page you created when you ran generate is within apps --> views -->home --> index.html

7) Can change the root of our index within the routes file e.g. root 'home#index' (foldername#filename)
8) Rails routes checks all the routes within the project

9) Within apps --> views --> layouts --> applications html displays all of our web pages and they are all linked through here. This happens through the <%yield%>

10) We can add styles through this page and it will happen on all pages
```

### Bootstrap

```
11) Then added bootstrap into my file by going on bootstrap.com, found the latest version to copy the template on, put this on the apps page. After this you match the code you have previously to put within this boot strap. yield where H1 is, Title replaces new tile and the copy the rest of the old code and paste below the head of the boot strap. Can then delete the old bootstrap.

12) To create a partial - create a file within the home folder and call this _header.html.erb

13) On the app html page within the body put <%= render "home/header %>, the page is able to pick up the header without the _ because render means it's looking for a partial file.

14) The header file is now linked and means you can type anything in the header file and it will be displayed through the app html.

15) To add a navbar go onto Bootstrap.com --> components --> navbar, copy the navbar that looks good, past the code within the header file. This navbar will now be shown on your web page and all other web pages linked. (can edit the navbar slightly within the header page e.g. change from light to dark, change the name too)

16) Can delete dropdowns by going within the header file and delete the indvidual li with code inside it too.
```

### Links

```
17) To create a link so that the buttons work on the navbar:
Within the header file - type in <%= link_to"WhateverYouWant"%>, foldername_filename_path (or root_path if it's the home page), class="whateverYouAreReplacingInTheLi". e.g. <%= link_to"Friends, root_path, class=nav-link>


18) rails routes shows you all your routes and shows the prefixes which can be used in the previous step
```

### Creating a scaffold - CRUD

```
19) To create the crud principals we can use something called scaffold. This will allow us to create, read, update and destroy. This can put information within a table.

20) run rails g scaffold friends first_name:string last_name:string email:string etc

21) This creates a lot of files, within the controller, db, htmls etc and are all linked to our other pages.  In the db files we can see the tables created.

22) rails db:migrate will actually make all of this go live and will create the database properly. In the example on step 20 we could visit localhost:3000/friends and we'd see the crud principals that we've created.
```

### Back to bootstrap

```
23) I then worked on some bootstrap to make the page look nicer. First go to app --> views --> friends (where all your table info was made in the previous steps). And also go to bootstrap.com --> components --> table. This will make our 'friends table' look nicer.

24) Within the index file you can change the <table> to class = "table", then add some things from bootstrap that you can find easily and put this within the class. Can see the changes on the website live.

25) Similar with buttons, bootstrap.com --> components --> buttons --> take an example of the button. At the bottom of the index page wher you can see the link to other pages, after the link you can add the class of a button and if you then visit the website you can see the button has been displayed in a much better way

26) Forms again is similar except bootstrap.com --> forms.
To make the changes do this within the friends --> _forms file. An example of a change that I made is:
I changed the class to mb-3 and added the class: "form-control" too.
See below:
<div class="mb-3">
    <%= form.label :twitter %>
    <%= form.text_field :twitter, class: "form-control" %>

```

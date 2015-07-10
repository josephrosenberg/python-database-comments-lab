# Python Database Blog Comments Lab

### An adventure in One-to-Many relationships

## Concept

This lab will expand your blog capabilities!  After this lab you will be able to comment on specific blog posts. This will demonstrate a One-to-Many relationship, where *one* post can have *many* comments.

## Objectives

+ Create a comment database model
+ Make a corresponding front end that allows users to create comments
+ Show a list of all posts and their comments

## Directions

1. Fill in the `Comment(ndb.Model)` with a `StringProperty` for a name, a `TextProperty` for the comment, and a `DateTimeProperty` that automatically records the date the record was created.
2. Add a `comment_keys` variable to the `Post` model and have it store a repeated list of `KeyProperty`s
3. Fill in the `CommentHandler` class so it can handle a `post()` request and will create a new comment and store it in the appropriate Post.
  + We have retrieved the post for you by storing its key in a hidden input field in the front end form
4. Open `index.html` and fill in the necessary HTML to make a form that posts to `/comment` and sends the commenters name and comment to the back end.


2. Fill in the `get()` of `MainHandler` so it queries for all the posts and sends it to the template to render
  + It might be good to just print the values to the console or send the raw text with `self.response.write` until you flesh out the frontend
3. Build up the frontend HTML so it can display all the posts.
4. Add a form to the front end that posts to the `/` root url with a new title and content for a post.
5. Fill in a `post()` method in `MainHandler` that gets the data from the form, creates a new `Post`, and stores it in the datastore.

## Stretch

+ Make the site look better with CSS and more creative HTML
+ Validate comment content and commenter name
+ Add an email field
+ Try to flip the relationship and store the single post on each comment
  + How does this change your needs on the front end?

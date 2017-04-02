## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?

`rails new` followed project name, and then other options as you wish (e.g. set what type of server, leave out minitest, specify rails version.

2. What do Models generally inherit from in rails?

In Rails 4, `ActiveRecord::Base`. In Rails 5, it is something else - maybe `ApplicationRecord`, which inherits from ActiveRecord::Base

3. What do Controllers generally inherit from in a rails project?

Application Controller, which inherits from `ActionController::Base`

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?

In `routes.rb`, add `get '/horses/:id', to: 'horses#show'` or `resources: horses, only: [:show]`. I'd probably do the second to make it easier to add another route later.

5. What rake task is useful when looking at routes, and what information does it give you?

`rake routes` gives a lot of information about each route - prefix, which gives the path helper name, verb which is what kind of request, uri pattern which gives the url path pattern, and the controller action which gives the controller it is sending the request to, and which action (method) within that controller it should hit.

6. What is an example of a route helper? When would you use them?

`categories_path` is a helper to get to the index of all categories. You can use them instead of hard-coding the path into your view - easier to maintain, don't have to update one by one if something changes.

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

`_path` gives the relative path whereas `_url` gives the full absolute path. I think the latter would be used when you have to references the full path, or something outside your app (?).

8. What are strong params and why are the necessary?

Strong params specify what parameters can be passed in - this is important for security and built into Rails, otherwise a malicious user could add whatever parameters she wanted and cause damage, get somewhere in the app that she shouldn't, e.g. admin-only views.

9. What role does `form_for` play in helping us create our forms?

It is a helper to create a form for an object. It is a quick way to create the necessary html input tags and associated information (title, name, type).

10. How does `form_for` know where to submit the user's input?

**(?)** It knows based on the specified object

11. Create a form using a `form_for` helper to create a new `Horse`. 
```ruby
<%= form_for @horse do |f| %>
<%= f.label :name %>
<%= f.text_field :name %>

<%= f.label :hands %>
<%= f.text_field :hands %>

<%= f.submit %>
<% end %>
```

12. Why do we want to validate our models?

To make sure the data we have is consistent and complete.

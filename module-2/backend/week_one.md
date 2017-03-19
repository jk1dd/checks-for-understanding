## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.
>GET - client asking for information

>POST - submit new data

>PUT - update data

>DELETE - remove data
2. What is Sinatra?
>Sinatra is a web app framework, and it comes with specific language
4. What is MVC?
>(M)odel, (V)iew, (C)ontroller - three main components of a web application (that follows the MVC pattern). Controller is the server file, models are the objects (also talks to database), and views are what renders and allows a user to interact with an app.
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
>Following conventions allows for clearer code, more easily understood and supported by others (and future selves), and it Sinatra requires certain things to follow guidelines (as it is looking for key words).
6. What types of variables are accessible in our view templates without explicitly passing them?
>??
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    erb :index
  end
  ```
>Insert @count = 1 above erb :index
8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
>`erb: index, locals: {name: "Mr. Ed"}`
9. What's the purpose of ERB?
>ERB allows for HTML formatting (and CSS and additional styling) as well as evaluating Ruby within it.
10. Why do I need a development AND test database?
>Development allows you to build out the application, and do whatever you have to, but testing must be clean and consistent, to make sure it will work in production.
11. What's responsive design?
>Design that automatically responds to the size and type of screen.
12. What is CRUD and why is it important?
>(C)reate, (R)ead, (U)pdate, (D)elete. The essential and basic actions of how a user interacts with data through an application. Important to allow for these things to happen.
13. What does HTTP stand for? 
>HyperText Transfer Protocol
14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
>One way just evaluates (<% >), where another also displays (<%= %>)
15. What's an ORM?
>Object Relational Mapper - mapping data as objects.
16. What's the most commonly used ORM in ruby (Sinatra & Rails)?
>ActiveRecord
17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
>get '/restaurants' - view all restaurants(read)

>get '/restaurants/new' - view form to create new restaruant (create)

>post '/restaurants' - click submit to save restaurant (create)

>get '/restaurants/:id/edit' - view form to edit restaurant (update)

>put '/restaurants/:id' - click submit to save changes (update)

>delete '/restaurant/:id' - delete restaurant (delete)


18. What's a migration? 
>You need a migration each time something changes with the tables in your db - creating a new table, dropping an old, adding columns, or changing header names
19. When you create a migration, does it automatically modify your database?
>No, you have to run the migration to update your database
20. How does a model relate to a database?
>A model interacts with the database (and performs calculations if need be) in order to retrieve/provide the data requested/sent by the client via the controller.
21. What's the difference between agile workflow and waterfall method?
>Agile workflow is an iterative process, focused on sprints of smaller (but fully functioning) pieces of software. Waterfall method, the more traditional approach taken from business and manufacturing, involves planning the whole project out at the beginning, and following that path. Waterfall tends to have worse outcomes.
22. What is the difference between `#new` and `#create`?
>`#new` creates a new instance of the model object, but does not save it. `#create` creates that instances and saves it.

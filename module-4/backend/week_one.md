## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's the most useful thing you learned from completing the intermission week work?

Basic Javascript syntax - makes it easier to look at. Also, the exercises for iterating were useful to complete the sorting algorithims.

2. What are some tools to help debug JavaScript code?

`debbuger;` will stop the code if you have the console open. `console.log` to print out to the console what you would like to see.

3. What are some tools you need in order to unit test your JavaScript?

The mocha library to run tests, and the chai library to have assertions.

4. What is the syntax for invoking a function?

`sampleFunction()` the parentheses on the end (and any arguements needed) invokes the function. Without the parens, it won't be invoked.

5. What's the difference between `==` and `===` in JavaScript?

`==` checks for equality, but `===` checks for equality of both value and datatype. It is better to use `===` pretty much always, to my understanding.

6. What's the difference between asynchronous and synchronous JavaScript? 

Synchronous JavaScript happens in order, whereas asynchronous happens in different order. Both powerful and tricky.

7. How do we setup a route when creating an API with Node and Express?

`app.get('/api/foods', function() {}` with the get being replaced by the verb of the route

8. What do we use Knex for?

It is sort of an ORM, but less featured than ActiveRecord.

9. What's `npm` and what do we use it for?

'Node Package Manager' which allows us to install external libraries and packages.

#### Review  
10. What's the MVC design pattern? Describe each part of MVC?

Model-View-Controller. It is one pattern for organizing an application. Model refers to the objects involved in your application. Views are what is displayed to the user. Controller takes requests and sends them to the right place. Controller sends to Model, which talks to the database (if needed) and then what was requested is displayed to the View.

11. What is AJAX? What are some benefits of using AJAX?

AJAX allows you to make a call to the database without refreshing the page. It is writting in JavaScript (jQuery?). It is useful for updating things immediately.

12. What's a background worker? When would we want to use a background worker?

Background workers are tasks set to run in the background - an example of asynchronous code in Rails. We would want to use one if we had something that takes a bit longer to execute (e.g. emailing a user) where the user doesn't have to wait around.

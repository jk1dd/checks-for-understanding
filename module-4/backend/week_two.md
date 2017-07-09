## Week Two - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What is Webpack and why is it useful?

Webpack is a way to take all your developer-friendly things and mash it down to a more effienct, computer-friendly format. This includes minifying (or uglyfying), converting es6/7 into es5, and putting all javascript in one file.

2. When do you want to use event delegation?

Event delegation can happen because of bubbling. Add an event listener to a parent, and then it can fire for its descendants (had to look this one up).

3. What's one difference between ES5 and ES6?

ES6 can do string interpolation with backticks. There is also a rocket notation thing rather than passing a callback function, but i haven't used it yet.

4. What's the deal with semi-colons in JavaScript?

They used to be necessary, but they are pretty much optional now, except on some single line things (I'm thinking of a for loop, for example). They are inserted automatically.

5. How are you using the MVC design pattern in your Quantified Self project?

We have pulled out actions into a router and a controller. We also have files named after objects that contain methods for that object. Not true models yet though.

6. How do you execute raw SQL in node?

We are using knex.raw() and putting SQL in quotes inside that. There may be another way?

7. What's a callback function and what are some reasons when we use/need callback functions?

A callback function is a function that is passed to another function as a parameter, and then called inside that other function. We use them to execute functions within other functions, like in jQuery when we pass a callback to be executed later on some event, or when we iterate through an array.

8. What is CORS?

Cross Origin Resource Sharing. Allows resources to be requested from another domain - generally restricted for security reasons.

9. What are some steps to avoid CORS?

?? Allow it in your application?

#### Review  

10. Why do people say "HTTP is stateless"?

Each HTTP request is a blank slate, without a state. 

11. What is a RESTful API?

A RESTful API follows the RESTful conventions/language of REST, so others know what to expect.

12. What are some main characteristics of a team following an agile workflow?

MVP delivered ASAP, constant feedback loop, iterative process. Daily short standups, sprints.

13. What are some advantages/disadvantages to using OAuth to authenticate a user?

Advantage - outsource security, make it easy for user to sign up, add legitimacy
Disadvantages - no control over security, other application could get compromised

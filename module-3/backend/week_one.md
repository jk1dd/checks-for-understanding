## Week One - Module 3 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. What is `json`, what does it stand for, and why is it important?

JavaScript Object Notation - it looks like a hash but isn't one. It needs to be parsed to be readable.
1. What kind of object is JSON in Ruby? How do we know it's JSON?

Hash - we know because it looks like a nested hash thing?
1. What's the difference between `joins` and `includes` in ActiveRecord?

Actually I am not sure! I am guess it is the kind of join (e.g. inner vs left). 
After some research, it looks like includes will just get you the relevant relationship you are asking about, whereas joins will join the whole table.
1. What's an API?

Application Programming Interface - a way for programs to talk to each other (and send data back and forth)
1. How do we test an internal API (in general)?

Request specs - navigate to the endpoint and make sure the data we expect to be there is there.
1. What are two different ways to customize your `json`?

Not sure! After looking it up - JBuilder or Serializer.
1. If the the methods below return collections, what object (class) will they return? What kind of objects will be returned inside of that object?
   * `.find_by_sql` - not sure - docs seem to say the model object
   * `.connection.execute` - Something deeper, don't remember
   * `.where` - ActiveRecordRelation object, with objects inside
1. (Security) What is SQL injection? When can it happen? How can you prevent it?
1. What do you need to do differently when you adding `POST`, `PUT`, and `DELETE` endpoints to your API when using the `--api` flag when creating a Rails app versus not using the flag?
   * Hint: What class does `ApplicationController` inherit from when creating a Rails project with the `--api` flag? What about without the `--api` flag? What do they do differently? Why?
1. What's your process for solving advanced SQL or ActiveRecord lookups?

Draw it out, draw arrows to plan what is needed, break it down and solve piece by piece.

#### Review  
6. What is an ORM, what does it stand for, and why is it helpful?

Object relational mapping - make objects from things on tables. Then you can use them in OOP.
7. How do you create a record in the following table in SQL? In Active Record?   
   (Users table with columns first_name, last_name, email, and age)
8. Given an array numbers = [1,2,3,4,5], find the sum of the doubles of all the numbers.

`numbers.map {|n| n * 2}.reduce(:+)`

#### Self Assessment  
Rate yourself on the following scale.  
4  I know and understand all these concepts and did not have to look anything up  
3  I know and understand most of these concepts but had to look something up  
2  I am uncertain about some of these concepts and had to look some things up ^^  
1  I am feeling lost about with these concepts and had to look many things up ^^  

^^ Please let an instructor know where you'd like support to catch you up. 

Probably 2.5 or maybe a 3. Nothing I've never heard of before, but had to do some googling.

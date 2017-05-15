## Week Two - Module 3 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. What's OAuth?

OAuth is using and external service to authenticate your users.
2. What are some advantages/disadvantages of implementing OAuth?

Advantages include ease of use - outsource the need for secure authorization to another company. 
3. How many exhanges of information need to take place before a user is authenticated with OAuth?

I think 3 - user goes to your applications, hits "authorize with w/e", redirected to that site where they sign in, then that site sends back a token so your app can make requests on behalf of that user. Also user is redirected back to your application.
4. Why do we want to create services?

Separate responsibility in the application?
5. Why is it good practice to create PORO's with the data received from an API?

Not sure, beyond keeping responsibility separated, and code clean and durable for your future self and other devs.
6. What do we use VCR for? Why is it a good idea to use this tool?

VCR records an API call, then uses that to run tests against instead of the real thing. It works at the rack layer (I think). This is good because it makes your tests faster and doesn't rely on network connectivity. However, your tests won't fail if the API changes - it will still be using the old cassette - so your application can break without much warning.

#### Review  

7. What does HTTP stand for?

Hypertext Transfer Protocol
8. How do you create the following table in SQL? In Active Record?   
   (Users table with columns first_name, last_name, email, and age)   
   
In SQL - I'd have to google it. CREATE table is a thing I know though.
In Active Record - `rails g model User first_name last_name email age:integer`
9. Writing Files: given a text file located at "/Documents/pizza.txt", write code to read the file from the filesystem, then    write a new file at "/Documents/line_count.txt" containing the number of lines in the original file.  

Uh oh. 

#### Self Assessment  
Rate yourself on the following scale.  
4 I know and understand all these concepts and did not have to look anything up  
3 I know and understand most of these concepts but had to look something up  
2 I am uncertain about some of these concepts and had to look some things up ^^  
1 I am feeling lost about with these concepts and had to look many things up ^^  

^^ Please let an instructor know where you'd like support to catch you up. 


2.5 or 3 I think.




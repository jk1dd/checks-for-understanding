## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
> ActiveRecord allows for easier communication/interaction between your models and your database - allows you to set up more straightforward queries.
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
>`Team.all`, `Team.find(1)`, `Team.find_by(name: "Team")`, `Team.where(size: 55)`, `Team.order(size: :desc)` and many more. The arguments they take will be different depending on the attributes of the team instance (aligning with column names). You can access them because they are acting as shortcuts to queries on the database, in this case the Team table.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
>`Team.find(4)` to find the team object, `Team.find(4).name` should return the name as a string. Without an owners table, I am not sure how you would find the owner with only the code in question 2. You could find the ownder_id with `Team.find(4).owner_id` but then you would need to find some way to match it to the name of the owner.

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
>Now you could find the owner by calling `Team.find(4).owner.name`, since the relationship is set up so that the owner id in the team object would match with the primary key of owner in the owner table, from which you could return the name.

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
>This would be a many-to-many relationship. One student will have many teachers, and one teacher will have many students. You could represent this with a join table that includes an id, student_id, and teacher_id. Relationships would be set up in the models, e.g. in Teacher, has_many :students, through :teacher_students
6. Define foreign key, primary key, and schema.
>Foreign key is the primary key of another table, included to establish the relationship between two entities.
>Primary key is the unique identifier of each record in a table, usually an integer, that is never reused or repeated
>Schema is your 'source of truth' for what tables and relationships are in the database.
7. Describe the relationship between a foreign key on one table and a primary key on another table.
>The foreign key on a table is the primary key of another table. In a one to many relationship, the primary key of the one becomes the foreign key on each instance of the many
8. What are the parts of an HTTP response?
>?? status code, header, body


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
>`Model.first` - takes the first instance of a Model object
>`Model.create(attributes here)` - create an object in your database
>`Model.group(:status).count` - haven't used this yet, but would return a hash with status name as key, and count as value
>`Model.join(:things)` - also haven't used, but this returns a model object for all objects with things
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
>are all rake tasks ActiveRecord? if so `rake db:drop`, `rake db:migrate`, `rake db:test:prepare`
3. What two columns does `t.timestamps null: false` create in our database?
>created_at and updated_at
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
>One school has many teachers, but each teacher has one school. One-to-many relationship.
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
>Each teacher object will need a school_id (as foreign key) that is the primary key of the school
6. Give an example of when you might want to store information besides ids on a join table.
>When there is relevant information to be stored at that relationship. The example that always comes up in class is students and courses - many to many relationship, but also there is a grade for each student in each course. So the join table course_students would have id, student_id, course_id, and grade.
7. Describe and diagram the relationship between patients and doctors.
>In a primary care setting, probably one to many. One doctor has many patients, each patient only has one doctor.
8. Describe and diagram the relationship between museums and original_paintings.
>One to many - one museum has many paintings, each painting can only be in one place at once.
9. What could you see in your code that would make you think you might want to create a partial?
>a form that gets used more than once (e.g. for creating a new object and editing an existing)

## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
** ActiveRecord is an ORM, which allows us to communicate with the database without using SQL. It also makes is so that it works regardless of the type of database (postgresql, sqlite3, etc.) doesn't matter. **

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

** Team will have methods such as all, first, last, pluck, group, and lot more, all of which are available through ActiveRecord. **

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

```ruby
team = Team.find(4)
team.name
```

```
owner_id = team.owner_id
owner = Owner.find(owner_id)
```

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
```
team.owner
```

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
6. Define foreign key, primary key, and schema.
7. Describe the relationship between a foreign key on one table and a primary key on another table.
8. What are the parts of an HTTP response?
3. What do they allow you to do?
^^This question has no context, and therefore no response.
7. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

table: students        teachers
name                   name
teacher_id

8. Define foreign key, primary key, and schema.
A foreign key is an id that references a row in another table. A primary key is a unique identifier for a row in a table. A schema represents the structure of the database.
9. Describe the relationship between a foreign key on one table and a primary key on another table.
The primary key of a row becomes its foreign key in another table.
10. What are the parts of an HTTP response?
Headers, body, verb, and status code.
11. Describe some techniques to make our Sinatra code more DRY. Give an example of when you would use these techniques.
Using the layout erb is one way to DRY, as well as making an application controller that holds the basics that other controllers could inherit. I'd use the application controller (which is set up in Rails) to hold variables and methods I need in all controllers.


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
** 1: Average, so I never have to do an average myself again.**
** 2: Pluck, which gives you just the attribute you specify. **
** 3: Where, which allows me to specify what I'm looking for with multiple attributes. **
** 4: Joins, which lets me make a temporary join table to get shit done. **
** 5: to_sql, which displays the SQL behind the request it is called on. This helps me verify what is happening in SQL.**
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database?
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?
** 1. Migrate: I like giving databases structure. And honestly, where would we be without it? **
** 2. Drop: Goodbye, tables. I use this to ensure my migrations are running fresh on an empty database. **
** 3. Seed: Seed populates the database with the data from the seed file. I'm pretty good at it. **
4. What can you expect from a group as you begin working together? As you continue working together?
** This feels pretty subjective. I expect everyone to DTR honestly and efficiently, and communicate often. As we continue working together, I expect my group to retro daily, work through any tensions, and focus on deliverables.**
5. What two columns does `t.timestamps null: false` create in our database?
** Created at and Updated at **
6. What cURL flag can you use to send a `POST` request?
** curl -d **
7. What case does JSON (and JavaScript) use for multi-word variables?
** Camel case. **
8. What case does Ruby use for multi-word variables?
** Snake case **
9. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
** A teacher belongs to a school. A school has many teachers. The teacher will have a school id. **
10. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
** Tables **
** teachers **  ** schools **
   name             name
   school_id
11. Give an example of when you might want to store information besides ids on a join table.
** I could store other information about the relationship in the join table, like the timestamps documenting the beginning of the relationship. **
12. Describe and diagram the relationship between patients and doctors.
** Patients belong to a doctor. Doctors have many patients.**
** Tables **
** patients ** ** doctors **
    name          name
    doctor_id

** I guess a patient could have many doctors. **
** patients **  ** doctors **  ** doctorpatients **
   name             name          doctor_id
                                  patient_id

13. Describe and diagram the relationship between museums and original_paintings.
** Paintings belong to a museum. A museum has many paintings. **
** Tables **
** paintings **    ** museums **
   name               name
   museum_id
14. What are some examples of acceptable values for the parts of an HTTP response?
** The header holds metadata, which can include date, content type, and status. The body holds the actual data for the page.**
15. What types of output do we want to test when we test our controllers?
** I guess you could test the status code and the instance variables. **
16. What could you see in your code that would make you think you might want to create a partial?
** My new and edit forms are really similar, so I would put that into a partial. **
17. Why might you use a helper method?
** Helper methods can save you time and help write DRY code. **

## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?

    At a high level ActiveRecord is a DSL that wraps the SQL language for easier
    interactions with databases in Rails.

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

  Some methods you can call are .all, .find, .where, .group and .count. You have access to these methods because
  the model is inheriting them from ActiveRecord, they are ActiveRecord methods.  

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?



4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

   You would find the row by id and call the name of that row like this Team.find(4).name.

5. In a database that's holding students and teachers, what will be the relationship between students and teachers?  Draw the schema diagram.

   This would me a many to many relationship. A student has many teachers and a teacher has many students.

6. Define foreign key, primary key, and schema.

   A foreign key is the key the creates a relationship between two tables, a primary key is the key each indivual row of a table and a schema is reference to the layout of the database.

7. Describe the relationship between a foreign key on one table and a primary key on another table.

    The foreign key on one table is associated with the primary key on another if the keys correlate. A table's
    primary key is tied to another table through a foriegn key.

8. What are the parts of an HTTP response?
    the start line, the header and the body


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database?
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources
* I was able to answer most questions independently, but utilized outside resources for a few
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel confident about the content presented this week
* I feel comfortable with the content presented this week
* I feel overwhelmed by the content presented this week
* I feel quite lost by the content presented this week

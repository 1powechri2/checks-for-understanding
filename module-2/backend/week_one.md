## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
    1. Get - retrieves a resource
    2. Post - Creates a new resource
    3. Patch - changes an aspect of a resource
    4. Put - changes all aspects of a resource
    5. Delete - destroys a resource

2. What is Sinatra?
    It is a platform for creating web based applications with the ruby language.

3. What is MVC?
    It is an acronym that stands for Model View Controller and it is a popular
    format for web based applications. It is a way to divide specific logic into
    separate objects.

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
    Convention sets a way for people to recognize the intentions of

5. What types of variables are accessible in our view templates without explicitly passing them?
    local variables and instance variables

6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
    name = 'Mr. Ed'

8. What's the purpose of ERB?
    to use the ruby language inside of html files

9. Why do I need a development AND test database?
    The development db holds the actual tables used in the app,
    the test db holds small tables for testing that can be manipulated.
    Tests can damage the actual tables used in the db.

10. What is CRUD and why is it important?
      It is an acronym for create, read, update, destroy and these are the fundamental
      operations used in handling data.

11. What does HTTP stand for?
      Hypertext transfer protocol

12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
      There are the brackets <% %> and <%= %>, the latter one prints to the browser

13. What's an ORM? What does it do?
      Object Relational Mapping treats the rows of a database table like objects,
      in the case of ActiveRecord they are treated like class instances.

14. What's the most commonly used ORM in ruby (Sinatra & Rails)?
      ActiveRecord

15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
      Create - Post  '/restaurant/index'
      Read   - Get   '/restaurant/index'
      Read   - Get   '/restaurant/id'
      Update - Put   '/restaurant/id'
      Update - Patch '/restaurant/id'
      Destroy- Delete'/restaurant/id

16. What's a migration?
      A migration is a file that describes the architecture for a db table.

17. When you create a migration, does it automatically modify your database?
      No

18. How does a model relate to a database?
      The model provides the class through which the app can access the database.

19. What is the difference between `#new` and `#create`?
      New is a ruby method and create is an ActiveRecord method.


### Review Questions:  
20. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?
    require 'csv'

    CSV.foreach('./data/films.csv', headers: true, header_converters: :symbol) do |film|
    Invoice.create(id: film[:id],
                  title: film[:title],
                  description: film[:description])

21. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}
```
How would I add 'granola bar' to things you should have when hiking?
  activities[hiking][supplies].push('granola bar')

22. What are the 4 Principles of OOP? Give a one sentence explanation of each.
      Encapsulation - hide data from external sources
      Abstraction   - classes use each other but don't know how they work
      Inheritance   - the sharing of behaviors from other classes
      Polymoprhism  - An occurance of several phenotypes within a species. I don't
      know


### Self Assessment:
Choose One: (erase the others)

* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:

* I feel comfortable with the content presented this week

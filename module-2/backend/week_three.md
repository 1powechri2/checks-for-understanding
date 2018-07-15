## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?

    rails new app_name

2. What do Models generally inherit from in rails?

      Models in rails inherit tables stored in the database

3. What do Controllers generally inherit from in a rails project?

      Controllers in rails inherit from the rails routes

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?

      You would put this code inside the routes folder `resources :horses`. Then you would create a show action in the controller that would create the route where you would be able to see a specific horse by its id.  

5. What rake task is useful when looking at routes, and what information does it give you?

      The task is `rake routes`, It provides a list of all the routes that rails has created for the resources you have built.

6. What is an example of a route helper? When would you use them?

      A route helper is a specific code that wraps the the actual url of a request for example /horses
      becomes horses_path in rails. You can use is when redirecting a page and you can use it when writing
      test in rails.

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

      I'm guessing _url is the entire url request whereas the _path comes after the domain name.

8. What are strong params and why are they necessary?

      Strong params are a hash containing only the key value pairs that you allow them to. This is necessary
      to keep users from gaining access to other parts of the params and restricting use to only the data necesary
      for the action.

9. What role does `form_for` play in helping us create our forms?

      'form_for' is first part of code that is used in creating a form and it creates access to the variable that
      was passed to it.

10. How does `form_for` know where to submit the user's input?

      It knows from the variable it has been sent. The variable holds keys that form_for assigns the user
      input to.

11. Create a form using a `form_for` helper to create a new `Horse`.

      <%= form_for @horse do |f| %>
      <%= f.label :name %>
      <%= f.text_field :name %>
      <% end %>

12. Why do we want to validate our models?

      So we can make sure they always receive the data they need to be complete.

13. What are the steps of the DNS lookup?

      I honestly don't know.

### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?

      horse.moves.prance

15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?

      You walk two nodes to get to 3 wheras you only walk one to get to true.

16. What is inheritance?

      It is how classes get access to attributes and behaviors from other classes.

### Self Assessment:
Choose One:

* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:

* I feel comfortable with the content presented this week

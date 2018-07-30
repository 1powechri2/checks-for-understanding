### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?

    You create a flash hash inside an action method within a controller. When that action path is visited
    it prints the message to the screen.

2. Where is cart information/temporary information usually stored?

    Inside an instance of a PORO but it can also be stored in a database and deleted when certain conditions
    are met.

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?

    Reasons not to store a cart in a database are it requires extra relationships which requires users to have to log on before using the cart and it also requires lots of saving and deleting from the database which can
    result in unwanted database clutter.

4. What is the purpose of the asset pipeline?

    To compress all the code read by the browser so it loads faster and contains no unnecessary characters.

5. Why do we precompile our assets?

    I don't know.

6. What do each of the following tags do?

```ruby
<%= stylesheet_link_tag "application" %>

    This links a stylesheet file to the entire project.

<%= javascript_include_tag "application" %>

    Same as above but for javascript

<%= image_tag "rails.png" %>

    This is an image tag, it is the relative path for an image file within a rails project
```

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
    A Readme is a giant user story, the story applies to someone using the app itself or developers integrating
    the code. It describes the entire scope of the project and guides the user through all of its functions. It is
    also a great tool to help developers create an application that should function exactly as it describes.

8. What are the top four accessibility issues that we as developers should be aware of?
    Unregistered user functionality, registered user functionality,
    admin functionality and security functionality against intruders that wish to hack our app.

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?

    Before save is an example of a callback that occurs before an object is
    created. The only time we use it is to create a slug.

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)

  To do this you use we use rails helper called enum, the value true is created as an array index. Create a default value for this index where active = 0 which is not true. Using a boolean you create a method that looks at this index and if it equals 1 then the program knows that the user is active and it grants it special
  privileges.
```

11. What is the difference between a scope and a class method?

    a scope method creates a bias, it has variables and return values that are only accessed by the scope it
    creates, a class method is accessible to the entire possibility of that class, it does not depend on
    an instance and can query the entire database. This is totally wrong.


### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?

    session[:cart]["48"] = 4

  12b. How would you increase the quantity of item 29?

    session[:cart]["29"] += 4

  12c. How would you find out how many items your user is thinking about purchasing?

    sessions[:cart].values.sum

13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  

      Polymorphism is the inheritance of the same behavior for different objects. I don't know what duck typing is.

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  

    "(630) 854-5483".delete("(", ")").gsub([' ', '-'], '.')

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

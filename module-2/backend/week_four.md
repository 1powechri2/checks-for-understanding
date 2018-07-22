## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?

    It is a small piece of data that gets saved in a users browser so that we they visit a site they can
    be identified by the app.

2. What’s the difference between a session and a cookie?

    A session starts when a user logs in and ends when the user logs out.

3. What’s a flash and when do you want to use flashes?

    A flash is a message that pops up in the browser to verify if a user intended to do
    an action. It is usually used when a user is deleting something.

4. Why do people say “HTTP is stateless”?

    People say http is stateless because each response from a server is static and holds no
    record of the client or the clients who have visited it.

5. What’s authentication? Explain.

    Authentication is the process by which a user or client can be identified after they have created an
    account and granted access to certain pages or data.

6. What’s the difference between authentication and authorization?

    Authorization is the ability to identify a user in regards to their privilege to 'author' aspects
    of a website. It usually differentiates between an admin and a normal user.

7. What’s a before filter?

    A before filter is a method that is called upon a class before any other methods can be used.

8. How do we keep track of a user once they’ve logged in?

    We keep track of a user by assigning their id to the session hash which is then saved as an
    instance variable that is shared among all models.

9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?

    Namespacing a resource creates routes that are only allowed access by a certain role designation for a user.
    Nested resources are used for access to certain routes that require ids that relate to table relationships.

10. At a high level, what tools can you use to implement authorization? How would you use them?

      The tools used for authorization are user login, user role designations and namespacing routes. A user logs
      in and is identified as an admin through their role. The role in turn allows the user to access the admin routes that are defined by namespacing in the routes config folder.

11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?

      An enum is a method that reads an array by index and defines that index to a users role. You declare the enum
      inside the model/class for a user.

12. What are some strategies you can use to keep your views DRY?

      Strategies you can use to DRY up your code are before filters, private params methods and the erb render method
      for views where forms are repeated.


### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  

  Holiday.all.order(:name)

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?

    IIIII  DDD    K   KK     
      I    D  D   K KK      
      I    D   D  KK       :(      .....yet!
      I    D  D   K KK
    IIIII  DDD    K    KK  

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources

Choose One:

* I feel comfortable with the content presented this week

## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
  a cookie is a bit of data stored by the browser and sent to the server with every request. 
2. What’s the difference between a session and a cookie?
  a session is a collection of data stored on the server and associated with a given user (usually via a cookie containing an id code.)
3. What’s a flash and when do you want to use flashes?
  is a special part of the session which is cleared on each request. This means that values stored in the flash will only be available in the following request.
    can ues it to pass along messages to the user.
    use it to send identifiers to your views.
4. Why do people say “HTTP is stateless”?
  HTTP is stateless because the connection between the browser and the server is lost once the transaction ends.
5. What’s authentication? Explain.
  process of verifying someones credentials.
6. What’s the difference between authentication and authorization?
  Authentication is the process of verifying someone or something.
  Authorization is essentially what the authenticated is able to do.
7. What’s a before filter?
  it states what should be done prior to a specific event or action.
  Like logging in a user or setting current_user to admin before executing various tasks.
8. How do we keep track of a user once they’ve logged in?
  through the session.
9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
  resources created in one namespace are hidden from other namespaces. This can be used to determine authorization levels. Nesting resources makes those resources hidden in that namespace, but it also changes the routes for that resource.
10. At a high level, what tools can you use to implement authorization? How would you use them?
  namespacing, enums, sessions.
  namespacing admin and nesting resources within. Using user roles and enums to specify user type. Storing this info in the session as current_user.
11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
  An enum is a way to change and store variable status. Typically used with limitd options like status' or user types. A way to set flags and change a methods actions based on the enum value.
12. What are some strategies you can use to keep your views DRY?
  sending some of the work, when possible, to your models.

### Reviews Questions 
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
holidays = [
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  

sorted = holidays.sort_by! do |element|
      element[:holiday][:name].downcase
    end

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300? 


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week

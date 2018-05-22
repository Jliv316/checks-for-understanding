## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
1. Rails new example_project -T -d="postgresql" --skip-spring --skip-turbolinks

2. What do Models generally inherit from in rails?
2. ApplicationRecord

3. What do Controllers generally inherit from in a rails project?
3. ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
4. Resources :horses, only: [:show]

5. What rake task is useful when looking at routes, and what information does it give you?
5. Rake routes - the current established routes for your application

6. What is an example of a route helper? When would you use them?
6. horses_path(horse) to visit a path

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
7. URL returns the entire url ‘http:yadayadayada’ for the specific route where _path just returns the path ‘/horses’

8. What are strong params and why are they necessary?
8. Strong params help protect what information your application will accept from user params.

9. What role does `form_for` play in helping us create our forms?
9. Form_for gives us an easy way to generate a well crafted form.

10. How does `form_for` know where to submit the user's input?
10. Based on the given instance variables and order they are entered into the form_for array [@company, @job].

11. Create a form using a `form_for` helper to create a new `Horse`. 
11. form_for @horse do |f|
    1. f.label :type
    2. f.text_field :type
    3. f.label :name
    4. f.text_field :name
    5. f.submit
    6. End
    7. All in erb tags

12. Why do we want to validate our models?
o make sure that we aren’t populating our database with objects that have nil fields where we expect actual values.

13. What are the steps of the DNS lookup?
13. Browser sends domain name to DNS where it checks its database for an IP address that matches that domain name. Grabs that IP address and sends to server.


### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?
14. prance

15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3? 
furniture[:purchased] returns true
furniture[:table][:height]

16. What is inheritance?
Essentially taking all qualities and functions of another thing whether that be a controller, model, module, etc.

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources

Choose One:
* I feel confident about the content presented this week

### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

### Week 5 Questions
1. How do we make flash messages display on a page?
  flash[:success] = "You created #{@station.name}"
2. Where is cart information/temporary information usually stored?
  In the session
3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
  A users cart changes so frequently, that storing it in the database would require a disgusting amount of pulls from the database in turn slowing down your application.
4. What is the purpose of the asset pipeline?
  To compile all of your assets at one time so we aren't making incremental pulls from the server.
5. Why do we precompile our assets?
  To grab all of your css files, js, etc. in one shot. To speed up your application.
6. What do each of the following tags do?

```ruby 
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```
  each returns a tag or link tag for the given arguments. 

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
  The read me file is the face of your project. If a user cannot code, or doesn't have a strong enough background to read through tests, the readme file is the most important peice of information.
  Even if the user does have a programming background, we can save a lot of investigation time by writing a good read me file. 
  Also, it looks really good for future employers etc.
8. What are the top four accessibility issues that we as developers should be aware of?

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
  callback method. It would be found in the model level.
10. Given the following object, how would we create a scope for all users who are active?

```ruby 
User.create(name: "Happy", active: true)

```
  scope :active_users, {where(active: true)}

11. What is the difference between a scope and a class method?
  scopes and class methods are very similar in a lot of ways. I found that scopes will always return a relation
  whereas class methods will not.
  scope :by_status, -> status { where(status: status) if status.present? }
  Scope above: and Class method below:
  def self.by_status(status)
    where(status: status) if status.present?
  end
  the class method will not work as written. Must write as:
  def self.by_status(status)
  if status.present?
    where(status: status)
  else
    all
  end
end

### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4? 
  cart = {cart: {"17" => 4, "204" => 52, "29" => 22}}
   cart[:cart]["48"] = 4
  12b. How would you increase the quantity of item 29?  
    cart[:cart]["29"] += 1
  12c. How would you find out how many items your user is thinking about purchasing?   
    cart[:cart].values.sum
13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?   
    It's the ability to present the same interface for differing data types.
    duck typing is code that accepts any object that has a particular method.
    overloading and overriding
14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
  string = (string.gsub(/[()]/, ""))
  string = (string.gsub(/\D/, "."))
### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week

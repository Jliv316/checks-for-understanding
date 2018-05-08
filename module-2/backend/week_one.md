## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
  - GET: retrieve a resource from a url
  - POST: create a new resource
  - PUT: update an entire resource
  - PATCH: update a part of a resource
  - DELETE: remove or destroy a resource
2. What is Sinatra?
  - Free open source software web application library and domain specific launguage written in Ruby.
   - it is a Ruby web application framework.
4. What is MVC?
  - Model, view, controller.
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
6. What types of variables are accessible in our view templates without explicitly passing them?
  - instance variables defined in our controller.
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
  - @name = 'Mr. Ed'
9. What's the purpose of ERB?
  - Used to describe how data should be used to create HTML.
10. Why do I need a development AND test database?
  - Our development database is the actual database you will use to interact with your application. The Test database is seperate and 
    is a great way to test out your code without affecting your actual database.
11. What is CRUD and why is it important?
  - Create, Read, Update, Delete. Which is a list of operations that can be preformed on a resource.
12. What does HTTP stand for? 
  - Hyper Text Transfer Protocol.
13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  - <% %> does not render the the return value. <%= %> renders the return value of the enclosed statement.
14. What's an ORM?
  - Object Relational Mapping. Allows us to easily interact with our relational database by mapping rows in the database to ruby objects.
15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  - ActiveRecord
16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  1) READ '/restaurants' GET - a view of all restuarants from index.erb
  2) READ '/restaurants/:id' GET - a view of a specific restaurant from show.erb
  3) CREATE '/restaurants/new' GET - a form to create a new restaurant in new.erb
  4) CREATE '/restaurants' POST - data to the server and redirect to '/restaurants'
  5) UPDATE '/restaurants' GET -  a form to update an existing restaurant in edit.erb
  6) UPDATE '/restaurants/:id/edit' PUT - data to the server to update an exhisting restaurant's information
  7) DELETE '/restaurants/:id' DELETE - existing information
17. What's a migration? 
  - Migrations hold instructions that can be used to laster create a data base when running rake db:migrate
18. When you create a migration, does it automatically modify your database?
  - It does not
19. How does a model relate to a database?
  - The model interacts with the database and holds methods to a particular resource.
20. What is the difference between `#new` and `#create`?
  - new generates a new instance of an object while create generates a new instance and saves it to the database.
### Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?
  - class CSVWizard
  def self.read_file(filename)
    CSV.open(filename,
             headers: true,
             header_converters: :symbol)
    end
  end
22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone'],
  brunch: {cost: $35, supplies: ['mimosa flutes'],
  antiquing: {cost: $200, supplies: ['list of antique stores'] 
}
```
How would I add 'granola bar' to things you should have when hiking?
activities[:hiking][:supplies] << "granola bar"
23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
  1) Encapsulation - THe implementation of hiding data by restricting access to public methods.
  2) Abstraction - a concept or idea that is not associated with any particular instance.
  3) Inheritance - expresses an "is a" relationship between two objects. Using proper inheritance,in classes, we can reuse the code of existing super classes.
  One entity can inherit attributes from another entity.
  4) Polymorphism - means "having many forms". Having the same method with modifications. Overiding and overloading.
### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few 

Choose One:
* I feel comfortable with the content presented this week

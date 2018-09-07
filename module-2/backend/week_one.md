## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
  ```
  GET to retrieve a resource from a URL
  POST to create a new resource
  PUT to update an entire resource
  PATCH to update a part of a resource
  DELETE to delete a resource
  ```

2. What is Sinatra?
  ```
  A lightweight Rack-based, Ruby framework that allows to easily interact with the web. It has a Domain Specific Language that facilitates this interaction.
  ```

3. What is MVC?
  ```
  Model = Interacts with the database
  View = What we display on the browser
  Controller = The middleman between what is displayed (views) and gathering the information from the database (models)
  ```

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  ```
  Because REST is implemented across the web and provides a consistent and easy-to-follow interface for the client.
  ```

5. What types of variables are accessible in our view templates without explicitly passing them?
  ```
  Instance variables.
  ```

6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  ```ruby
  get '/horses' do
    erb :index
  end
  ```
  ```
  get '/horses' do
     @count = 1
    erb :index
  end
  ```
7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
  ```
  get '/horses' do
    erb :index, :locals => {:name => 'Mr. Ed'}
  end
  ```
8. What's the purpose of ERB?
  ```
  Embedded RuBy = allows us to use ruby and html in the same file.
  ```
9. Why do I need a development AND test database?
  ```
  To keep responsibilities clear. Having a shared database would make brittle code that is harder to test.
  ```
10. What is CRUD and why is it important?
  ```
  Create, Read, Update, Destroy = it is how we interact with a resource such as horses
  ```
11. What does HTTP stand for?
  ```
  Hypertext Transfer Protocol
  ```
12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  ```
  <% %> does not print information within carrots
  <%= %> prints information within carrots
  ```
13. What's an ORM? What does it do?
  ```
  Object Relational Mapper = a way for us to create objects from rows of a database table for easy interaction.
  ```
14. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  ```
  ActiveRecord
  ```
15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  ```
  GET /restaurants => To see all restaurants
  GET /restaurants/:id => To see one restaurant
  GET /restaurants/new => To be taken to the page to add a new restaurant
  POST /restaurants => To create and save a new restaurant
  GET /restaurants/:id/edit => To be taken to the page to edit a restaurant
  PUT /restaurants/:id => To edit and save a restaurant
  DELETE /restaurants/:id => To remove a restaurant
  ```
16. What's a migration?
  ```
  Instructions for how to modify the database.
  ```
17. When you create a migration, does it automatically modify your database?
  ```
  No. You have to run the migration using a rake command (rake db:migrate)
  ```
18. How does a model relate to a database?
  ```
  The model relates to a table in the database, and the relation of its tables to other tables.
  ```
19. What is the difference between `#new` and `#create`?
  ```
  new creates a new instance but does not save unless .save is called.
  create both creates a new instance and saves it all at once
  ```
20. Given a table named `animals`, What is the SQL query that will return all info from that table?
    `id     name        number_of_legs
    -----   ------      --------------
      1     panda       4
      2     giraffe     4
      3     whale       0
      4     bird        2
    `
    ```
    SELECT * FROM animals
    ```
21. Using the same table, What is the SQL query that will return only the animals that has 4 legs?
    ```
    SELECT * FROM animals WHERE number_of_legs = 4
    ```
### Review Questions:  
22. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
```
CSV.foreach("db/csv/films.csv", :headers => true, header_converters: :symbol) do |row|
film = Film.create(title: row[:title],
              description: row[:description])
```

23. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}
```
How would I add 'granola bar' to things you should have when hiking?
```
activities[:hiking][:supplies] << 'granola bar'
```

24. What are the 4 Principles of OOP? Give a one sentence explanation of each.
```
Encapsulation -- Only expose information and behavior that must be exposed to get your functionality
Abstraction -- Creating objects with simple logical interfaces that represent your item
Inheritance -- The ability to bring in methods from a single parent class
Polymorphism -- Methods of the same name on different objects, creating the ability to build dynamically
```

### Self Assessment:
Choose One: (erase the others)

* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:

* I feel overwhelmed by the content presented this week

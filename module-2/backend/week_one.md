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
    Sinatra is a web application framework that uses a domain specific language.  Sinatra responds to HTTP requests and aids in the development of web applications.
    ```

3. What is MVC?

    ```
    MVC is a design pattern which separates or silos where our logic lives.  It stands for Model, Controller, View, where the model holds the data logic, the controller holds the app/business logic, and the view holds the presentation logic.

    More generally, MVC models/simulates/prototypes user interaction with our web applications.
    ```

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?

  ```
  I believe we follow the MVC design pattern and conventions when using Sinatra because they will be required when moving up to Rails.
  More generally,
  ```

5. What types of variables are accessible in our view templates without explicitly passing them?

  ```
  ```

6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    erb :index
  end
  ```

  ```
  ```

7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

  ```
  ```

8. What's the purpose of ERB?

  ```
  ```

9. Why do I need a development AND test database?

    ```
    ```

10. What is CRUD and why is it important?

  ```
  ```

11. What does HTTP stand for?

  ```
  Hyper Text T Protocol
  ```

12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?

  ```
  ```

13. What's an ORM? What does it do?
    ```
    Object Relational Mapper, it stands in between the model and the database and translates commands between your model and database languages
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
    A migration populates a table based on that table's specific instructions/blueprint
    ```
17. When you create a migration, does it automatically modify your database?
    ```
    Yes
    ```
18. How does a model relate to a database?
    ```
    A model dictates how table objects are created?
    ```
19. What is the difference between `#new` and `#create`?
    ```
    new will only intialize a new instance of the table object, while create will both initialize a new instance of the table object AND save it to the table
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
  ```

24. What are the 4 Principles of OOP? Give a one sentence explanation of each.

  ```
  ```

### Self Assessment:
Choose One: (erase the others)

* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:

* I feel overwhelmed by the content presented this week

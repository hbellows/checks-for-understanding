## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
```
ActiveRecord is an ORM (Object-Relational-Mapping). It communicates with our database and turns queries into SQL statements. It also allows us to interact with objects in our database as if they are regular Ruby objects.
```
2. Assume you have the following model:
```ruby
class Team < ActiveRecord::Base
end
```
What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
```
Team.all, Team.find, Team.find_by, Team.where - These are inherited from ActiveRecord
```
3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
```
team = Team.find(4)
Owner.find_by(team: team)
```
4. Assume that you added a line to your `Team` class as follows:
```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```
Now how would you find the owner of the team with an id of 4?
```
Team.find(4).owner
```
5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
```
Students Table
ID
Name
Teachers Table
ID
Name
Student_Teachers Table
ID
Student_ID
Teacher_ID
```
6. Define foreign key, primary key, and schema.
```
Foreign key = used to link two tables together
Primary key = how each record is uniquely identified in the database
Schema = a map of the tables in the database
```
7. Describe the relationship between a foreign key on one table and a primary key on another table.
```
The foreign key references the primary key of another table
```
8. What are the parts of an HTTP response?
```
status
header(s)
body

Protocol/Version, Status Code, and its Description - the very first line of a valid HTTP Response is consists of the protocol name, it's version, status code of the request, and a short description of the status code.

HTTP Response Headers - HTTP Response Headers contain information about the environment of the server machine (HTTP Request Headers contain information about the environment of the client machine).

HTTP Response Body - this the actual response which is rendered in the client window (the browser window). The content of the body will be HTML code.
```

### Optional Questions
1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
```
find = returns record by ID
find_by = returns first record that matches criteria
where = returns all records that match criteria
sum = adds all information that match criteria
joins = joins a table based on matching criteria
```
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
```
rake db:migrate = takes the migrations and creates a database based on them
rake db:setup = db:create, db:schema:load, db:seed all at once
rake db:reset = db:drop db:setup
```
3. What two columns does `t.timestamps null: false` create in our database?
```
created_at and updated_at
```
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
```
A teacher belongs to a school and a school has many teachers
```
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
```
Schools Table
ID
Name

Teachers Table
ID
Name
School_ID
```
6. Give an example of when you might want to store information besides ids on a join table.
```
A student might have many classes and the grades for each of those classes could be stored on a join table.
```
7. Describe and diagram the relationship between patients and doctors.
```
A patient has many doctors and a doctor has many patients

Patients Table
ID
Name

Doctors Table
ID
Name

Patient_Doctors Table
ID
Patient_ID
Doctor_ID
```
8. Describe and diagram the relationship between museums and original_paintings.
```
A museum has many original_paintings and a original_painting belongs to a museum.
Museums Table
ID
Name

Original_Paintingss Table
ID
Name
Museum_ID
```
9. What could you see in your code that would make you think you might want to create a partial?
```
Repetitive information
```

### Self Assessment:
Choose One:

* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:

* I feel comfortable with the content presented this week

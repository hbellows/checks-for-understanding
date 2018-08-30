## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
```
rails new
```
2. What do Models generally inherit from in rails?
```
Action pack (Application Controller, Application Record)?
```
3. What do Controllers generally inherit from in a rails project?
```
```
4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
```
resources :horses, only: [:show]
```
5. What rake task is useful when looking at routes, and what information does it give you?
```
rails routes - all the available routes
```
6. What is an example of a route helper? When would you use them?
```
link_to "Link Name", things_path - When wouldn't you use them?
```
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
```
No clue
```
8. What are strong params and why are they necessary?
```
strong params hide important information from the rest of the program, and from users; the keep unwanted information out, and sensitive information in.
```
9. What role does `form_for` play in helping us create our forms?
```
automated form templates so we don't have to write as much html
```
10. How does `form_for` know where to submit the user's input?
```
Voodoo
```
11. Create a form using a `form_for` helper to create a new `Horse`.
```

form_for @horse do |f|
  f.label :name
  f.text_field :name
  f.submit
end
```
12. Why do we want to validate our models?
```
to make sure necessary information is reaching our model
```
13. What are the steps of the DNS lookup?
```
```

### Review Questions
14. Within a feature test and given the following HTML, write the code necessary to target the following section and check the person's name?

  `<section id="personal-info">
    <h3><%= @person.name%></h3>
   </section>
  `

```
```
15. How would you call the method `prance` from within the method `move` on a `Horse` instance?
```
?
```
16. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?
```
furniture[:table][:height] vs furniture[:purchased]
```
17. What is inheritance?
```
```

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

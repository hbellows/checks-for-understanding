### Week 5 Questions

Re-pull from this repository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
```
In the controller:
flash[:notice] = "message"
In the application.html:
<% flash.each do |type, message| %>
  <%= content_tag :div, message, class: type %>
<% end %>

```
2. Where is cart information/temporary information usually stored?
```
Temporary information is stored in a session.
```
3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
```
It would require multiple updates/deletions while someone makes up their mind about what they want to buy, resulting in extra database work.
```
4. What is the purpose of the asset pipeline?
```
Concatenating/Minifying: Makes the assets we serve more compact.
Precompiling: Allows us to write in languages related to CSS/JavaScript.
Fingerprinting: Provides a means to invalidate cached assets
```
5. Why do we precompile our assets?
```
The browser only understands 3 languages: HTML, CSS and Javascript.  Some would prefer to write in a different, or simplified languages (eg, coffescript for javascript, sass for css).  Precompiling translates these languages back to their base or root languages, those the browser understands.
```
6. What do each of the following tags do?
```ruby
<%= stylesheet_link_tag "application" %> => Creates a link to app/assets/stylesheet - It embeds a call to the CSS stylesheet
<%= javascript_include_tag "application" %> => Creates an HTML script tag for the specified source
<%= image_tag "rails.png" %> => Creates a link to app/assets/images - It embeds a link to an image in the HTML file
```
7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
```
A good readme includes good descriptions of the what is meant to do, how to use/install the app, it posts screen shots and code snippets so users feel confident installing/using your application.  It provides good, usable guidance for users of all levels.  A good readme is important because you want people to actually use your app.
```
8. What are the top four accessibility issues that we as developers should be aware of?
```
Visual impairment (important features are both color coded and labeled, images, tabs, links have good descriptions readable by screen readers)
Hearing impairment (important information that is prompted by a sound also shows a label or message, videos are captioned)
Cognitive impairment (animations can be distracting or anxiety inducing for some with cognitive impairments so there be a link or an ability to disable them.)
Physical impairment (websites navigable by a keyboard, or keyboard assist like a joystick)
```
9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
```
before_save is an example of a callback.  This particular callback would appear in the model.
```
10. Given the following object, how would we create a scope for all users who are active?
```ruby
User.create(name: "Happy", active: true)
```
```
scope :active, -> true
User.active (?)
```
11. What is the difference between a scope and a class method?
```
They are almost the same, but scope, because of it's flexibility can handle edge cases better than class methods.  With a class method, you'd have write an elsif to handle a nil entry, or an empty string entry, where with a scope this can be handled by chaining scopes together. Class methods are great if your logic outgrows scope methods (chaining too many scope methods together is a good sign you need a more robust method.)(?)
```

### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

12a. How would you add item with id of 48 with a quantity of 4?  
```
hash[:cart][:48] = 4
```
12b. How would you increase the quantity of item 29?
```
hash[:cart][:29] += num
```
12c. How would you find out how many items your user is thinking about purchasing?  
```
hash[:cart].values.sum
```
13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?
```
Polymorphism is the ability to the same method in many different places, on many different objects.  For ruby, this might be the ability to use #each on an array and a hash, or #length to count the number of elements in an array or the number of characters in a string.

In Ruby, duck typing usually defines that concept that programmers treat an object for what it does rather than what it is (what class/module it might inherit from).
```
14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
```
```

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week

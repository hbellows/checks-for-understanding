## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
```
A cookie is a common technique for implementing sessions in Rails.  A cookie is a small pieces of text placed on the user’s browser. Because cookies persist from one page to the next, they can store information (such as a user id) that can be used by the application to retrieve the logged-in user from the database.

```
2. What’s the difference between a session and a cookie?
```
HTTP is a stateless protocol, treating each request as an independent transaction which makes it unable to use information from any previous requests. This means there is no way within the Hypertext Transfer Protocol to remember a user’s identity from page to page; instead, web applications requiring user login must use a session, which is a semi-permanent connection between two computers.  A cookie, then, is the means by which we mimic state.

They are similar but not the same. Session is an entire hash that gets put in the secure session cookie that expires when the user closes the browser. The “expiration” of that cookie is a “session”. Each value in the cookies hash gets stored as an individual cookie.
```
3. What’s a flash and when do you want to use flashes?
```
Flash is a special hash that persists only from one request to the next. It is sort of like a session hash that self destructs after it’s opened. It’s commonly used to send messages from the controller to the view so the user can see success and failure messages after submitting forms.
```
4. Why do people say “HTTP is stateless”?
```
HTTP is a stateless protocol, treating each request as an independent transaction which makes it unable to use information from any previous requests.
```
5. What’s authentication? Explain.
```
Most applications require a user to sign up. As a user, you can sign up for a service, log in, and log out when you're done.
```
6. What’s the difference between authentication and authorization?
```
Authentication is the process of determining whether someone or something is, in fact, who or what it is declared to be. In private and public computer networks (including the Internet), authentication is commonly done through the use of logon passwords.

Authorization is the function of specifying access rights to resources, which is related to information security and computer security in general and to access control in particular.
```
7. What’s a before filter?
```
It is used to run some code in your controller at very specific times, for instance before any other code has been run. For instance, if a user is requesting to run an action they haven’t been authorized for, then the filter can send back the appropriate error/redirect before they’re able to do anything else. It basically filters out unauthorized requests.

The before_action method takes the symbol of the method to run before anything else gets run in the controller. If it returns false or nil, the request will not succeed.
```
8. How do we keep track of a user once they’ve logged in?
```
sessions and cookies
```
9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
```
Namespacing a route in Rails does three things:

-Allows us to put the controller for a resource into a directory inside of our controllers directory.
-Changes the route that a user would visit.
-Changes the prefix that we would use as a path helper.

Nesting a route allows to relate resources that have a natural parent/child relationship.

Nested routes allow us to capture relationships in our routing, while namespacing routes allow us to organize groups of controllers under a namespace (for our purposes, we group administrative controllers under Admin::namespace)
```
10. At a high level, what tools can you use to implement authorization? How would you use them?
```
At a high level, authorization requires:
-attributes for roles, typically in a User model
-access rules added to controller actions, restricting access to prohibited pages
-methods to check roles in view templates, displaying content conditionally
```
11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
```
Your database needs an integer column.  We would declare the enum in the model.
```
12. What are some strategies you can use to keep your views DRY?
```
We can use partial forms.
```

### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  
```
array.map do |hash|
  hash[:holiday][:name]
end.sort
```
14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?
```
number = "$300"
number.gsub(/[^\d\.-]/,'').to_i

<!-- note to self: the - at the end of the regex preserves negative numbers:
number = "-$300.50"
number.gsub(/[^\d\.-]/,'').to_i = -300 -->
```
### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week

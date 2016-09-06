## Week Three Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What are the 3 main features in an ERD?
```
Entities: Objects that we store the information about.
Relationships: The way each entities are linked to one another
Cardinalities: An attribute of each relationship, can either be "One to One", "One to Many", or "Many to Many"
```
2. Create an ERD for the following database: Restaurants, Customers, Items, Ingredients, Beverages, Orders, Vendors.
```

```
3. What is the entry at the command line to create a new rails app?
```
rails new app_name
```
4. What do Models generally inherit from in rails?
```
Models inherit from ActiveRecord::Base
```
5. What do Controllers generally inherit from in a rails project?
```
Controllers inherit from ActionController::Base
```
6. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
```
resources :horses, only [:show]
```
7. What rake task is useful when looking at routes, and what information does it give you?
```
'rake routes' prints the list of routes that have been defined in the project's routes file.
```
8. What is an example of a route helper? When would you use them?
```
horses_path is equivalent to '/horses' and horse_path(id) is the same as '/horses/:id'
Route helpers are useful because often times we do not know the exact url or pathname that we want to access, whereas that information is dynamically accessible through the route helper.
```
9. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
```
_url refers to the entire url address including the domain, whereas the _path refers to everything after the domain
```
10. What are strong params and why are the necessary?
```
strong params are a way to explicitly require only specific params. They are necessary because a user might inject a parameter of their own into a POST/PUT request where we do not want there to be one, and we do not want a chance that our code will be affected by that injected parameter. By specifying only the params we expect to come back to us, we keep the application safe from such vulnerabilities.
```
11. What role does `form_for` play in helping us create our forms?
```
form_for(Object) is an easy way to create a form that fills in attributes for a particular object.
```

12. How does `form_for` know where to submit the user's input?
```
The controller is responsible for handling the user's input from a "form_for", likely in a POST/PUT method.
```
13. Create a form using a `form_for` helper to create a new `Horse`. 
```
<%= form_for(Horse.new) do |f| %>

  <%= f.label :name %>
  <%= f.text_field :name %>
  
  <%= f.submit %>
<% end %>
```
14. Why do we want to validate our models?
```
We want to validate our models because this is the lowest-level at which we can force the submitted data to be correct. For example, we don't want to create a new Artist without a name because that would not make sense to us, so we validate this at the Model level such that a new artist can never be created without the name field filled out.
```

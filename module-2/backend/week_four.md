## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?
```
A cookie is an object that is saved on the user's browser that a server can interact with. It saves information about the user so that when they return, they don't have to fill it in again. It allows for http with 'state'.
```
* What’s the difference between a session and a cookie?
```
A session is like an ecrypted cookie. A user can still see it, but they cannot easily edit it, whereas with a cookie they can edit the values and even add their own parameters.
```
* What’s a flash and when do you want to use flashes?
```
A flash is a message that stays with the User's browser for one more request, presented and then deleted. It is useful for displaying error messages on the refreshed page, for instance when they did not fill out a form correctly.
```
* Why do people say “HTTP is stateless”?
```
HTTP is stateless means that requests are independent of one another and don't hold any information between each other.
```
* What’s authentication? Explain.
```
Authentication is the process of verifying that the user is who they say they are.
```
* What’s the difference between authentication and authorization?
```
Authorization is the gaining access of resources based on the identity. Authentication is necessary for authorization because if we want to allow certain users to see certain items, we need to first verify that the person on the other end is a user that we know of. Authentication is the verification that they are a user. Authorization is granting them permissions based on their identity.
```
* What’s a before filter?
```
A before_filter in rails is an action that must be performed before any action on that controller is allowed to be executed. Usually for admin controller actions, we should set a before_filter to verify that the current user is an admin or something along those lines.
```
* How do we keep track of a user once they’ve logged in?
```
We use a session controller and create new sessions for users to keep track of them once they've logged in.
```
* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
```
Namespacing a resource is appropriate for when we don't have the parent object as an entity in the database. For example in 'admin/categories', 'admin' is not a database object so it does not need to be crudded. However, when both resources are database objects, nesting the resources allows for full crud control of both resources. 
```
* At a high level, what tools can you use to implement authorization? How would you use them?
```
Authorization can be implemented with tools like OAuth or OmniAuth.
```
* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
```
An enum is a collection of strings that represent integer values in the database. Enums are declared in the model.
```
* What are some strategies you can use to keep your views DRY?
```
Partials and helpers can help keep views dry. A good place for a partial is the new/edit form for resources. It is usually very similar, so this can be 'partialled out' and referenced in both new/edit. A helper is like a bit of logic for methods. Sometimes we want to display something a certain way, in the view we would called the helper_method(thing_to_display) instead of formatting it in the view itself.
```

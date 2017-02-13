## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?
** rails new project_name --optional-flags version **
2. What do Models generally inherit from in rails?
**ApplicationRecord **
3. What do Controllers generally inherit from in a rails project?
**ApplicationController**
4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
** resources :horses, only: [:show] **
5. What rake task is useful when looking at routes, and what information does it give you?
** Rake routes shows you a list of the all of the routes available in your application. You can also narrow it be resource.**
6. What is an example of a route helper? When would you use them?
** The route helpers look like (for resources: :horses) horses_path, horse_path(horse), etc. They're useful shortcuts that I can use anywhere I would normally write out the route, like in a redirect or a link. **
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
** Path is for the view, and is relative to its current location. URL is an aboslute location. **
8. What are strong params and why are the necessary?
** Strong params are for permitting only the allowed params through an input hash. This is necessary so that someone can't inject params into your hash that are potentially malicious. **
9. What role does `form_for` play in helping us create our forms?
** Form_for sets up the form for a specific object (or objects, if there's a dependency). **
10. How does `form_for` know where to submit the user's input?
** Form_for submits the input via the create function for the object it is set up for, which is why it is passed the object on the first line. **
11. Create a form using a `form_for` helper to create a new `Horse`. 
```
form_for @horse do |f|

f.label :name, "Name"
f.text_field :name

f.submit
end
```
12. Why do we want to validate our models?
Validating models ensures data integrity in your database, and on the model level, they are database agnostic.

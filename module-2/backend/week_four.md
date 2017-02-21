## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?
A cookie is a small piece of data issued by the server and stored by the client.
* What’s the difference between a session and a cookie?
A session stores information on the server instead of the client-side.
* What’s a flash and when do you want to use flashes?
A flash is a type of cookie that lasts for one action. They are generally used to display messages, like errors and successes.
* Why do people say “HTTP is stateless”?
HTTP doesn't maintain state over multiple requests. It uses cookies, sessions, and flash to work around this.
* What’s authentication? Explain.
Authentication is the process of proving someone is who they say they are.
* What’s the difference between authentication and authorization?
Authentication is: are you who you say you are? Authorization is: what do you have access to?
* What’s a before filter?
A before filter allows us to set up actions that happen before certain other actions.
* How do we keep track of a user once they’ve logged in?
We use the session to track the user_id.
* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
Nesting a resource works when it is owned by the outer resource, another object. Namespacing changes the url, but doesn't require that the inner resource rely on another resource or object.
* At a high level, what tools can you use to implement authorization? How would you use them?
I use a before filter to check that a user is logged in, scoping to ensure that user can only view items that belong to them, and session to track the current user.
* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum? 
Enum allows us to assign strings to integers. I think it helps us convey more meaning, as well as prevent us from errors caused by forgetting what our integers represent. I think they're defined in the model.
* What are some strategies you can use to keep your views DRY?
Partials!

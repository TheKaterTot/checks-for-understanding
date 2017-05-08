## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's the most useful thing you learned from completing the intermission week work?
  ***Because of my previous experience with Javascript, I found the intermission work fairly simple, but really helpful to cement the basics.***

2. What are some tools to help debug JavaScript code?
  ***I like to use debugger and console.log (I used .dir a lot when writing my personal project). I've found that's usually enough to help me find my bugs. I know there is a Pry.js, but I haven't tried it yet.***
  
3. What are some tools you need in order to unit test your JavaScript?
  ***You need a testing framework, and depending on that framework, an assertion library. For my personal project, I used mocha and expect, but I'm learning to use chai now.***
  
4. What is the syntax for invoking a function?
  ***myFunction()***
  
5. What's the difference between `==` and `===` in JavaScript?
  ***The double is a soft equal, so 3 == '3'. The triple is an exact equal, which requires the elements (if not numbers) to be the exact same object.***
  
6. What's the difference between asynchronous and synchronous JavaScript? 
  ***Synchronous JavaScript generally happens in the order it is written. Asynchronous JavaScript is dependent on future events that may or may not happen to trigger the code.***
  
7. What's a callback function and what are some reasons when we use/need callback functions?
  ***Callback functions are one way that JavaScript handles its asynchronous code. They often dictate what happens when the original function is done and what it should return.***
  
8. What's the biggest difference between a promise and a callback?
  ***While both rely on future events, promises impose order on normally asynchronous behavior.***

9. How do we setup a route when creating an API with Node and Express?
  ***
  `
  app.get('/', function(req, res) {
    console.log('meh');
  }
  `
  ***
  
10. What's `npm` and what do we use it for?
  ***npm stands for node package manager. We use it to install and manage node modules in our projects. ***

#### Review  
11. What's the MVC design pattern? Describe each part of MVC?
  *** MVC is the model view controller architecture. The view controls what is sent to the client, the controller houses the actions that the views require to render, and the models establish the behavior of those actions.***
12. What is AJAX? What are some benefits of using AJAX?
  ***Asynchronous JavaScript and XML is beneficial for making request between the client and the server. ***
13. What's a background worker? When would we want to use a background worker?
  ***Background workers are used to basically say, do this task later. They're often used for tasks that take a long time.***

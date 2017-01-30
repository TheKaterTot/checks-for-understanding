## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.
The five common verbs: 
  ** 1. Get ** Get's purpose is to receive information.
  ** 2. Post ** Post's purpose is to send information.
  ** 3. Put ** Put's purpose is to update information.
  ** 4. Delete ** Delete's purpose is to delete information.
  ** 5. Head ** Head returns just the header, which I imagine is useful for something I haven't encountered yet.
2. What is Sinatra?
  * Sinatra is a DSL alternative to Rails that allows me to run a web app. It uses Rack to help communicate with the server.*
4. What is MVC?
  *MVC is: Model View Controller. This is the architecture for web apps.*
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  * Using REST makes the code readable to everyone, even if they're new to the project. It makes the code logical to everyone
  * familiar with the conventions. *
6. What types of variables are accessible in our view templates without explicitly passing them?
  *The view templates can access local and instance variables.*
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    erb :index
  end
  ```
  ***
  ```ruby
    get '/horses' do
      @count = 1
      erb :index
    end
    ```
    ***
8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
    ```ruby
    get '/horses' do
      erb :index, locals: {name: "Mr. Ed"}
    end
    ```
9. What's the purpose of ERB?
  *To have access to ruby to render dynamic views. *
10. Why do I need a development AND test database?
  *The test database should be clean so that tests run without data that may have been entered during development. *
11. What's responsive design?
  *It's design that works for both desktop and mobile because the screen size is flexible. It responds to the screen size changing. *
12. What is CRUD and why is it important?
  * CRUD (Create, Read, Update, Delete) is the foundation for web development. It provides the basic functionality needed for
  a web app. *
13. What does HTTP stand for? 
  *Hyper Text Transfer Protocol*
14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  * 1: <%= test %> 2. <% test %> *
  * Use 1 when you want to render the Ruby. Use 2 when you want to evaluate it, but not render.*
15. What's an ORM?
  * Object Relational Mapping --ActiveRecord is an ORM. *
16. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  * ActiveRecord *
17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  *
    ```ruby
      get '/restaraunts' do
        @restaurants = Restaurant.all
        erb :index
      end
      ^^ This renders the index page
      
      get '/restaurants/:id' do
        @restaurant = Restaurant.find(params[:id])
        erb :show
      end
      ^^ This renders an individual restaurant page.
      
      get '/restaurants/new' do
        erb :new
      end
      ^^ This renders a page where a user can add a new restaurant.
      
      post '/restaurants' do
        Restaurant.create(params[:restaraunt]
        redirect '/restaurant'
      end
      ^^ This submits the new info from the form and posts it to /restaurants to be persisted.
      
      get '/restaurants/:id/edit' do
        erb :edit
      end
      ^^ Shows the update page for a restaurant.
      
      post '/restaurants/:id' do
        Restaurant.update(params[:restaurant])
        
        redirect '/restaurant/:id' 
      end
      ^^ Submit the updated info from the form to be persisted.
      
      delete '/restaurants/:id' do
        Restaurant.destroy(params[:id])
        
        redirect '/restaurants'
      end
    ```
  *
18. What's a migration? 
  *A migration sets up the structure inside of a database with instruction to build tables. *
19. When you create a migration, does it automatically modify your database?
  * No. You have to run the migration after it's been created before it modifies the DB. *
20. How does a model relate to a database?
  * A model represents a table within a database. *
21. What's the difference between agile workflow and waterfall method?
  * Waterfall is setting a plan and sticking to it, despite changes that may derail that plan. Agile is meant
  to be flexible. It requires working in small steps and giving/getting feedback often so that the project is adjusted
  as necessary for deadlines, features, and other changes. *
22. What is the difference between `#new` and `#create`?
  * New creates a thing, but does not save Thing. Create is a combination of new and save, which means that Thing is persisted right away. *

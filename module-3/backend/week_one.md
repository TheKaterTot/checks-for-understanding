## Week One - Module 3 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

1. What kind of object is JSON in Ruby? How do we know it's JSON?
1. What's the difference between `joins` and `includes` in ActiveRecord?
1. What's an API?
1. How do we test an internal API (in general)?
1. What are two different ways to customize your `json`?
1. If the the methods below return collections, what object (class) will they return? What kind of objects will be returned inside of that object?
   * `.find_by_sql`
   * `.connection.execute`
   * `.where`
1. (Security) What is SQL injection? When can it happen? How can you prevent it?
1. What do you need to do differently when you adding `POST`, `PUT`, and `DELETE` endpoints to your API when using the `--api` flag when creating a Rails app versus not using the flag?
   * Hint: What class does `ApplicationController` inherit from when creating a Rails project with the `--api` flag? What about without the `--api` flag? What do they do differently? Why?
1. What's your process for solving advanced SQL or ActiveRecord lookups?
** JSON stands for Javascript Object Notation. It's important because it's one of the easiest ways to serve up data to the frontend and expose an internal API. **
2. What's the difference between `joins` and `includes` in ActiveRecord?
** Joins joins tables, but includes is used for eager loading, which is important to avoid multiple queries (n+1 queries). I've used incluces in the past to ensure an object's relationships were available in a view without having to make separate queries. **
3. What's an API?
** An API (application program interface) is a particular set of rules that that programs can follow to communicate with each other. It can be as simple as rendering JSON or as complex as the instructions that the microprocessors in the computer follow. **
4. How do we test an internal API (in general)?
** With request specs that test the body of the JSON response. **
5. What are two different ways to customize your `json`?  
** JBuilder and Serializer **

#### Review  
6. What is an ORM, what does it stand for, and why is it helpful?
** Object Relational Mapping. The ORM is helpful to map out the relationships and attributes of objects in a database. **
7. How do you create a record in the following table in SQL? In Active Record?   
   (Users table with columns first_name, last_name, email, and age)
   ** INSERT INTO users (first_name, last_name, email, age) VALUES ('katy', 'isgreat', 'katyisgreat@example.com', 400) **
8. Given an array numbers = [1,2,3,4,5], find the sum of the doubles of all the numbers.  
```
def doubler(num)
  num * 2
end

def find_total(nums)
  nums.reduce(0) do |total, num|
    total += doubler(num)
  end
end

answer = find_total([1, 2, 3, 4, 5])
#30
```

#### Self Assessment  
Rate yourself on the following scale.  
4  I know and understand all these concepts and did not have to look anything up  
3  I know and understand most of these concepts but had to look something up  
2  I am uncertain about some of these concepts and had to look some things up ^^  
1  I am feeling lost about with these concepts and had to look many things up ^^  
Rate yourself on the following scale.
**4. I know and understand all these concepts and did not have to look anything up  **
Even if I'm a little wrong, I wanted to try to not look anything up.
3. I know and understand most of these concepts but had to look something up  
2. I am uncertain about some of these concepts and had to look some things up *  
1. I am feeling lost about with these concepts and had to look many things up *  

^^ Please let an instructor know where you'd like support to catch you up. 

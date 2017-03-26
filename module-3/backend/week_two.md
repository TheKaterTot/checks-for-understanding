## Week Two - Module 3 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

1. What's OAuth?
2. What are some advantages/disadvantages of implementing OAuth?
3. How many exhanges of information need to take place before a user is authenticated with OAuth?
4. Why do we want to create services?
5. Why is it good practice to create PORO's with the data received from an API?
6. What do we use VCR for? Why is it a good idea to use this tool?  

#### Review  

7. What does HTTP stand for?  
8. How do you create the following table in SQL? In Active Record?   
   (Users table with columns first_name, last_name, email, and age)   
9. Writing Files: given a text file located at "/Documents/pizza.txt", write code to read the file from the filesystem, then    write a new file at "/Documents/line_count.txt" containing the number of lines in the original file.  

#### Self Assessment  
Rate yourself on the following scale.  
4 I know and understand all these concepts and did not have to look anything up  
3 I know and understand most of these concepts but had to look something up  
2 I am uncertain about some of these concepts and had to look some things up ^^  
1 I am feeling lost about with these concepts and had to look many things up ^^  

^^ Please let an instructor know where you'd like support to catch you up.



* What's OAuth?
** OAuth is one way for a user to authorize an app to access their information via a third party. **
* What are some advantages/disadvantages of implementing OAuth?
** One advantage is that part of the login process can be outsourced, and I don't have to necessarily implement Bcrypt or another password management system. One disadvantage is that I have less control of my users' information. **
* How many exhanges of information need to take place before a user is authenticated with OAuth?
** The client app makes a request to access data, which goes to an authorization server. The user approves the request, and the server issues an access token. So, like, 4? **
* Why do we want to create services?
** Services are a good way to follow the single responsibility principle. They handle services specifically so that models and POROs don't get muddled. **
* Why is it good practice to create PORO's with the data received from an API?
** I don't know if I know a good textbook answer for this, but I found it to be really helpful for clarification in my project. Having a PORO for different types of data received helped me organize and keep track of my data. **
* What do we use VCR for? Why is a good idea to use this tool?
** VCR allows us to avoid making a call to the API every time we run our tests. It makes a cassette that records a response from the API and replays it in the test suite. **

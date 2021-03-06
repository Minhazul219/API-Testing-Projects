
# API Testing

 What is an API? (Application Programming Interface)
 
   API is the acronym for Application Programming Interface, which is a software intermediary that allows two applications to talk to each other. Each time you use an app like Facebook, send an instant message, or check the weather on your phone, you’re using an API.



## What Is an Example of an API?

  When you use an application on your mobile phone, the application connects to the Internet and sends data to a server. The server then retrieves that data, interprets it, performs the necessary actions and sends it back to your phone. The application then interprets that data and presents you with the information you wanted in a readable way. This is what an API is - all of this happens via API.

To explain this better, let us take a familiar example.

Imagine you’re sitting at a table in a restaurant with a menu of choices to order from. The kitchen is the part of the “system” that will prepare your order. What is missing is the critical link to communicate your order to the kitchen and deliver your food back to your table. That’s where the waiter or API comes in. The waiter is the messenger – or API – that takes your request or order and tells the kitchen – the system – what to do. Then the waiter delivers the response back to you; in this case, it is the food.

Here is a real-life API example. You may be familiar with the process of searching flights online. Just like the restaurant, you have a variety of options to choose from, including different cities, departure and return dates, and more. Let us imagine that you’re booking you are flight on an airline website. You choose a departure city and date, a return city and date, cabin class, as well as other variables. In order to book your flight, you interact with the airline’s website to access their database and see if any seats are available on those dates and what the costs might be.

However, what if you are not using the airline’s website––a channel that has direct access to the information? What if you are using an online travel service, such as Kayak or Expedia, which aggregates information from a number of airline databases?

The travel service, in this case, interacts with the airline’s API. The API is the interface that, like your helpful waiter, can be asked by that online travel service to get information from the airline’s database to book seats, baggage options, etc. The API then takes the airline’s response to your request and delivers it right back to the online travel service, which then shows you the most updated, relevant information.
## API Testing with Postman

Postman is an application used for API testing

### POSTMAN Request
There are mainly several types of postman request. But in here we are going to talk about some five kinds of request.

- Post-  New input request to the server.
- Put - Value Update request to the server.
- patch- One section modify request to server.
- Get- value generate request from server.

### Environment Setup

For set up an environment . You have to create a new environment and rename the environment. And you have to put some JS Script on the such environment.
As like for id set up in environment 

var jsonData = pm.response.json();

pm.environment.set("id", jsonData.bookingid)

### Permission Set Up

Why do we need permission in PostMan. We need permission to update/patch/delete values in API.

For permission , the developer will give you permission like {“Admin:admin”
                                                                                                 “Password:Password1234”}

Now open permission request with Get request and test script will be 

var jsonData=pm.response.json();
pm.environment.set("access", jsonData.token)
you will find token on the body. And set this token to environment.

### Querry Parameters
Query parameters are some additional data that we can submit with our request through API. Query parameters are optional.

## Newman 
1. Go to the folder where you export collection and environment
2. Click on folder location bar and type CMD
3. In CMD type: Newman run (collection name) -e (environment name) -r cli,htmlextra


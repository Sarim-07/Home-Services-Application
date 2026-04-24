                                    # Home-Services-Application
                        # Team
                   NAME            CMS                 
            Muhammad Talal Aqdas  547601
            Sarim Farooq Khan     542714
 
                                            #Introduction
We chose to create a home services application. As the name suggests, it will be an app in which services will be provided. You can either use a service or become a service provider yourself.

Finding reliable service providers for home problems like plumbing, electrical issues, or cleaning can be difficult. People often waste time searching online, asking friends, or calling random numbers. In urgent situations, it can be stressful to find someone trustworthy quickly.
This project aims to create a simple application in Java that helps customers find and book home services. The system provides a place where both customers and service providers can interact easily. Customers can see available services, book them, and check their past bookings. Service providers can see requests, accept or reject them, and manage their schedule.
                               
                                
                                             #Problem Statement
                              
Many people face problems when trying to get home services. They may not know which provider is reliable or available. Booking can take a lot of time and tracking previous services is often difficult. Service providers also face challenges managing multiple requests at the same time. People in need either have to ask friends, family members, neighbors and more when in need of a service. Many often text paragraphs to explain their requirements for a service in WhatsApp groups or post on social media.
Similarly, service providers find it difficult to advertise their services.
This project aims to make booking home services faster and easier, while also giving providers a way to manage requests efficiently.

Apart from solving a real-life problem, this project is also a way to practice the object-oriented programming concepts we have learned in class. Concepts like inheritance, encapsulation, polymorphism, and abstraction will be applied while building this system.

                                  #Features

      #Customer side

1.You can register as a customer with your name, email, password, phone number and home address.

2.Then you log in. It takes you to your own personal dashboard.

3.The first thing you see is an overview screen that shows your bookings and some stats.

4.You can look through. Book from eight different services that are divided into four categories.

5.When you book something you get to pick a date and time that works for you.

6.You can see all your bookings. What is happening with them. If they are pending, accepted, rejected or cancelled.

7.You will get a notification on your app when a service provider says yes or no to your request.

8.After a job is done you can give the provider a rating.

9.You can also change your profile information like your name, phone number and address.

10.When you are all done you can log out.


                            #Service Provider side

1.You can sign up to be a provider and choose what kind of work you want to do.

2.Your dashboard will show you how jobs you have and how many requests are waiting for you.

3.You can look at all the requests that are waiting for you and decide which ones you want to accept or reject.

4.You can see every booking you have ever had.

5.You can also see how stars you have on average and how many reviews you have gotten.

6.You can change your profile if you need to.

7.When you are finished you can log out.

                   #Admin side

1.The admin dashboard is separate. It Opens in a new window.

2.The first screen you see has some numbers, a bar chart that shows how many bookings there are for each category and a circle chart that shows what is happening with all the bookings.

3,You can see a list of all the customers. Delete their accounts if you need to.

4.You can see a list of all the providers and suspend or unsuspend them.

5.You can see every booking and cancel any of them if you have to.

6.There is also a screen, for analytics that has a bar chart showing how much money is being made from each service category and a chart showing which providers are doing the best.

                               #OOP Concepts Applied
                               
       Concept                     Where It's Used
       
     1.  Abstraction          User is an abstract class — you can't instantiate it directly, 
                              only Customer, ServiceProvider, and Admin
                              
     2.  Inheritance          Customer, ServiceProvider, and Admin all extend User and inherit 
                              common fields like name, email, and password
                              
     3.  Polymorphism         db.login() returns a User reference that could be a Customer, ServiceProvider,
                              or Admin — the correct dashboard is shown based on the actual type
     
     4.  Encapsulation        All fields across every class are private with controlled access through
                              getters and setters
     
     5. Singleton             PatternDataStore and NotificationManager use the Singleton pattern. only one 
                              instance exists throughout the app
     
    6. Observer Pattern       NotificationManager uses a BadgeListener interface to update notification badges
                              in real time across the UI
                              
    7. Composition            Customer contains a list of Booking objects; ServiceProvider contains lists of Booking
                              and Service objects
                              

       

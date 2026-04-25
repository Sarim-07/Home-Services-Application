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
                              

                                               ## How to Run

You need two things. Java JDK 17 and IntelliJ IDEA.

1. Clone the repo or just download it as a zip and open it in IntelliJ.
2. Once it loads go to src then homeservicessystem then find MainGUI.java
3. Right click it and hit Run.

The app will start with a splash screen and then bring you to the login page. From there you can log in as a customer, service provider or admin. You can also register a new account if you want.

If you want to test things quickly here are some accounts that are already in the system.

#ADMIN
Email: admin@home.com  Password: admin123
Email: support@home.com  Password: support123

#CUSTOMERS
Email: ahmed@gmail.com  Password: 1234
Email: sara@gmail.com  Password: 1234
Email: bilal@gmail.com  Password: 1234

#SERVICE PROVIDERS
Email: usman@pro.com  Password: 1234
Email: ali@pro.com  Password: 1234
Email: clean@pro.com  Password: 1234
Email: coolair@pro.com  Password: 1234

           # Code Explanation

**How the App Starts**

When you run the app, SplashScreen is the first thing that shows up. It shows the name of our Project: “Home Services Management System”. It also mentions our names and our CMS IDs along with the name of our instructor. This splashscreen lasts for about 3-5 seconds.
  After that MainGUI takes over. MainGUI is basically the backbone of the whole application. It handles everything from login and registration to building the right dashboard for whoever logged in.



**How Login Works**

Login uses polymorphism. The login() method in DataStore returns a User object. But User is an abstract class so it can never be just a "User". The actual object coming back is always either a Customer, ServiceProvider or Admin. MainGUI checks which one it is and then shows that person their correct dashboard. This is polymorphism in action.


**How Data is Managed**

Everything goes through DataStore. It is a Singleton which means only one instance of it exists throughout the entire app. No matter which screen you are on, everyone is reading from and writing to the same DataStore. It keeps all the customers, providers, bookings and services in memory.
DataPersistence works alongside DataStore. Every time something changes, it saves automatically. When you open the app again it loads everything back so nothing is lost.

**How the Customer Side Works**

After logging in as a customer you land on your dashboard. From there you can browse 8 services across 4 categories. When you book something you pick a date and time. That booking gets stored in DataStore and also saved to disk through DataPersistence. You can track your bookings and see if they are Pending, Accepted, Rejected or Completed.

**How the Service Provider Side Works**

The provider logs in and sees their own dashboard. All incoming booking requests show up there. They can accept or reject each one. The moment they do that, the customer gets a notification.

**How Notifications Work**

NotificationManager handles all notifications. It uses the Observer Pattern with a BadgeListener interface. This means whenever something changes, like a booking getting accepted, the notification badge on the UI updates instantly in real time. You do not have to refresh anything. The UI is always listening.

**How the Admin Side Works**

The Admin dashboard opens as a completely separate window. From there the admin can see every single user and every booking in the system. They can delete customer accounts, suspend or unsuspend providers and cancel any booking. There are also two charts. One shows bookings per category and the other shows revenue per category.


   # Tools and Technologies Used

Language: We built the entire application in Java. No other language was used anywhere 
in the project.

IDE: We used IntelliJ IDEA for writing, running and debugging the code.

UI Framework: For the graphical interface we used Java Swing and Java AWT. Both of these 
come built into Java so we did not need to install anything extra. Swing handled the components like buttons, panels, tables and cards. AWT handled the layouts, colors and event listeners.


Data Storage: We did not use any external database. Instead we used file-based storage 
through our DataPersistence class which saves and loads data locally on 
your machine.

Version Control: We used Git and GitHub to manage our code throughout the project. 

UML Diagrams: After completing the code we created UML class diagrams using IntelliJ for every class in the system to document the structure of the project and show how all the 
classes connect to each other.




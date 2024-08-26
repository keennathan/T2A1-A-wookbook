# Q1 Describe the architecture of a typical API project, such as a Flask application.
## Model View Controller Architecture
Software architecture is a way that we can describe software systematically and also refers to how different software interact with each other.  One of the most popular Software architectures is Model-View-Controller(MVC).  
<br>  
MVCs' design patern divides any application into three interconnected components, allowing for effecient code organisation, easier maintenance and scalability. 

*MVC Architecture Diagram*  
![MVC Architecture Diagram](docs/MVC-diagram.png)
### The Model  
The Model component is resposible for managing the application's data related logic, such as the schemas and interfaces of the project.  It interacts with the database to define the data structure and retrieves, manipulate and store data.  It acts as a middleman between the database and the controller.

### The View
The View component handles the presentation part of the application with things that the user can interact with, such as text boxes, dropdowns etc.  Its primary role is to displays the data, and sends all the inputs from the user to the Controller component.  

### The Controller  
The controller component acts as the go-between for the Model and View components.  It handles and processes the user inputs then determines what data from the *model* will be displayed in the *View*.  

### Benifits of MVC
The benefits of this architecture is that it separates each component making it easier to maintain and organise code by setting clear responsibilties for each.  By separating each part, it can be developed,scaled, and tested independently.  

### References 
* https://www.youtube.com/watch?v=DUg2SWWK18I 
* https://www.freecodecamp.org/news/model-view-architecture/
* https://www.geeksforgeeks.org/mvc-design-pattern/
* https://www.guru99.com/mvc-tutorial.html

# Q2 Identify a database commonly used in an API project (such as a Flask application) and discuss the pros and cons of this database.



# Q3 Discuss an implementation of an Agile project management methodology for an API project.


# Q4 Provide an overview and description of a standard source control process for an API project.



# Q5 Provide an overview and description of a standard testing process for an API project.


# Q6 Explain the three principles of information system security.



# Q7 Provide an overview of what would need to be done within an API project to implement at least one of the principles explained in Question 6.



# Q8 Explain the legal obligations that developers of a social media website or social media application would have in regards to handling user data, with reference to any applicable laws or acts.



# Q9 Describe the structural aspects of the relational database model. Your description should include information about the structure in which data is stored and how relations are represented in that structure.



# Q10 Describe the integrity aspects of the relational database model. Your description should include information about the types of data integrity and how they can be enforced in a relational database.



# Q11 Describe the manipulative aspects of the relational database model. Your description should include information about the ways in which data is manipulated (added, removed, changed, and retrieved) in a relational database.



# Q12 Conduct research into a web application (app) and answer each of the following sub-questions:

- List and describe the software (tech stack) used by the app. 
- Describe or make educated guesses about the hardware used to host the app.
- Describe the interaction of technologies within the app.
- Describe the way data is structured within the app’s database(s).
- Identify the entities/tables that are tracked within the app’s database(s).
- Identify the relationships and associations between the entities/tables identified in sub-question E.
- Design an entity relationship diagram (ERD) based on the answers provided to sub-questions E and F. This must represent a relational database model, even if the app itself uses something other than a relational database model.
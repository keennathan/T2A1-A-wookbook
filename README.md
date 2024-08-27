# Q1 Describe the architecture of a typical API project, such as a Flask application.
## Model View Controller Architecture
Software architecture is a way that we can describe software systematically and also refers to how different software interact with each other.  One of the most popular Software architectures is Model-View-Controller(MVC).  
<br>  
MVCs' design patern divides any application into three interconnected components, allowing for effecient code organisation, easier maintenance and scalability. 

*MVC Architecture Diagram*  
![MVC Architecture Diagram](docs/MVC-diagram.png)
### The Model  
The Model component is resposible for managing the application's data related logic, such as the schema's and interfaces of the project.  It interacts with the database to define the data structure and retrieves, manipulate and store data.  It acts as a middleman between the database and the controller.

### The View
The View component handles the presentation part of the application with things that the user can interact with, such as text boxes, dropdowns etc.  Its primary role is to displays the data, and sends all the inputs from the user to the Controller component.  

### The Controller  
The controller component acts as the go-between for the Model and View components.  It handles and processes the user inputs then determines what data from the *model* will be displayed in the *View*.  

### Benifits of MVC
The benefits of this architecture is that it separates each component making it easier to maintain and organise code by setting clear responsibilties for each.  By separating each part, it can be developed, scaled, and tested independently.  

### References 
* https://www.youtube.com/watch?v=DUg2SWWK18I 
* https://www.freecodecamp.org/news/model-view-architecture/
* https://www.geeksforgeeks.org/mvc-design-pattern/
* https://www.guru99.com/mvc-tutorial.html

# Q2 Identify a database commonly used in an API project (such as a Flask application) and discuss the pros and cons of this database.

## PostgreSQL
PostgreSQL, while one of the oldest, is still one of the most advanced Relational Database Management Systems out there.  It is open source, meaning it is managed and maintained by a vibrant community of people and the source code is available to anyone under the PostgreSQL licence.  

### Pros 
1. *Transactions*:  
    - PostgreSQL supports transactional DDL(Data Definition Language), which allows for complex relational applications to make schema changes and other operations in a single transaction.  With this feature it reduces the need for extensive error handling code, which simplifies developement and enhances reliability.  

2. *ACID Compliance*: 
    - PostgreSQL is ACID (Atomicity, Consistency, Isolation, Durability) compliant. This means it ensures that transactions are reliable so your data remains secure and accurate.  

    ![ACID Diagram](docs/ACID.png)  

3. *Extensibility*:  
    - It is highle extensible, this allows developers to add custom functions, languages and data types.  This flexibility allows for a more tailored approach for specific needs when creating specilised or complex projects.  

4. *Security*:  
    - PostgreSQL offers powerful security features, including support for user priviledges and the ability to lock down enviroments at the OS level.  This makes it useful for applications that require a high level of security, such as those handling sensitive data.  

5. *Open Source and Community Support*:  
    - As an open-source database, PostgreSQL benefits from a vibrant community that actively maintains and supports it. This community-driven model ensures continuous improvement and quick resolution of issues.  

6. *Platform Compatibility*:  
    - PostgreSQL is compatible with various platforms, including Windows, Linux, and Mac. This cross-platform support makes it versatile for deployment in different environments.  

### Cons

1. *Database Structure*:  
    - PostgreSQL is predominantly a relational database, meaning it works with structured data in predefined schemas.  This can be limiting when dealing with unstructured or semi structured data, where as NoSQL databases like MongoDB might be more flexible.  

2. *Open Source Limitations*:
    - While open source is generally an advantage, it also means that PostgreSQL lacks the commercial support and warranties that come with branded software.  This can be a drawback for businesses that require guaranteed support or liability protection.  

3. *Slower Performance*:  
    - When handling very large datasets, particulary when there are complex queries involving many rows and colomns, PostgreSQL's performance can degrade.  This slower performance can be a concern in high-speed, large-scale applications where rapid query execution is critical.  

4. *Complexity*:  
    - PostgreSQL can be more complex to set up and maintain because of its advanced features, especially for those who are unfamiliar with it.  This complexity might slow down developement with its learning curve for new users.  

### Conculsion
For Flask applications, PostgreSQL can be a powerful and flexible database option.  However, it might not be the best choice for projects that need rapid developement, simple setup, or working with unstructured data, where as another database type might be better suited.  

### References
* https://www.aalpha.net/blog/pros-and-cons-of-using-postgresql-for-application-development/
* https://www.geeksforgeeks.org/postgresql-tutorial/?ref=shm
* https://www.youtube.com/watch?v=Yfrrjt1ieyk

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
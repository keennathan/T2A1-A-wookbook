# Q1 Describe the architecture of a typical API project, such as a Flask application.
# Model View Controller Architecture
Software architecture is a way that we can describe software systematically and also refers to how different software interact with each other.  One of the most popular Software architectures is Model-View-Controller(MVC).  
<br>  
MVCs' design patern divides any application into three interconnected components, allowing for effecient code organisation, easier maintenance and scalability. 

*MVC Architecture Diagram*  
![MVC Architecture Diagram](docs/MVC-diagram.png)
## The Model  
The Model component is resposible for managing the application's data related logic, such as the schema's and interfaces of the project.  It interacts with the database to define the data structure and retrieves, manipulate and store data.  It acts as a middleman between the database and the controller.

## The View
The View component handles the presentation part of the application with things that the user can interact with, such as text boxes, dropdowns etc.  Its primary role is to displays the data, and sends all the inputs from the user to the Controller component.  

## The Controller  
The controller component acts as the go-between for the Model and View components.  It handles and processes the user inputs then determines what data from the *model* will be displayed in the *View*.  

## Benifits of MVC
The benefits of this architecture is that it separates each component making it easier to maintain and organise code by setting clear responsibilties for each.  By separating each part, it can be developed, scaled, and tested independently.  

### References 
* https://www.youtube.com/watch?v=DUg2SWWK18I 
* https://www.freecodecamp.org/news/model-view-architecture/
* https://www.geeksforgeeks.org/mvc-design-pattern/
* https://www.guru99.com/mvc-tutorial.html

# Q2 Identify a database commonly used in an API project (such as a Flask application) and discuss the pros and cons of this database.

# PostgreSQL
PostgreSQL, while one of the oldest, is still one of the most advanced Relational Database Management Systems out there.  It is open source, meaning it is managed and maintained by a vibrant community of people and the source code is available to anyone under the PostgreSQL licence.  

## Pros 
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

## Cons

1. *Database Structure*:  
    - PostgreSQL is predominantly a relational database, meaning it works with structured data in predefined schemas.  This can be limiting when dealing with unstructured or semi structured data, where as NoSQL databases like MongoDB might be more flexible.  

2. *Open Source Limitations*:
    - While open source is generally an advantage, it also means that PostgreSQL lacks the commercial support and warranties that come with branded software.  This can be a drawback for businesses that require guaranteed support or liability protection.  

3. *Slower Performance*:  
    - When handling very large datasets, particulary when there are complex queries involving many rows and colomns, PostgreSQL's performance can degrade.  This slower performance can be a concern in high-speed, large-scale applications where rapid query execution is critical.  

4. *Complexity*:  
    - PostgreSQL can be more complex to set up and maintain because of its advanced features, especially for those who are unfamiliar with it.  This complexity might slow down developement with its learning curve for new users.  

## Conculsion
For Flask applications, PostgreSQL can be a powerful and flexible database option.  However, it might not be the best choice for projects that need rapid developement, simple setup, or working with unstructured data, where as another database type might be better suited.  

### References
* https://www.aalpha.net/blog/pros-and-cons-of-using-postgresql-for-application-development/
* https://www.geeksforgeeks.org/postgresql-tutorial/?ref=shm
* https://www.youtube.com/watch?v=Yfrrjt1ieyk

# Q3 Discuss an implementation of an Agile project management methodology for an API project.
# Kanban-Agile Methodology
Kanban was originally developed as part of the Toyota Production System in the 1940's and has became a popular Agile Software Developement methodology.  Its key function was as a signaling device to manage the flow of parts in a 'pull' production system.  With respect to software developement, Kanban helps teams to visualise their workflow, manage work in progress(WIP), and continuously improve process through incremental changes.  

![Kanban Board](docs/kanbanBoard.png)

## Key Concepts and Features  
1. **Kanban Board:**  
    - A Kankan board is a visual tool that represents the workflow of a project.  It is divided into different columns that state different phases of the developement process, such as "To-Do", "In-Progress", and "Done".  These Tasks are represented as cards, that move across the columns as they progress through the workflow.  
    - The board can be physical (eg. sticky notes on a whiteboard) or digital (eg. tools like Trello or Jira).  It provides a clear overview of the status of each task and helps identify where tasks might be stuck for too long.  
2. **Pull Systems:**  
    - Kanban operates with a pull system, which means tasks are only pulled into the workflow when there is a capacity to handle them.  The pull system helps prevent overloading team members and ensures a steady flow of work, reducing delays and improving efficiency.  
3. **Work-In-Progress (WIP) Limits:**  
    - One of the key practices in Kanban is to set WIP limits, this helps cap the number of tasks that can be in progress at any given time.  These limits help keep the team focused on completing tasks rather then statring new ones, which enhances productivity and reduces the likelihood of work getting stuck in the pipeline.  
4. **Kanban Principles:**  
    - *Start with the Existing Process:* Kanban emphasises beginning with the current process without drastic changes.  Instead, it focuses on making incremental, evolutionary improvements.  
    - *Agree to Incremental Changes:* Teams should aim for small, manageable changes rather than large-scale overhauls, which coulsd disrupt workflow and meet resistance.  
    - *Respect Current Roles and Responsibilities:* Kanban does not prescribe specific roles, allowing teams to maintain their current structure while gradually adoping the methodology.  
5. **Cumulative Flow Diagram (CFD):** A CFD is an advanced Kanban tool that provides a visual representation of the workflow over time.  It shows the distribution of tasks across different stages of the process, helping teams identify trends, predict bottlenecks, and make adjustments to improve workflow stability.  

## Steps of the Kanban Approach
1. **Visualise Workflow:**  
    - Map out the current process and define the stages of work.  Visualise these stages on a board, with tasks moving from left to right as they process.  
2. **Establish a Pull System:**  
    - Implement a pull system where work is only pulled into the next stage when there is the capacity to do so, preventing bottlenecks and ensuring smooth flow.  
3. **Set WIP Limits:** 
    - Define limits on how many tasks can be in each stage of the process at any time.  This will encourage teams to complete the tasks before starting new ones, enhancing focus and reduce mulitasking.  
4. **Apply Pull Signals:**  
    - Use signals to indicate when new tasks can be pulled into stage.  Such as, when a task is completed in one stage, it signals the team to pull a new task from the previous stage.  

In summary, using Kanban for API developement not only streamlines the workflow and enhances team productivity but also ensures that the project is delivered efficiently, with a strong focus on quality.  The flexibility, visibility, and continuous improvement principles of Kanban make it an ideal choice for managing the complexities and fast-paced demands of API projects.  


### References
* https://www.youtube.com/watch?v=36Mmyi65mko
* https://www.geeksforgeeks.org/what-is-kanban/
* https://www.geeksforgeeks.org/kanban-agile-methodology/
* https://hygger.io/blog/online-kanban-board/


# Q4 Provide an overview and description of a standard source control process for an API project.

# Source Control

Source Control, or version control, is a crucial component of mordern software developement, particulary for API projects.  It involves involves managing changes to code over time, ensuring that every modification is tracked, documented, and can be reviewed.  This process allows for multiple developers to collaborate efficiently, even when they are working in different locations, and ensures that the code remains organised,secure, and recoverable.  

## Key Components
1. **Repository:**  
    - The repository is like a database that stores all versions of the project.  It contains the complete history of all the changes made to the API's codebase, including who made the changes, when they were made, and why they were made.  The repository can be centralised (eg. with a system like Subversion) or distributed (eg. with Git).  
2. **Branches:**  
    - A branch is a parallel version of the code the diverges from the main repository.  In an API project, branches are typically used to develope new feature, fix bugs, or test changes without affecting the main codebase.  Developers work on their own branches and only merge their changes back into the main branch after a thorough review and testing has occured.  
3. **Commits:**  
    - A commit is an action that saves a snapshot of the developer's changes to the repository. Each commit includes a message describing what was changed and why, which helps in maintaining a clear historyof the project's progression.  
4. **Pull Requests:**  
    - When a developer wants to merge their changes from a feature branch into the main branch, they open a pull request.  This process allows the other team members to review the code, suggest improvements, or catch potential issues before the changes are integrated to the main codebase.  
5. **Push and Pull Operations:**  
    - In a distributed version control system, like Git, changes are first committed to the developer's local repository.  These changes are then pushed to the central repository so that they can be shared with others.  Conversely, a pull operation is used to fetch updates from the central repository into the local environment.  

## Standard Source Control Workflow for an API Project 
1. **Cloning the Repository:** Each developer clones the repository from the central repository to create a local copy on their machine.  This includes the entire history of the project and all the branches.  
2. **Creating a New Branch:** Before making any changes, developers create a new branch from the main.  This is typically named after the feature that the developer will be working on (eg.'feature/user-auth').  
3. **Developing and Committing Changes:** The developer will then make changes to the codebase.  Once the changes are ready, they are added to the staging area and then committed locally with a descriptive message.  
4. **Pushing the Branch:** After committing, the developer will push the branch to the central repository.  This makes the changes available for review by the rest of the team.  
5. **Creating a Pull Request:** The developer will then open a pull request, inviting other team members to review the changes.  The pull request should link to any relevent issues or tasks and include a detailed explanation of what has been changed.  
6. **Code Review and Testing:** The pull request is reviewed by other developers.  They may suggest improvements or request changes.  Once the review is complete, automated test are usually run to make sure the new code does not break existing functionality.  
7. **Merging the Branch:** Once the code has passed the review and testing stages, it is then merged into the main branch.  This step usually involves another review to ensure that the merge does not introduce conflicts.  
8. **Deleting the Branch:** After merging, the feature branch is deleted to keep the repository clean and focused on active branches.  

In summary, by implementing a standard source control process, API projects can maintain a high level of code quality, ensure seamless collaboration, and reduce the risk of errors in the production environment.

### References
* https://www.atlassian.com/git/tutorials/what-is-git
* https://www.geeksforgeeks.org/version-control-systems/

# Q5 Provide an overview and description of a standard testing process for an API project.

# API Testing
API testing is a crucial component of software testing, it ensures the API functions as intended, providing reliable, secure and effient communication between the different software components.  While UI testing focuses on the look and feel of an application, API testing centers on the backend, notably the business logic, security, and the data response mechanisms.  

# API Testing Process
## 1. Define the Scope and Requirements
When beginning the API testing process, it is essential to define the scope and understanding of the API.  It is key to have a comprehensive understanding of how the API should function and what business logic it handles.  This requires identifying all the API endpoints that need to be tested, which includes the methods (such as GET, POST, PUT, DELETE) and the parameters that are associated with each.  It is also a good idea to define the expected HTTP response codes for both successful and unsuccessful requests, along with the corresponding error messages.  

## 2. Test Case Development
After the scope is defined, the next step involves developing test cases that will cover a wide range of scenarios, includeing normal, boundary and error conditions.  Each test case should specify input conditions, expected results and actual results to allow for thorough testing.  It is also important to include tests that will measure performance, such as response times and data integrity checks, and tests that validate authorisation and error handling.  Non-function features, like the API's ability to perform well under load, maintain security and operate reliably should aslo be tested.  

## 3. Execution of Test Cases
When the test cases are developed, execution of these tests can begin.  Automated testing tools like Postman, Insomnia or SoapUI are typically used to send requests to the API and validate the responses with the expected results.  These tests are particularly valuable in Agile environments, where continuous testing and fast feedback are essential.  However, manual testing still plays a part, especially for exploratory testingof areas not covered by automated scripts.  Manual tests are useful for newly introduced features that require a more-hands on aproach.  

## 4. Evaluation and Reporting
After executing the tests,  the results need to be thoroughly analyzed.  This involves comparing the actual results with the expected outcomes and identify any discrepancies.  If there are any failures, errors, or unexpected behaviors they should be logged and investigated further.  Performance and load texting are especially important at this stage to assess how well the API will handle increased loads and stress conditions.  Additionally, security validation is essential to check for vulnerabilities.  

## 5. Bug Fixing and Retesting
Once the issues are identifyed, they need to be tackled through a bug-fixing process.  Developers work on the bugs, and once they are fixed, the API is then retested to ensure the issues are resolved.  This step often includes testing to ensure that the new changes have not introduced new bugs or negatively impacted other parts of the API.  Continuous retesting help maintain the stability of the API as it evolves.  

## In Summary
By following these steps, developers can ensure that the API's are not only functional and reliable but also secure and efficient, which ultiately lead to higher qualtity software and improve customer satisfaction.  

### References
* https://testsigma.com/guides/api-testing/
* https://caisy.io/blog/api-testing-for-developers
* https://www.techtarget.com/searchapparchitecture/definition/API-testing

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
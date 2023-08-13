User Story 1

**As a** customer    
**I need** to create an account with my basic information  
**So that** I can start shopping on the e-commerce website  
      
### Details and Assumptions
    * The database model and a Python Flask-based API with an enpoint to create a customer account has already been developed.      
### Acceptance Criteria     
    gherkin 
    Given the customer account microservice is running
    When I provides my name and address to create the account
    Then the microservice should create my account
    And I should receive a confirmation message

User Story 2

**As a** customer    
**I need** to be able to view my account informationc information  
**So that** I can review my details and make changes if needed  
      
### Details and Assumptions
    * The database model and a Python Flask-based API with an enpoint to create a customer account has already been developed.      
### Acceptance Criteria     
    gherkin 
    Given the customer account microservice is running
    And I have a valid customer ID
    When I request to view my account information
    Then the microservice should return my name and address details

User Story 3

**As a** customer    
**I need** to be able to update my account information  
**So that** I can keep my details accurate and up-to-date  
      
### Details and Assumptions
    * The database model and a Python Flask-based API with an enpoint to create a customer account has already been developed.      
### Acceptance Criteria     
    gherkin 
    Given the customer account microservice is running
    And I have a valid customer ID
    When I provide updated name and address details
    Then the microservice should update my account information
    And I should receive a confirmation message

User Story 4

**As a** customer    
**I need** to be able to delete my account  
**So that** I can remove my personal information from the system if I want
      
### Details and Assumptions
    * The database model and a Python Flask-based API with an enpoint to create a customer account has already been developed.      
### Acceptance Criteria     
    gherkin 
    Given the customer account microservice is running
    And I have a valid customer ID
    When I request to delete my account
    Then the microservice should delete my account information
    And I should receive a confirmation message

User Story 5

**As a** customer account manager   
**I need** to be able to list all customer accounts  
**So that** I can view a summary of all registered customers  
      
### Details and Assumptions
    * The database model and a Python Flask-based API with an enpoint to create a customer account has already been developed.      
### Acceptance Criteria     
    gherkin 
    Given the customer account microservice is running
    When I request to list all customer accounts
    Then the microservice should return a paginated list of customer names and addresses
    And the list contains up to <page_size> customer accounts per page
    And the list is sorted in ascending order based on customer names
    And I can navigate to different pages using the pagination links

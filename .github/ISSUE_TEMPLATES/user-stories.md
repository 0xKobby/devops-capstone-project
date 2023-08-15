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

User Story 6

**As a** Developer
**I need** automation to build and test every pull request
**So that** I do not have to rely on manual testing of each request, which is time-consuming
    
### Details and Assumptions
    * GitHub Actions will be used for the automation workflow
    * The workflow must include code linting and testing 
    * The Docker image should be postgres:alpine for the database
    * A GitHub Actions badge should be added to the README.md to reflect the build status
### Acceptance Criteria
    gherkin
    Given code is ready to be merged
    When a pull request is created
    Then GitHub Actions should run linting and unit tests
    And the badge should show that the build is passing

User Story 7
    
**As a** service provider
**I need** my service to use security headers and CORS policies
**So that** my web site is not vulnerable to CORS attacks

### Details and Assumptions
    * Flask-Talisman will be used for security headers
    * Flask-Cors will be used to establish cross-origin resource sharing (CORS) policies
### Acceptance Criteria
    gherkin
    Given the site is secured
    When a REST API request is made
    Then secure headers and a CORS policy should be returned

User Story 8

**As a** developer
**I need** to containerize my microservice using Docker
**So that** I can deploy it easily with all of its dependencies

### Details and Assumptions
    * Create a `Dockerfile` for repeatable builds
    * Use a `Python:3.9-slim` image as the base
    * It must install all of the Python requirements
    * It should not run as `root`
    * It should use the `gunicorn` wsgi server as an entry point
### Acceptance Criteria
    gherkin
    Given the Docker image named accounts has been created
    When I use `docker run accounts`
    Then I should see the accounts service running in Docker

User Story 9

**As a** service provider
**I need** my service to run on Kubernetes
**So that** I can easily scale and manage the service

### Details and Assumptions
    * Kubernetes manifests will be created in yaml format
    * These manifests could be useful to create a CD pipeline
    * The actual deployment will be to OpenShift
### Acceptance Criteria
    gherkin
    Given the Kubernetes manifests have been created
    When I use the oc command to apply the manifests
    Then the service should be deployed and run in Kubernetes

User Story 10

**As a** developer
**I need** to create a CD pipeline to automate deployment to Kubernetes
**So that** the developers are not wasting their time doing it manually

### Details and Assumptions
    * Use Tekton to define the pipeline
    * It should clone, lint, test, build, and deploy the service
    * Deployment should be to OpenShift
    * It can use a manual trigger for this MVP
### Acceptance Criteria
    gherkin
    Given the CD pipeline has been created
    When I trigger the pipeline run
    Then I should see the accounts service deployed to OpenShift
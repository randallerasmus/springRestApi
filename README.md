# springRestApi
Rest API Design

When Designing A Rest Api there are a few questions that we need to ask 
1.  Who will use our rest API?
2.  How will they use our API?

Then you must design the API based on the requirements

Now the API design process - Step by Step

1.  Review the API requirements
2.  Identify the main resource or Entity
3.  Use the http methods to assign action on a given resource

Lets sketch a Scenario:

You are given a task to create a rest api for a customer relationship management system.

<<<<<<< STEP 1 >>>>>>> REVIEW THE API REQUIREMENTS
So the clients of the CRM system should be able to do the following:

- get a list of customers
- get a single customer by id
- Add a new customer 
- Update a customer
- Delete a customer

*************Based on the above we will have full crud support via the rest api

<<<<<<< STEP 2 >>>>>>> IDENTIFY THE MAIN RESOURCE / ENTITY
- To identify the main resource / entity, look for the most prominent noun

for the purpose of this project --> our main entity here is the "customer"

Now convention is to use plural form of resource for example like /entity:customers

meaning something like this --> /api/customers

<<<<<<< STEP 3 >>>>>>> USE HTTP METHODS TO ASSIGN ACTION ON RESOURCE

| Http Method    | CRUD Actions  |
| :------------- | :----------:  |
|                |               |
|                |               |



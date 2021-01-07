# DESIGNING A RESTFULL API

This explains the simple process of designing a restfull api

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
|  POST          | Create a new Entity                         |
|  GET           | Read a list of entities or a single entity  |
|  PUT           | Update a existing entit                     |
|  DELETE        | Delete an existing entity                   |

This means that here we have our full crud support via the http method and also the best practice in designing a restufll spi

Crud Endpoint Examples

| Http Method    | EndPoint                               |CRUD Action                                  |
| :------------- | :------------------------------------: | :------------------------------------:      |
|  POST          | /api/customers                         |Create a new customer                        |
|  GET           | /api/customers                         |Read a list of customers                     |
|  GET           | /api/customers/{customerId}            |Read a single customer                       |
|  PUT           | /api/customers                         |Update an existing customer                  |
|  DELETE        | /api/customers/{customerId}            |Delete an existing customer                  |

NB!! -  for the POST and PUT methods we will send the customer data as JSON in the request message body 
We will see this later on where we will use postman to complete these two requests.

Now lets look at the ANTI- PATTERNS

These are things you dont do.. These are rest anti patterns , bad practice 
NEVER INCLUDE THE ACTIONS IN THE ENDPOINT

| Http Method    | EndPoint                                     |CRUD Action                                  |
| :------------- | :------------------------------------:       | :------------------------------------:      |
|  POST          | /api/customersList                           |Create a new customer                        |
|  GET           | /api/addCustomers                            |Read a list of customers                     |
|  PUT           | /api/updateCustomers                         |Update an existing customer                  |
|  DELETE        | /api/deleteCustomer                          |Delete an existing customer                  |

Instead use Http methods to assign actions as mentioned below and here you can see we dont place behaviour in the endpoint method
As you can see the entity / resource name has no actions listed in the endpoints

| Http Method    | EndPoint                                     |CRUD Action                                  |
| :------------- | :------------------------------------:       | :------------------------------------:      |
|  POST          | /api/customers                               |Create a new customer                        |
|  GET           | /api/customers                               |Read a list of customers                     |
|  GET           | /api/customers/{customerId}                  |Read a single customer                       |
|  PUT           | /api/customers                               |Update an existing customer                  |
|  DELETE        | /api/customers/{customerId}                  |Delete an existing customer                  |




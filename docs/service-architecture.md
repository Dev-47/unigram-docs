# Service Architecture

The project will be built using the **microservice architechure**, and communicate using asychronous and synchronous protocols.
- For **asynchronous protocols**, we will be using **RabbitMQ** as a message broker.
- For **synchronous protocols**, this is language dependent, check the official documentation of your language to get the HTTP request library

# Short Note on Micoservice Architecture

Microservice is an independent service that can work alone as an application, losely coupled with other applications to perform similar functions.
This makes development faster and easier to maintain, it also encourages usabilty, gives more options on language choices, helps manage resources 
and work load among developers. In this architecture, you can have 2 or more services cummunicating with each other to perform similar operations.

more on microservices
- [From AWS](https://aws.amazon.com/microservices/)
- [From Microsoft](https://docs.microsoft.com/en-us/azure/architecture/guide/architecture-styles/microservices)


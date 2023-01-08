# [Calculator-Color](https://www.calculator.net/)

## Contributing

We love contributions!
Take a look at [our contributing page](CONTRIBUTING.md).

### Use case

The sample application has two services namely service-one and service-two. Each of the service has its own database service-one-db and service-two-db respectively. During the startup of the services, it persists the service name and an auto generated UUID in its perspective database and sends the data to the RabbitMQ exchange which then broadcasts the data to all the queues based on the routing key. Every microservices listens to its own RabbitMQ queue and keeps updating the database as and when it receives the data.

Below are the screens of the application.

![alt tag](https://github.com/mudigal-technologies/microservices-sample/blob/version-5/documents/screens/_Web%20App/01.%20Home.png?raw=true)

Clicking on the tab's one or two the data that you see on the screen is based on the data fetched by the respective service by calling its database.

![alt tag](https://github.com/mudigal-technologies/microservices-sample/blob/version-5/documents/screens/_Web%20App/02.%20One.png?raw=true)

Notice that the UUID generated for service-one which lies in service-one-db is in sync with service-two tab which is achieved by RabbitMQ (asychronous communication between microservices). 

![alt tag](https://github.com/mudigal-technologies/microservices-sample/blob/version-5/documents/screens/_Web%20App/03.%20Two.png?raw=true)




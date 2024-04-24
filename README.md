## **Hi! :wave:, I'm Muhammad Fiqo Anugrah and this is my repo for Tutorial 8 Adpro C**


> REFLECTION

**a. What is AMQP?**

AMQP stands for Advanced Message Queuing Protocol, a standard communication protocol used to facilitate asynchronous message exchange between components, services, or systems. This protocol is designed to ensure reliable and secure communication, supporting various features such as message queuing, routing (through exchanges and bindings), publish-subscribe mechanisms, and transactions. The reliability and flexibility of AMQP make it highly suitable for applications requiring guaranteed message delivery and efficient communication in distributed environments.

**b. What does "guest:guest@localhost:5672" mean?**

"guest:guest": This represents a username and password pair used for authentication to an AMQP server. In this context, "guest" is the default username and also the default password commonly used in development or testing settings, not in production, for security reasons.
"localhost": This term indicates that the connection to the AMQP server will be made to the local machine, i.e., the computer where this command is executed. It is often used for local testing and development where the server runs on the same machine as the client.
"5672": This is the standard TCP port number used by AMQP servers to listen for incoming connections. This port is designated by convention for AMQP communication, although it can be configured to use a different port if necessary.
Overall, "guest:guest@localhost:5672" describes using default credentials to access an AMQP server running on the local machine at the standard port. It is typically used for development and testing purposes.


## Simulation Slow Subscriber
![image](https://github.com/fiqoanugrah/tutorial-8-subscriber/assets/87713462/c2ca651a-07ef-43ff-9945-1e93fdbfac44)
The screenshot from the RabbitMQ Management Interface above shows a peak of approximately 30 messages in the queue at a certain point in time. This indicates that the publisher sent a burst of messages that temporarily accumulated in the queue. The consumer was either not fast enough to process these messages as they arrived or there was a deliberate pause in processing, resulting in the spike observed.
In my setup, the total number of queued messages peaked at around 30. This is reflective of the publisher's configuration and the rate at which it was publishing messages, as well as the consumer's ability to process those messages at the time of the capture.







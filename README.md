## **Hi! :wave:, I'm Muhammad Fiqo Anugrah and this is my repo for Tutorial 8 Adpro C**


> REFLECTION

a. What is AMQP?

AMQP stands for Advanced Message Queuing Protocol, a standard communication protocol used to facilitate asynchronous message exchange between components, services, or systems. This protocol is designed to ensure reliable and secure communication, supporting various features such as message queuing, routing (through exchanges and bindings), publish-subscribe mechanisms, and transactions. The reliability and flexibility of AMQP make it highly suitable for applications requiring guaranteed message delivery and efficient communication in distributed environments.

b. What does "guest:guest@localhost:5672" mean?

"guest:guest": This represents a username and password pair used for authentication to an AMQP server. In this context, "guest" is the default username and also the default password commonly used in development or testing settings, not in production, for security reasons.
"localhost": This term indicates that the connection to the AMQP server will be made to the local machine, i.e., the computer where this command is executed. It is often used for local testing and development where the server runs on the same machine as the client.
"5672": This is the standard TCP port number used by AMQP servers to listen for incoming connections. This port is designated by convention for AMQP communication, although it can be configured to use a different port if necessary.
Overall, "guest:guest@localhost:5672" describes using default credentials to access an AMQP server running on the local machine at the standard port. It is typically used for development and testing purposes.









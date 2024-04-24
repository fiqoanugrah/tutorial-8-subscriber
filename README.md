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


![image](https://github.com/fiqoanugrah/tutorial-8-subscriber/assets/87713462/24b3de0a-ac7c-4ea7-a659-28c8b0061771)


![image](https://github.com/fiqoanugrah/tutorial-8-subscriber/assets/87713462/b28ec3a1-a6ee-4984-b99f-0fe90da6349c)

After running three different subscribers in separate terminals with `cargo run`, the message queue's spike decreases faster than when running a single subscriber. This behavior is expected because having multiple subscribers allows for concurrent message consumption. Each subscriber takes a portion of the message load, processing messages in parallel, which enhances throughput and reduces the time messages spend in the queue.

This reflects a well-distributed workload among multiple consumers, a key principle in scalable message-driven architectures. It's an effective way to handle bursts of messages or high message volumes.

Upon reviewing the code for both the publisher and subscribers, there are always opportunities for improvement. Some considerations include:

- **Batch Processing**: If the subscribers can process messages in batches, this could reduce the overhead of acknowledging each message individually.

- **Performance Monitoring**: Implementing more detailed logging or metrics collection for both publishers and subscribers could provide insights for further optimizations.

- **Error Handling**: Reviewing how the system behaves under failure (e.g., subscriber crashes or network issues) and ensuring there's robust error handling and recovery.

- **Message Acknowledgment**: Ensuring that messages are not lost, it might be beneficial to review the acknowledgment strategy. For instance, ensuring idempotence in message processing if auto acknowledgment is enabled.

- **Resource Allocation**: Monitoring the resources (CPU, memory usage) to make sure the system is properly provisioned.


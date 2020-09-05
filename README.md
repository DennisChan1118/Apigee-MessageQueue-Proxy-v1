# Apigee-MessageQueue-Proxy-v1

## Introduction
* Implement in a No Target Proxy.
* MessageQueue connection information is setting in Key Value Map (mq-configs).
* Use the [Apigee-Javacallout-JmsIntegrator](https://github.com/DennisChan1118/Apigee-Javacallout-JmsIntegrator) JMS program in Java Callout policy to send message to ActiveMQ.
* There is only a queue producer feature. But it's easy to extend the JMS program above to implement a queue comsumer or a publish/subscribe topic feature.

## Use the following 'curl' command to invoke 'SendMessage' service:
```
curl -X POST 'http://{your host}:{your port}/v1/queue/send' \
-H 'Content-Type: text/plain' \
-d 'Hello!!!'
```
The expected result is
```
Hello!!!
```
Use Message Queue web console or command line to check the message in the queue.

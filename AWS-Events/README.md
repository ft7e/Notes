# AWS: Events

### SQS and SNS are important components for scalable, large scale, distributed, cloud-based applications:

## Comparisons: SQS vs SNS in AWS — Simple Notification Service and Simple Queue Service.

SNS is a distributed publish-subscribe service.

SQS is distributed queuing service.

Amazon SNS is a fast, flexible, fully managed push notification service that lets you send individual messages or to bulk messages to large numbers of recipients. Amazon SNS makes it simple and cost effective to send push notifications to mobile device users, email recipients or even send messages to other distributed services.

Amazon SQS is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications.

SQS is distributed queuing system. Messages are not pushed to receivers. Receivers have to poll SQS to receive messages. Messages can be stored in SQS for short duration of time (max 14 days).

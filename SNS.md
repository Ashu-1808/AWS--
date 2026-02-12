
#  Amazon SNS (Simple Notification Service)

## What is SNS?
```
- Amazon SNS is a fully managed publish/subscribe (Pub-Sub) messaging service.
- It is used to send messages or notifications to multiple subscribers instantly.
- Fast, flexible, fully managed push notification service
- Web service that manages sending messages to subscribing endpoints
- Supports individual delivery or fan-out delivery
- Pay-as-you-go model (No upfront cost)


How SNS Works:
  Publisher  →  Topic  →  Subscribers


Step-by-Step Flow:
 1. Publisher sends a message
 2. Message is published to an SNS Topic
 3. SNS automatically delivers the message to all Subscribers
   (This architecture is called: Fan-Out Architecture
     One message → Delivered to multiple endpoints.)

Core Components
 1. Topic :
  - Logical access point for messages
  - Messages are published to a topic (not directly to users)
  - Each topic has a unique **ARN (Amazon Resource Name)**

 2. Publisher :
  - Service or application that sends messages
  - Examples:EC2, S3, CloudWatch, Lambda, Custom, applications

 3. Subscriber
  - Endpoint that receives messages
  - Supported endpoints: Email,SMS, SQS, Lambda, HTTP / HTTPS



SNS Key Features :
  1. Fully managed service
  2. High availability
  3. Real-time message delivery
  4. Push-based system
  5. Message fan-out
  6. Scalable
  7. No server management required


SNS Pricing :
 - Pay-as-you-go
 - No upfront cost
 1. SMS
   - First 100 messages are free
   - After that pricing depends on country
 2. Email
   - 1000 emails are free
   - After that approx ₹2 / 100000 emails
 3. SQS & Lambda
   - Free tier available for lifetime


SNS Common Use Cases :
  1. Application alerts
  2. CloudWatch alarms
  3. Auto Scaling notifications
  4. Order confirmation emails
  5. Broadcasting messages
  6. Fan-out to multiple SQS queues
  7. System event notifications

```
# 🔹 SNS vs SQS

| SNS                           | SQS                            |
| ----------------------------- | ------------------------------ |
| Push-based                    | Pull-based                     |
| Pub-Sub model                 | Queue model                    |
| Sends to multiple subscribers | One consumer processes message |
| Real-time notifications       | Message storage & processing   |
| Fan-out supported             | No direct fan-out              |

# 🔹 Simple Architecture Diagram

```
                +-----------+
                | Publisher |
                +-----------+
                      |
                      v
                +-----------+
                |   SNS     |
                |   Topic   |
                +-----------+
               /     |      \
              v      v       v
           Email    SQS    Lambda
```


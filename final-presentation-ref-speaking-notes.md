# Speaking Notes for Final Presentation

## Introduction & Agenda (Wallace - 1 minute)

Good morning everyone. My name is Wallace Msagusa, and along with my teammates – Simon, Hussein, David, and Emma – we're presenting our System Orchestration for User Engagement project for Hiveonline. Today, we'll share our progress with our client representative, Qusai Alfaki, and our faculty advisor, Professor Ostheimer.

In our presentation today, we'll first introduce the problem we've addressed, then outline our proposed solution. We'll demonstrate our implementation with a live demo, evaluate our work, and conclude with future directions. Now I'll hand over to Emma, who will describe the problem we're solving.

## Problem Description (Emma - 1.5 minutes)

Thank you, Wallace.

Hiveonline is an impact FinTech that connects smallholder farmers across Africa with markets, resources, and investment opportunities. They serve over 65,000 farmers in Kenya, Mozambique, and Ghana, but face a significant challenge with user engagement.

The core problem is that users interact with Hiveonline's platforms but don't receive enough personalized reminders or notifications. The prompts they do receive are generic and not intelligent, leading to declining user retention over time.

For example, when a farmer receives payment for their harvest, they should get a smart reminder to repay their loan if they can afford it – but without automated orchestration, these opportunities are missed.

Our project aims to solve this problem by creating an orchestration system that applies business logic to trigger meaningful, timely communications that drive user engagement and financial activity. Now Simon will explain our solution.

## Proposed Solution (Wallace - 2 minutes)

Thank you, Emma.

We've designed a layered architecture that integrates seamlessly with Hiveonline's existing systems. As you can see in this diagram, we have five key layers:

The Front-End Layer interfaces with MyCoop and VSLA systems that users already interact with.

At the heart of our system is the Orchestration Layer, which combines FastAPI for real-time processing with Apache Airflow for scheduled workflows. This hybrid approach allows us to handle both immediate events and time-based triggers.

The Integration Layer uses Kafka Consumers and REST Clients to connect with Hiveonline's services, ensuring we can react to events and access the data needed for intelligent orchestration.

The Notification Layer handles the multi-channel delivery across SMS, email, and in-app notifications, with support for multiple languages.

Finally, we have the Storage Layer using PostgreSQL and the Monitoring Layer with Prometheus and Grafana to track system performance.

Our implementation focuses on five key triggers that address the most critical user engagement scenarios. I'll now hand over to Hussein who will demonstrate our system in action.

## Demo (Simon - 3 minutes)

Thank you, David.

I'll now demonstrate our orchestration system in action. We've developed a web interface for monitoring and managing the triggers and notifications.

[SHOW LOGIN SCREEN]
First, I'll log in to our administrative dashboard, which gives us an overview of all active triggers and recent notification activities.

[SHOW DASHBOARD]
Here on the dashboard, you can see statistics for our five implemented triggers. For instance, the User Inactivity trigger has sent 154 notifications this week, with an engagement rate of 42%.

[SHOW TRIGGER CONFIGURATION]
Let me show you how we configure a trigger. This is the Production Plan Overdue trigger, which identifies when a farmer's crop plan is past its end date with no deliveries recorded. We can set parameters like the number of days overdue before notification, and which channels to use.

[SHOW NOTIFICATION TEMPLATES]
Here are our notification templates in multiple languages. For each trigger, we have templates for different channels - SMS, email, and in-app notifications. You can see the template variables that are populated with user-specific data.

[SHOW NOTIFICATION LOG]
This is the notification log, showing recent communications sent to users. We track delivery status and user engagement to measure effectiveness.

[DEMONSTRATE REAL-TIME TRIGGER]
Finally, let me show a real-time trigger in action. When I create this new VSLA group member, you can see the system immediately generates welcome notifications for the member and alerts for the group administrators.

That completes our demonstration. I'll now hand over to David who will evaluate our implementation.

## Evaluation (David - 1.5 minutes)

Thank you, Simon.

Let me share our evaluation of how the solution addresses Hiveonline's user engagement challenge.

We've successfully implemented all Seven priority triggers with complete workflows - from event detection to multi-channel notification delivery. Our system handles both real-time events like new member additions and scheduled checks for inactivity or overdue items.

The architecture we've built is scalable and extensible, making it easy to add new triggers as Hiveonline's needs evolve. We've also created a comprehensive multi-language notification system, essential for Hiveonline's diverse user base across multiple African countries.

During implementation, we faced several challenges. Integration complexity was addressed through a phased approach and using mock services during development. For real-time performance concerns, we implemented a queue-based architecture to handle peak loads.

Supporting multiple languages was challenging, but our template-based localization system ensures accurate translations. Finally, we managed timeline pressure through MoSCoW prioritization, ensuring we delivered the most valuable functionality first.

Now I'll hand back to Wallace to discuss future work.

## Future Work (Hussein - 1 minute)

Thank you, David.

While we've delivered a robust orchestration system, there are several areas for future enhancement:

First, developing more sophisticated trigger conditions using advanced business rules. To allow more personalized communications based on user behavior patterns.

Second, integrating deeper user analytics that would help to track notification effectiveness and refine engagement strategies over time.

Third, adding machine learning to predict optimal notification timing and content.

Fourth, extending to additional communication channels like WhatsApp and Telegram to reach users through their preferred platforms.

Finally, a self-service portal to allow Hiveonline administrators to create custom triggers without requiring technical support.

This concludes our presentation. We'd like to thank Qusai and Professor Ostheimer for their guidance throughout this project. We're now open to any questions you might have.

## Q&A Session (All team members - 5 minutes)

[Be prepared to answer questions related to:
- Technical implementation details
- Integration with Hiveonline's existing systems
- Performance and scalability considerations
- Security and privacy features
- Localization and language support]

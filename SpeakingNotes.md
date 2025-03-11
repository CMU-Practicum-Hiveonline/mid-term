# 10-Minute Speaking Notes for Updated Hiveonline Presentation

## Hussein (Slides 1-2) - 2 minutes

### Slide 1: Title Slide
Good morning everyone. My name is Hussein Murashi, and along with my teammates – Wallace, Simon, David, and Emma – we're presenting our System Orchestration for User Engagement project for Hiveonline. Today, we'll share our progress with our client representative, Qusai Alfaki, and our faculty advisor, Professor Ostheimer. Thank you for joining us.

### Slide 2: Agenda
Here's what we'll cover today. We'll start with an introduction to the problem we're addressing, followed by our project goals and proposed solution. We'll then discuss key requirements, share our current progress, outline challenges we've faced and our approach to overcome them, and finally present our next steps. 

I'll now hand over to Emma, who will introduce Hiveonline and describe the problem we're addressing.

## Emma (Slides 3-4) - 2 minutes

### Slide 3: Introduction and Problem Description
Thank you, Hussein. 

Hiveonline is a digital financial platform that uses blockchain technology to connect African smallholder farmers with markets, resources, and opportunities across multiple countries. They currently serve over 65,000 farmers in Ghana, Kenya, and Mozambique.

The core problem Hiveonline faces is declining user retention due to insufficient personalized communication. With users speaking different languages across multiple countries, generic notifications fail to drive meaningful engagement. There's no automated system to send relevant, timely prompts to users based on their activity or financial situation.

A key example is when a farmer receives payment for their harvest but doesn't receive a smart reminder to repay their loan—a missed opportunity for both the farmer and Hiveonline.

### Slide 4: Project Goals
To address these challenges, we've defined five key goals:

First, we aim to automate communication using rule-based triggers that initiate timely, personalized notifications.

Second, we're targeting a 30% increase in platform usage through these relevant communications.

Third, we'll enable multi-channel delivery with support for SMS, in-app, and email notifications in multiple languages.

Fourth, we'll facilitate financial actions by prompting users at optimal times, such as loan repayment reminders after harvest payments.

Finally, we'll provide analytics to measure the effectiveness of these communications, helping Hiveonline refine their engagement strategies.

I'll now pass to Simon, who will explain our proposed solution and key requirements.

## Simon (Slides 5-6) - 2 minutes

### Slide 5: Proposed Solution and Planned Deliverables
Thank you, Emma.

Our solution is a layered architecture designed to integrate seamlessly with Hiveonline's existing systems. As you can see in this diagram, we have:

The Front-End Layer connects with the existing MyCoop and VSLA interfaces that users already interact with.

The Orchestration Layer is our core component, combining FastAPI for real-time processing and Apache Airflow for scheduled workflows.

The Integration Layer uses Kafka Consumers and REST Clients to connect with Hiveonline's existing services.

The Notification Layer handles multi-channel message delivery across different platforms.

And finally, we have the Storage Layer using PostgreSQL and the Monitoring Layer with Prometheus and Grafana for performance tracking.

### Slide 6: Key Requirements
For our implementation, we've identified five key requirements:

Our Development Framework combines FastAPI for API endpoints and real-time processing with Apache Airflow for workflow orchestration.

For the Messaging System, we're implementing real-time Kafka processing to handle event streams from multiple sources.

The Business Logic component is a contextual communications engine that determines when and how to engage users.

We'll support multiple Communication Channels including SMS, Email, and In-App Notifications to reach users through their preferred medium.

Finally, we're implementing comprehensive Monitoring Tools with a performance metrics dashboard to track system health and engagement effectiveness.

Now, Wallace will take you through our current progress and implementation approach.

## Wallace (Slides 7-8) - 2 minutes

### Slide 7: Current Progress
Thank you, Simon.

This diagram illustrates our current implementation progress. We've established the foundational architecture for how the orchestration system will integrate with Hiveonline's existing platform. 

On the top left, you can see the user-facing apps—MyCoop and VSLA—which connect to various hiveonline platform services, including Identity, Finance, Crop Plans, Notification, and Marketplace.

Our orchestration system, highlighted in blue, connects to these services via HTTP and Kafka streams. Within our system, we've implemented:
- The FastAPI component for handling real-time events
- The rule-based engine using Apache Airflow with DAGs, scheduling, and execution components
- A task engine with workers to process notifications
- A PostgreSQL database for data persistence
- And performance monitoring using Grafana and Prometheus

We're currently in the process of connecting these components to create a seamless workflow.

### Slide 8: Challenges and Mitigation
We've encountered several challenges during our implementation, but we've developed effective mitigation strategies for each:

The first challenge is Integration Complexity, due to the multiple systems and data formats we need to work with. We're addressing this using mock services for development and taking a phased integration approach.

For Real-Time Performance concerns, especially with the potential volume of events, we're implementing a queue-based architecture to handle peak loads efficiently.

Multi-Language Support presents challenges in ensuring accurate translations. We're developing a template-based localization framework to address this.

Finally, we're dealing with Timeline Pressure due to our delayed start by using MoSCoW prioritization to ensure we deliver the most valuable functionality first.

I'll now hand over to David, who will walk us through our timeline, next steps, and references.

## David (Slides 9-11) - 2 minutes

### Slide 9: Current and Next Steps
Thank you, Wallace.

Looking at our project timeline, we've completed several key milestones, including requirements analysis, technical architecture design, development environment setup, and implementing the core FastAPI service.

We're currently in the first implementation phase, running from March 11-25, where we're developing the three core trigger scenarios: inactivity detection, group prompts, and loan repayment reminders.

Our next phase, from March 26 to April 10, will focus on API connections and testing in the staging environment.

The final phase, from April 11-22, will include production release and technical documentation. We're on track with this timeline and confident in our ability to deliver a high-quality solution that meets Hiveonline's needs.

### Slide 10: References
For this project, we've consulted several key resources, including Hiveonline's platform documentation and documentation for Apache Airflow, FastAPI, and Kafka Streams. These resources have been valuable in guiding our technical decisions and ensuring alignment with best practices.

### Slide 11: Q&A
This concludes our midterm presentation. We'd like to thank Qusai and Professor Ostheimer for their time and guidance throughout this project. We're now open to any questions you might have about our progress or plans.

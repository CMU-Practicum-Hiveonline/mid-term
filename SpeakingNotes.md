
# Speaking Notes - System Orchestration for User Engagement Presentation

## Slide 1: Title Page (30 seconds)
**Speaker: Wallace**

Good morning everyone. My name is Wallace, and along with my team members – Simon, Hussein, David, and Emma – we're working on the System Orchestration for User Engagement project for Hiveonline. 

Today, we're excited to share our progress with you, particularly our client representative, Qusai Alfaki, and our faculty advisor, Professor Ostheimer. Thank you for joining us.

## Slide 2: Agenda (20 seconds)
**Speaker: Wallace**

Here's what we'll cover today. We'll start with the problem we're addressing and our project goals, followed by our proposed solution and current progress. We'll then dive into the technical architecture, implementation approach, challenges we've faced, and our timeline for the remainder of the project.

I'll now hand over to Hussein to describe the problem we're addressing.

## Slide 3: Problem Description (60 seconds)
**Speaker: Hussein**

Thank you, Wallace. 

The core problem Hiveonline faces is declining user retention due to insufficient communication. Users interact with the MyCoop and VSLA platforms but don't receive enough timely reminders or personalized notifications to keep them engaged.

Currently, communications are primarily manual, which doesn't scale effectively for Hiveonline's 65,000+ farmers across Ghana, Kenya, and Mozambique. Each country requires tailored engagement strategies due to language differences and local contexts.

Perhaps most critically, the system is missing opportunities to prompt beneficial financial actions—for example, reminding farmers to repay loans after receiving payment for their harvest.

These challenges impact both user retention and financial outcomes for Hiveonline and its users. Emma will now take us through our project goals.

## Slide 4: Project Goals (60 seconds)
**Speaker: Emma**

Thanks, Hussein.

Our project has five key goals to address these challenges:

First, we aim to automate communication by implementing rule-based triggers that will initiate timely, relevant notifications to users.

Second, we're targeting a 30% increase in platform usage through these relevant communications.

Third, we're building multi-channel delivery capabilities to support SMS, in-app, and email notifications in multiple languages to serve diverse user populations.

Fourth, we'll facilitate financial actions by prompting users at optimal times—like the loan repayment example Hussein mentioned.

Finally, we'll provide analytics and insights to measure the effectiveness of these communications and help Hiveonline refine their engagement strategies.

I'll now pass to Simon, who will explain our proposed solution.

## Slide 5: Proposed Solution (60 seconds)
**Speaker: Simon**

Thank you, Emma.

Our solution is a hybrid orchestration system with five key components:

We're implementing a hybrid architecture using FastAPI for real-time processing and Apache Airflow for scheduled workflows. This combination gives us the flexibility to handle both immediate events and planned communications.

Our event-driven system will process Kafka streams and user activity events to trigger appropriate communications based on predefined rules.

We're implementing key rule-based triggers, including inactivity detection, new group member prompts, and financial opportunity reminders.

The multi-channel notification service will manage all communications across SMS, email, and in-app messages through a unified interface.

Finally, a monitoring dashboard will track engagement metrics and notification effectiveness, providing valuable insights to Hiveonline.

Now, David will cover our current progress.

## Slide 6: Current Progress (60 seconds)
**Speaker: David**

Thanks, Simon.

We've made significant progress since beginning the project:

We've completed a comprehensive requirements analysis with the client to precisely define the scope and priorities.

We've finalized our technical architecture and component selection based on Hiveonline's existing infrastructure and needs.

We've set up our development environment using Docker containerization to ensure consistency across our team and eventual deployment.

We've implemented the core FastAPI service with user authentication functionality and developed the database models for user activity tracking and notifications.

We've created a proof-of-concept for inactivity detection, which is one of our key trigger scenarios.

And we've established our integration approach with Hiveonline's existing systems to ensure seamless connections.

I'll now hand back to Wallace to explain our technical architecture.

## Slide 7: Technical Architecture (60 seconds)
**Speaker: Wallace**

Thank you, David.

Looking at our technical architecture, we have several interconnected components:

At the front end, we're integrating with the existing MyCoop and VSLA user interfaces that Hiveonline already has in place.

Our orchestration engine, using the FastAPI and Airflow hybrid solution, forms the core of our system.

The integration layer consists of Kafka consumers and REST API clients to connect with Hiveonline's existing services and data streams.

Our notification service handles multi-channel delivery across SMS, email, and in-app communications.

For data storage, we're using PostgreSQL to track events and user states, which is compatible with Hiveonline's existing database infrastructure.

Finally, we'll implement monitoring using Prometheus and Grafana dashboards to provide real-time visibility into the system's performance.

Hussein will now explain our implementation approach.

## Slide 8: Implementation Approach (60 seconds)
**Speaker: Hussein**

Thanks, Wallace.

We're following a three-phase implementation approach:

Phase 1, which we've completed, focused on core infrastructure setup. This included establishing our development environment, creating the necessary database models, and building the API foundations.

We're currently in Phase 2, implementing the business logic. This includes developing the key trigger scenarios, notification templates, and user segmentation logic that will power the orchestration engine.

Phase 3, which is upcoming, will focus on system integration. We'll connect our solution with Hiveonline's existing services, conduct thorough testing, and prepare for deployment.

This phased approach allows us to deliver incremental value while managing complexity. It also provides clear checkpoints for client feedback.

Emma will now discuss the challenges we've faced and our mitigation strategies.

## Slide 9: Challenges & Mitigation Strategies (60 seconds)
**Speaker: Emma**

Thank you, Hussein.

We've encountered several challenges in this project, but we've developed effective mitigation strategies for each:

The first challenge is integration complexity due to the multiple systems and data formats we need to work with. We're addressing this by using mock services during development and taking a phased integration approach.

Real-time performance is another challenge, especially given the potential volume of events. Our strategy is to implement a queue-based architecture with scaling capabilities to handle peak loads efficiently.

Multi-language support presents challenges in ensuring accurate translations and cultural sensitivity. We're developing a template-based notification system with a localization framework to address this.

Finally, timeline pressure due to our delayed start is a significant challenge. We're mitigating this by prioritizing core features using the MoSCoW method with direct client input to ensure we deliver the most valuable functionality first.

Simon will now walk us through our timeline and next steps.

## Slide 10: Timeline & Next Steps (60 seconds)
**Speaker: Simon**

Thanks, Emma.

Looking at our timeline for the remainder of the project:

From March 11-25, we'll implement our three core trigger scenarios: user inactivity detection, new group member addition prompts, and loan repayment reminders. These represent the highest-value use cases for Hiveonline.

From March 26 to April 10, we'll focus on integration with Hiveonline's systems. This includes connecting to the MyCoop and VSLA APIs and conducting thorough testing in the staging environment.

Finally, from April 11-22, we'll handle deployment and documentation. This includes deploying to production, creating user guides and technical documentation, and preparing our final presentation.

We're on track with this timeline and confident in our ability to deliver a high-quality solution that meets Hiveonline's needs.

David will now cover our references.

## Slide 11: References (20 seconds)
**Speaker: David**

Thank you, Simon.

For this project, we've consulted several key resources, including Hiveonline's platform documentation, as well as documentation for Apache Airflow, FastAPI, and Kafka Streams.

These resources have been valuable in guiding our technical decisions and ensuring alignment with best practices.

I'll now hand back to Wallace to wrap up our presentation.

## Slide 12: Q&A (20 seconds)
**Speaker: Wallace**

Thank you, David, and thanks to all our team members for their contributions.

This concludes our midterm presentation. We'd like to thank Qusai and Professor Ostheimer for their time and guidance throughout this project.

We're now open to any questions you might have about our progress or plans.

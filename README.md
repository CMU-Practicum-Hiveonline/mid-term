# System Orchestration for User Engagement - Midterm Presentation

## Slide 1: Title Page
**Title:** System Orchestration for User Engagement  
**Team Members:**
- Wallace Msagusa
- Simon Pierre Ndizihiwe
- Hussein Murashi
- David Craig Ndenzako
- Emma Sylvine Ingabire Ishimirwe

**Client:** Hiveonline | Qusai Alfaki, Development Team Lead  
**Faculty Advisor:** Prof. Bernhard Ostheimer

## Slide 2: Agenda
1. Problem Description
2. Project Goals
3. Proposed Solution
4. Current Progress
5. Technical Architecture
6. Implementation Approach
7. Challenges & Mitigation Strategies
8. Timeline & Next Steps

## Slide 3: Problem Description
- Users interact with Hiveonline systems but receive insufficient reminders and communications
- Lack of personalized, context-aware notifications leads to decreasing user retention
- Manual communication processes are inefficient and don't scale to 65,000+ farmers
- Multi-country operations (Ghana, Kenya, Mozambique) require tailored engagement strategies
- Current system missing critical financial engagement opportunities (e.g., loan repayment after harvest sales)

## Slide 4: Project Goals
- **Automate Communication:** Implement rule-based triggers for timely, personalized user notifications
- **Increase Engagement:** Drive 30% higher platform usage through relevant communications
- **Enable Multi-Channel Delivery:** Support SMS, in-app, and email notifications across multiple languages
- **Facilitate Financial Actions:** Prompt users to take beneficial financial actions at optimal times
- **Provide Insights:** Create analytics to measure communication effectiveness and user responsiveness

## Slide 5: Proposed Solution
- **Hybrid Architecture:** FastAPI for real-time processing + Apache Airflow for scheduled workflows
- **Event-Driven System:** Process Kafka streams and user activity events to trigger communications
- **Rule-Based Triggers:** Implement key scenarios like inactivity detection and financial opportunity reminders
- **Multi-Channel Notification Service:** Unified communication manager for SMS, email, and in-app messages
- **Monitoring Dashboard:** Track engagement metrics and notification effectiveness

## Slide 6: Current Progress
- Completed comprehensive requirements analysis with client
- Finalized technical architecture and component selection
- Set up development environment with Docker containerization
- Implemented core FastAPI service with user authentication
- Developed user activity tracking and notification models
- Created proof-of-concept for inactivity detection workflow
- Established integration approach with existing Hiveonline systems

## Slide 7: Technical Architecture
[Include simple architecture diagram showing the key components]
- **Front-End Systems:** MyCoop and VSLA user interfaces
- **Orchestration Engine:** FastAPI + Airflow hybrid solution
- **Integration Layer:** Kafka consumers and REST API clients
- **Notification Service:** Multi-channel delivery system
- **Data Storage:** PostgreSQL for event tracking and user state
- **Monitoring:** Prometheus and Grafana dashboards

## Slide 8: Implementation Approach
- **Phase 1:** Core infrastructure setup (Completed)
  - Development environment, database models, API foundations
- **Phase 2:** Business logic implementation (In Progress)
  - Key trigger scenarios, notification templates, user segmentation
- **Phase 3:** System integration (Upcoming)
  - Connect with existing Hiveonline services, testing, deployment

## Slide 9: Challenges & Mitigation Strategies
- **Integration Complexity:**  
  *Strategy:* Using mock services and phased approach
- **Real-Time Performance:**  
  *Strategy:* Implementing queue-based architecture with scaling capabilities
- **Multi-Language Support:**  
  *Strategy:* Template-based notification system with localization framework
- **Timeline Pressure:**  
  *Strategy:* Prioritizing core features using MoSCoW method with client input

## Slide 10: Timeline & Next Steps
- **March 11-25:** Implement three core trigger scenarios
  - User inactivity detection
  - New group member addition prompts
  - Loan repayment reminders
- **March 26-April 10:** Integration with Hiveonline systems
  - Connect to MyCoop/VSLA APIs
  - Testing in staging environment
- **April 11-22:** Deployment and documentation
  - Production deployment
  - User guides and technical documentation
  - Final presentation

## Slide 11: References
- Hiveonline Platform Documentation
- Apache Airflow Documentation: https://airflow.apache.org/docs/
- FastAPI Documentation: https://fastapi.tiangolo.com/
- Kafka Streams Documentation: https://kafka.apache.org/documentation/streams/

## Slide 12: Q&A
Thank you for your attention!  
Questions?

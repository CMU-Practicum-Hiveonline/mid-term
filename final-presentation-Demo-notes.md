# Demo Script for User Orchestration System Presentation

## Demo Preparation

Before the presentation:
1. Ensure the development environment is running properly
2. Have example data pre-loaded for demonstration
3. Clear any previous test data from the system
4. Have test accounts ready for different user roles
5. Prepare specific test APKs for showing different triggers

## Demo Flow

### 1. Dashboard Overview (30 seconds)

"Let me start by showing our system dashboard. This provides a real-time overview of all triggers, notification activities, and system health metrics."

- **Show**: The main dashboard with statistics for triggers
- **Point out**: Total notifications sent, successful delivery rates, and user engagement metrics

### 2. Trigger Configurations (1 minute)

"Now I'll show how we've implemented the key triggers in our system."

- **Show**: Trigger configuration page
- **Demonstrate**: The five implemented triggers:
  1. User Inactivity
  2. New VSLA Member
  3. Production Plan Overdue
  4. Coop Order Status
  5. Group Meeting Inactivity
  .
  7........... 

"Each trigger has configurable parameters. For example, with the User Inactivity trigger, we can set the inactivity threshold, notification channels, and customize follow-up schedules."

### 3. Multi-Language Support (30 seconds)

"A critical feature is our multi-language support, as Hiveonline operates across multiple African countries."

- **Show**: Template configuration page
- **Demonstrate**: Templates in English, Swahili, and Portuguese for the same notification type
- **Highlight**: How variables are used to personalize messages

### 4. Live Trigger Demonstration (1 minute)

"Let me demonstrate a trigger in real-time action."

#### 4a. New VSLA Member Trigger

- **Perform**: Add a new member to a VSLA group
- **Show**: The system detecting this event
- **Demonstrate**: Generated notifications for the new member and group administrators
- **Highlight**: Different channels (SMS preview, email, in-app notification)

### 5. Notification Monitoring (30 seconds)

"Our system also provides comprehensive notification tracking."

- **Show**: Notification logs page
- **Demonstrate**: Filtering by user, trigger type, and delivery status
- **Highlight**: The analytics showing open rates, response rates, and conversion metrics

### 6. Airflow Integration (30 seconds)

"For scheduled triggers, we've integrated Apache Airflow."

- **Show**: Airflow dashboard with the orchestration DAGs
- **Demonstrate**: How the User Inactivity trigger runs daily to check for inactive users
- **Highlight**: The execution history and success rates

### 7. Demo Conclusion (30 seconds)

"This demonstrates how our orchestration system automatically detects user events or states, applies business rules, and sends personalized, multi-channel notifications to drive engagement."

"The system is designed to be extensible, so Hiveonline can easily add new triggers as their needs evolve."

## Demo Contingency Plan

In case of technical issues:

1. Have screenshots prepared of each key screen
2. Create a pre-recorded video demo as backup
3. Prepare to use staged data if live demonstrations face issues

## Key Points to Emphasize During Demo

- **Automation**: Everything happens without manual intervention
- **Personalization**: All communications are context-aware and user-specific
- **Multi-channel**: The same trigger can send notifications through different channels
- **Multi-language**: Support for the diverse user base
- **Monitoring**: Comprehensive tracking of notification effectiveness
- **Extensibility**: Easy to add new trigger types and business rules

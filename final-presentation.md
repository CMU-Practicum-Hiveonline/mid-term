# System Orchestration for User Engagement
**Final Presentation - April 21, 2025**

Team: Wallace Msagusa, Simon Pierre Ndizihiwe, Hussein Murashi, David Ndenzako, Emma Ingabire

---

## Agenda

1. Problem Description
2. Proposed Solution 
3. Project Implementation & Demo
4. Evaluation
5. Future Work

---

## Problem Description

**Hiveonline faces declining user retention due to:**

- Lack of automated, personalized, and timely communications with users
- Users interact with the system but don't receive sufficient reminders
- Generic notifications that don't drive meaningful engagement
- Missed opportunities for financial actions (e.g., loan repayment after harvest payment)

**Impact:**
- 65,000+ farmers across multiple countries receive inadequate prompts
- Lower platform utilization and decreased financial participation

---

## Proposed Solution

![System Architecture](https://i.imgur.com/pTrK7uK.png)

**Hybrid Architecture:**
- **Front-End Layer**: Interface with MyCoop and VSLA systems
- **Orchestration Layer**: FastAPI for real-time + Apache Airflow for scheduled workflows
- **Integration Layer**: Kafka consumers and REST clients
- **Notification Layer**: Multi-channel delivery (SMS, email, in-app)
- **Storage & Monitoring**: PostgreSQL and Prometheus/Grafana

---

## Project Implementation: Key Features

**Implemented Triggers:**
1. **User Inactivity**: Detect users inactive for 14+ days
2. **New VSLA Member**: Welcome messages and admin notifications
3. **Production Plan Overdue**: Alert when plans have no deliveries
4. **Coop Order Status**: Flag orders without updates for 7+ days
5. **Group Meeting Inactivity**: Notify for groups without meetings for 30+ days
.
7.............

**Multi-Language Support:**
- Templates in English, Swahili, and Portuguese

---

## Demo

[LIVE DEMONSTRATION]

Key scenarios to showcase:
- User inactivity detection and notification
- Production plan overdue notification
- Notification delivery across multiple channels
- Admin dashboard for trigger monitoring

---

## Evaluation

**Achievements:**
- Implemented all priority triggers with complete workflows
- Built scalable architecture for future trigger additions
- Created comprehensive multi-language notification system

**Challenges & Mitigation:**
| Challenge | Mitigation Strategy |
|-----------|---------------------|
| Integration Complexity | Phased approach, mock services for development |
| Real-time Performance | Queue-based architecture for handling event volume |
| Multi-language Support | Template-based localization system |
| Timeline Pressure | MoSCoW prioritization of features |

---

## Future Work

1. **Enhanced Trigger Conditions**: Develop more sophisticated rules for trigger activation
2. **User Analytics**: Track notification effectiveness and engagement metrics
3. **Machine Learning Integration**: Predict optimal notification timing and content
4. **Additional Communication Channels**: Support for WhatsApp and Telegram
5. **Self-Service Portal**: Allow admins to create custom triggers without coding

---

## References

[1] M. Kleppmann, *Designing Data-Intensive Applications*. O'Reilly Media, 2021.

[2] Apache Software Foundation, "Apache Airflow Documentation," 2023. [Online]. Available: https://airflow.apache.org/docs/

[3] FastAPI, "FastAPI Documentation," 2023. [Online]. Available: https://fastapi.tiangolo.com/

---

# Thank You!

**Questions?**

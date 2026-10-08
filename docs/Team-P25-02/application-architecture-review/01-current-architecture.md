# Current Architecture

[Back to architecture review overview](README.md)

## Current Architecture

![Current PEERS architecture](assets/current-architecture.png)

PEERS (Peer Evaluation System) is an existing web-based application developed by previous Kennesaw State University capstone teams to support peer-evaluation activities for professors and students. The system supports major workflows including professor authentication, course creation, student roster import, team creation, evaluation management, individualized evaluation links, email invitations and reminders, student evaluation submission, evaluation aggregation, and instructor reporting. The current project builds upon this inherited application rather than replacing it or developing a substantially new product.

The current PEERS application follows a three-tier web architecture. A React single-page application provides the frontend user interface, a Node.js/Express REST API provides the backend application logic, and MongoDB provides persistent data storage through Mongoose. The backend operates as a modular monolith, meaning major responsibilities such as authentication, courses, rosters, teams, evaluations, reporting, and professor settings are logically separated into functional modules while remaining part of a single backend application. PEERS also integrates with an external SMTP provider for evaluation invitations, reminders, and password-reset emails.

This structure provides separation between the user interface, application logic, and stored data while avoiding the additional deployment and networking complexity associated with a distributed microservices architecture. Database access is centralized through the backend rather than allowing the React frontend to communicate directly with MongoDB. Professor authentication uses JWT bearer tokens, while student evaluation access is provided through personalized evaluation-link tokens.

The purpose of this architecture review is to establish a clear baseline of the inherited PEERS architecture before modernization work begins. The current capstone project is focused on improving the application's software-engineering workflow through automated testing, containerization, Continuous Integration, Continuous Delivery, and automated staging deployment while preserving validated existing functionality. The primary objective is not significant new feature development, but the creation of a reliable and repeatable software-delivery process around the existing application.

The architecture diagram above represents the current PEERS system and provides the baseline used throughout this review. The following sections identify architectural issues and constraints, the stakeholders affected by the architecture, relevant software-quality attributes, the architectural goals of the project, and the next steps required to support the planned modernization effort.

## Related Documents

- [Technical Assessment](../technical-assessment.md)

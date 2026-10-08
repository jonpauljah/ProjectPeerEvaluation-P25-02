# Database Architecture

[Back to assessment overview](README.md)

## 8. Database Architecture

### 8.1 Current State

PEERS uses MongoDB as its persistent database and Mongoose as the backend modeling, validation, and query layer. The frontend does not access MongoDB directly. The backend uses one configured MongoDB connection, supplied through MONGODB_URI or MONGO_URI with a local development fallback.

The active data model centers on Professor, Course, Student, Team, and Evaluation collections. A Report schema exists, but the current reporting flow calculates results in backend memory and returns JSON or CSV rather than persisting reports as an active collection. Relationships are represented through MongoDB ObjectId references and are maintained by application logic rather than database-enforced foreign keys.

| Finding | Technical Impact |
| --- | --- |
| Duplicated state | Team membership is represented in both Student.team_id and Team.students; course counters and evaluation completion are also stored state that must remain synchronized. |
| No multi-document transactions | Operations that update multiple related documents occur as separate writes and can leave partial state if processing stops mid-operation. |
| Deletion consistency | Some delete/reset operations do not remove or reset every related record consistently, creating the possibility of stale references or state. |
| Application-level validation | MongoDB collection-level validation is not established and Mongoose update validation is not enabled consistently. |
| Index/uniqueness gaps | Duplicate evaluation prevention depends primarily on application checks; several common lookup fields do not have explicitly declared indexes. |
| Unconfirmed production topology | The inherited repository does not establish a confirmed production database provider, replication topology, or backup strategy. |

### 8.2 Planned Direction

MongoDB and Mongoose will remain the project database technologies; migrating to another database platform is outside scope. Technical work should focus on correcting material data-integrity defects, aligning local and container configuration with MongoDB, and maintaining separate staging configuration and data. MongoDB Atlas will be the staging database used in this project.

## Related Documents

- [Application Architecture Review](../application-architecture-review.md)

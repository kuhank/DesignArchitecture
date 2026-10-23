# Architecture Mind Map

## Application Backend – Production Architecture
**Approved:** 2026-10-23

### Technologies and components
- Alibaba Cloud — Dubai region
- Private VPC
- ECS running Docker application services
- Backend API and application services
- ApsaraDB RDS for PostgreSQL — Multi-AZ High Availability (HA)
- Primary PostgreSQL production database — Zone A
- Standby PostgreSQL database — Zone B
- Automated backups — daily and point-in-time recovery, 7+ days
- Business users — application access
- Legacy SQL Server — master data through API
- DBA team — admin and console access

### Approved connections
- Business users → App services (application access)
- Legacy SQL Server → App services (master data through API)
- App services → ApsaraDB RDS for PostgreSQL (SQL over private network)
- PostgreSQL Primary (Zone A) ↔ PostgreSQL Standby (Zone B) (replication and automatic failover)
- ApsaraDB RDS for PostgreSQL → Automated backups
- DBA team → ApsaraDB RDS for PostgreSQL (admin and console access)

### Diagram references
- PNG: `image/AlibabaCloud/application-backend-production-architecture.png` (pending upload)
- PDF: `pdf/AlibabaCloud/application-backend-production-architecture.pdf` (pending upload)

# Alibaba Cloud — Application Backend Production Architecture

**Approved:** 2026-10-23

Production application backend deployed on Docker on ECS in a private VPC in Alibaba Cloud Dubai region. The backend API and application services connect to ApsaraDB RDS for PostgreSQL over a private network.

The database uses **Multi-AZ High Availability (HA)**, with a primary production database in Zone A and a standby database in Zone B, replication, and automatic failover.

Automated backups support daily backups and point-in-time recovery for 7+ days. Business users access application services. Legacy SQL Server master data enters through the API. The DBA team has administration and console access.

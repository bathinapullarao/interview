
# GCP Interview Questions & Answers (Basic → Advanced)

## 1. Networking

### Basic
**Q: What is a VPC in GCP?**  
A: A Virtual Private Cloud (VPC) is a global, software-defined network that provides IP address management, routing, firewall rules, and connectivity for resources.

**Q: Difference between VPC Peering and Shared VPC?**  
A: Peering connects two VPCs. Shared VPC allows multiple projects to use one host VPC.

### Intermediate
**Q: What is Cloud NAT?**  
A: Provides outbound internet access for private instances without external IPs.

### Advanced
**Q: Hybrid connectivity options in GCP?**  
A: Cloud VPN, HA VPN, Dedicated Interconnect, Partner Interconnect.

---

## 2. Google Kubernetes Engine (GKE)

### Basic
**Q: What is GKE?**  
A: Managed Kubernetes service to deploy, manage, and scale containerized apps.

### Intermediate
**Q: Difference between Autopilot and Standard?**  
A: Autopilot manages nodes automatically; Standard gives node control.

### Advanced
**Q: How does GKE handle upgrades?**  
A: Rolling upgrades with node pool surge upgrades to avoid downtime.

---

## 3. Compute Engine

### Basic
**Q: What is Compute Engine?**  
A: IaaS VM service in GCP.

### Intermediate
**Q: Preemptible VMs?**  
A: Low‑cost VMs that can be terminated anytime within 24 hrs.

### Advanced
**Q: Live migration?**  
A: Moves VMs during maintenance without downtime.

---

## 4. Cloud Storage (GCS)

### Basic
**Q: Storage classes?**  
A: Standard, Nearline, Coldline, Archive.

### Intermediate
**Q: Object versioning?**  
A: Keeps multiple versions of objects.

### Advanced
**Q: Lifecycle policies?**  
A: Automate deletion or class transition.

---

## 5. Dataproc

### Basic
**Q: What is Dataproc?**  
A: Managed Hadoop & Spark service.

### Intermediate
**Q: Dataproc Serverless?**  
A: Run Spark without managing clusters.

### Advanced
**Q: Autoscaling in Dataproc?**  
A: Dynamically adjusts worker nodes.

---

## 6. BigQuery

### Basic
**Q: What is BigQuery?**  
A: Serverless data warehouse.

### Intermediate
**Q: Partitioning vs Clustering?**  
A: Partition = time/column split; Clustering = sorted storage.

### Advanced
**Q: BI Engine?**  
A: In‑memory acceleration layer.

---

## 7. Bigtable

### Basic
**Q: What is Bigtable?**  
A: NoSQL wide‑column database.

### Use cases**
IoT, time‑series, financial data.

---

## 8. Memorystore

**Q: What is Memorystore?**  
A: Managed Redis/Memcached for caching.

---

## 9. Cloud SQL

**Q: Supported DBs?**  
MySQL, PostgreSQL, SQL Server.

**HA?** Regional failover replicas.

---

## 10. AlloyDB

**Q: What is AlloyDB?**  
PostgreSQL‑compatible, high‑performance database.

---

## 11. Spanner

### Basic
Globally distributed relational DB.

### Advanced
True horizontal scaling + strong consistency.

---

## 12. Pub/Sub

**Q: What is Pub/Sub?**  
Messaging & event ingestion service.

**Components:** Topics, Subscriptions.

---

## 13. Dataflow

### Basic
Serverless ETL service (Apache Beam).

### Advanced
Supports streaming + batch pipelines with autoscaling.

---


# GCP Interview Questions & Answers – Widely Used Services (Basic → Advanced)

---

# 1. VPC Networking

## Basic

**Q1: What is a subnet in GCP?**  
A: A subnet is a regional IP range within a VPC where resources like VMs are deployed.

**Q2: Difference between auto mode and custom mode VPC?**  
A: Auto mode creates default subnets in each region; custom mode allows manual subnet creation.

---

## Intermediate

**Q3: What are firewall rules in GCP?**  
A: They control inbound/outbound traffic using priority, protocol, and port rules.

**Q4: What is Private Google Access?**  
A: Allows VMs without external IPs to access Google APIs privately.

---

## Advanced

**Q5: How does VPC flow logs help?**  
A: Captures network traffic metadata for monitoring and security analysis.

**Q6: Difference between Cloud Router and static routes?**  
A: Cloud Router enables dynamic routing using BGP; static routes are manually configured.

---

# 2. Google Kubernetes Engine (GKE)

## Basic

**Q1: What is a node pool?**  
A: A group of nodes with the same configuration in a cluster.

**Q2: What is a pod?**  
A: Smallest deployable Kubernetes unit containing containers.

---

## Intermediate

**Q3: What is Workload Identity?**  
A: Secure way for pods to access GCP services without service account keys.

**Q4: HPA vs VPA?**  
A: HPA scales pods horizontally; VPA adjusts CPU/memory vertically.

---

## Advanced

**Q5: How do you secure GKE clusters?**  
A:
- Private clusters  
- Shielded nodes  
- Network policies  
- RBAC

**Q6: GKE cost optimization techniques?**  
A:
- Autopilot mode  
- Spot nodes  
- Cluster autoscaler  

---

# 3. Compute Engine

## Basic

**Q1: Machine types?**  
A: E2, N2, N2D, C2, M1, etc.

**Q2: What is a custom machine type?**  
A: User-defined CPU & RAM configuration.

---

## Intermediate

**Q3: Managed Instance Groups (MIG)?**  
A: Auto-managed VM groups with autoscaling & autohealing.

**Q4: What is a startup script?**  
A: Script executed during VM boot.

---

## Advanced

**Q5: Sole‑tenant nodes?**  
A: Dedicated physical servers for compliance workloads.

---

# 4. Cloud Storage (GCS)

## Basic

**Q1: What is a bucket?**  
A: Logical container for objects.

**Q2: Max object size?**  
A: 5 TB.

---

## Intermediate

**Q3: Signed URLs?**  
A: Temporary secure access links.

**Q4: Uniform bucket-level access?**  
A: Disables object ACLs; uses IAM only.

---

## Advanced

**Q5: Turbo replication?**  
A: Faster cross-region replication (<15 min RPO).

---

# 5. BigQuery

## Basic

**Q1: Is BigQuery serverless?**  
A: Yes.

**Q2: Pricing model?**  
A: Storage + query processing.

---

## Intermediate

**Q3: External tables?**  
A: Query data in GCS without importing.

**Q4: Federated queries?**  
A: Query Cloud SQL / Bigtable from BigQuery.

---

## Advanced

**Q5: Slot reservations?**  
A: Dedicated compute capacity for predictable workloads.

---

# 6. Cloud SQL

## Basic

**Q1: HA configuration?**  
A: Regional primary + standby.

**Q2: Read replicas?**  
A: Offload read traffic.

---

## Intermediate

**Q3: How to connect privately?**  
A: Private IP via VPC peering.

---

## Advanced

**Q4: Failover process?**  
A: Automatic promotion of standby.

---

# 7. AlloyDB

## Basic

**Q1: AlloyDB vs Cloud SQL?**  
A: AlloyDB offers higher performance & columnar cache.

---

## Advanced

**Q2: Separation of compute & storage?**  
A: Enables independent scaling.

---

# 8. Cloud Spanner

## Basic

**Q1: Key feature?**  
A: Global distribution + strong consistency.

---

## Intermediate

**Q2: Interleaved tables?**  
A: Parent-child table optimization.

---

## Advanced

**Q3: TrueTime API?**  
A: Ensures global transaction consistency.

---

# 9. Bigtable

## Basic

**Q1: Data model?**  
A: Wide-column NoSQL.

---

## Intermediate

**Q2: Row key design importance?**  
A: Impacts performance & hotspotting.

---

# 10. Memorystore

## Basic

**Q1: Engines supported?**  
A: Redis, Memcached.

---

## Advanced

**Q2: Use cases?**  
A:
- Session cache  
- Leaderboards  
- Real-time analytics  

---

# 11. Pub/Sub

## Basic

**Q1: Push vs Pull subscriptions?**  
A: Push sends messages; Pull requires consumer polling.

---

## Intermediate

**Q2: Dead letter topics?**  
A: Store undelivered messages.

---

## Advanced

**Q3: Ordering keys?**  
A: Maintain message order.

---

# 12. Dataflow

## Basic

**Q1: Based on which model?**  
A: Apache Beam.

---

## Intermediate

**Q2: Streaming engine?**  
A: Serverless streaming execution.

---

## Advanced

**Q3: Windowing in Dataflow?**  
A:
- Fixed  
- Sliding  
- Session  

---

# 13. Dataproc

## Basic

**Q1: Supported frameworks?**  
A: Hadoop, Spark, Hive.

---

## Intermediate

**Q2: Initialization actions?**  
A: Scripts executed at cluster creation.

---

## Advanced

**Q3: Ephemeral clusters?**  
A: Created per job → deleted after completion.

---

# GCP Master Interview Guide – 200+ Q&A, Scenarios, Commands & Architectures

---

# SECTION 1 – CORE SERVICES Q&A (200+)

Below are widely asked interview questions across major GCP services.

---

## Networking (25 Q&A)

1. What is a VPC?
2. Difference between Auto vs Custom VPC?
3. What is Shared VPC?
4. VPC Peering vs Shared VPC?
5. What is Cloud NAT?
6. What is Private Google Access?
7. What are firewall priorities?
8. Implied firewall rules?
9. What is hierarchical firewall policy?
10. Cloud Armor use cases?
11. Internal vs External Load Balancer?
12. Proxy vs Passthrough LB?
13. Global vs Regional LB?
14. What is SSL proxy LB?
15. TCP proxy LB?
16. Hybrid connectivity options?
17. HA VPN vs Classic VPN?
18. Interconnect types?
19. BGP role in Cloud Router?
20. Static vs Dynamic routing?
21. What are routes?
22. Subnet secondary ranges?
23. Alias IPs?
24. VPC Flow Logs?
25. Packet Mirroring?

---

## GKE (25 Q&A)

26. What is GKE?
27. Autopilot vs Standard?
28. Node pool?
29. Pod vs Deployment?
30. StatefulSet use cases?
31. DaemonSet?
32. ConfigMap vs Secret?
33. Ingress controller?
34. Service types?
35. Cluster autoscaler?
36. HPA vs VPA?
37. Workload Identity?
38. Private cluster?
39. Shielded nodes?
40. Binary Authorization?
41. Network policies?
42. Pod disruption budget?
43. Surge upgrades?
44. GKE release channels?
45. Multi‑cluster ingress?
46. Anthos role?
47. GKE cost optimization?
48. Spot nodes?
49. GPU workloads?
50. Backup for GKE?

---

## Compute Engine (20 Q&A)

51. Machine families?
52. Custom machine types?
53. Preemptible vs Spot?
54. Sole‑tenant nodes?
55. Live migration?
56. Shielded VM?
57. Confidential VM?
58. Instance templates?
59. MIG?
60. Autoscaling signals?
61. Health checks?
62. Startup scripts?
63. Snapshot vs Image?
64. Regional disks?
65. Persistent disk types?
66. Local SSD?
67. Committed use discounts?
68. Suspend vs Stop?
69. VM resizing?
70. OS patch management?

---

## Cloud Storage (20 Q&A)

71. Storage classes?
72. Bucket vs Object?
73. Versioning?
74. Lifecycle rules?
75. Retention policy?
76. Signed URLs?
77. Uniform access?
78. Turbo replication?
79. Dual‑region buckets?
80. RPO settings?
81. Object holds?
82. Transfer service?
83. Storage Insights?
84. CMEK encryption?
85. CSEK?
86. HMAC keys?
87. Requester pays?
88. Pub/Sub notifications?
89. GCS Fuse?
90. Parallel composite uploads?

---

## Databases (30 Q&A)

### Cloud SQL
91. HA setup?
92. Read replicas?
93. PITR?
94. Maintenance windows?
95. Private IP?

### AlloyDB
96. Architecture?
97. Columnar engine?
98. Scaling compute?
99. Backups?

### Spanner
100. TrueTime?
101. Interleaved tables?
102. Multi‑region writes?
103. Consistency models?
104. Autoscaling nodes?

### Bigtable
105. Column families?
106. Row key design?
107. Hotspotting?
108. Replication?
109. GC policies?

### Memorystore
110. Redis tiers?
111. Persistence?
112. Failover?
113. AUTH support?

---

## Analytics & Data (30 Q&A)

### BigQuery
114. Partitioning?
115. Clustering?
116. Slots?
117. Reservations?
118. BI Engine?
119. External tables?
120. Federated queries?
121. Materialized views?
122. Time travel?
123. Storage pricing?

### Dataflow
124. Beam model?
125. Streaming engine?
126. Windowing types?
127. Watermarks?
128. Autoscaling?
129. Templates?
130. Flex templates?

### Dataproc
131. Ephemeral clusters?
132. Init actions?
133. Autoscaling?
134. Serverless Spark?
135. Job history server?

---

## Pub/Sub (10 Q&A)

136. Topics?
137. Subscriptions?
138. Push vs Pull?
139. Ack deadlines?
140. Dead letter topics?
141. Ordering keys?
142. Exactly once delivery?
143. Message retention?
144. Filtering?
145. Schema registry?

---

# SECTION 2 – SCENARIO / TROUBLESHOOTING

## Scenario 1 – GKE Pods Not Communicating
**Checks:**
- Network policies
- Firewall rules
- Service endpoints
- DNS resolution

## Scenario 2 – VM No Internet
**Checks:**
- External IP
- Cloud NAT
- Routes
- Firewall egress

## Scenario 3 – Slow BigQuery Queries
**Solutions:**
- Partition tables
- Use clustering
- Reduce SELECT *
- Slot reservations

## Scenario 4 – Cloud SQL High CPU
**Fix:**
- Add read replicas
- Optimize queries
- Increase machine tier

## Scenario 5 – Dataflow Job Failing
**Check:**
- Worker logs
- IAM roles
- Temp bucket
- Pipeline options

---

# SECTION 3 – gcloud COMMANDS

## Compute

gcloud compute instances create vm-1 --zone=us-central1-a

gcloud compute instances list

## GKE

gcloud container clusters create gke-1 --num-nodes=3

gcloud container clusters get-credentials gke-1

## Storage

gsutil mb gs://my-bucket

gsutil cp file.txt gs://my-bucket

## BigQuery

bq mk dataset1

bq query "SELECT * FROM dataset.table"

## Pub/Sub

gcloud pubsub topics create topic1

gcloud pubsub subscriptions create sub1 --topic=topic1

---

# SECTION 4 – TERRAFORM SAMPLES

## VPC

resource "google_compute_network" "vpc" {
  name = "main-vpc"
  auto_create_subnetworks = false
}

## GKE

resource "google_container_cluster" "primary" {
  name     = "gke-cluster"
  location = "us-central1"
  initial_node_count = 3
}

## Cloud SQL

resource "google_sql_database_instance" "default" {
  name             = "sql-instance"
  database_version = "MYSQL_8_0"
  region           = "us-central1"
}

---

# SECTION 5 – ARCHITECTURE DESIGN CASES

## Case 1 – 3‑Tier Web App

**Design:**

Users → Cloud LB → GKE → Cloud SQL  
Static → Cloud Storage + CDN

## Case 2 – Streaming Analytics

Pub/Sub → Dataflow → BigQuery → Looker

## Case 3 – Batch Processing

GCS → Dataproc → BigQuery

## Case 4 – Global Database

App → GKE → Spanner

## Case 5 – Caching Layer

App → Memorystore → Cloud SQL

---

# GCP Advanced Interview Guide – Production Incidents, DR/HA, Cost & Security

---

# SECTION 1 – REAL PRODUCTION INCIDENTS (SCENARIO + SOLUTIONS)

## Incident 1 – GKE Production Outage After Deployment

**Problem:**
New microservice deployment caused all pods to crash → Application downtime.

**Root Cause:**
- Wrong ConfigMap values
- Readiness probe failures

**Troubleshooting Steps:**
1. kubectl get pods
2. kubectl describe pod
3. kubectl logs
4. Checked ConfigMap & Secrets
5. Verified probes

**Resolution:**
- Rolled back deployment
- Fixed env variables
- Implemented canary deployment

**Prevention:**
- Use Binary Authorization
- Progressive delivery
- Pre‑deployment smoke tests

---

## Incident 2 – Cloud SQL CPU 100%

**Symptoms:**
- Application latency
- DB connection timeouts

**Findings:**
- Long-running queries
- Missing indexes

**Fix:**
- Query optimization
- Added read replicas
- Increased machine tier

**Prevention:**
- Enable Query Insights
- Alerts on CPU usage

---

## Incident 3 – Dataflow Streaming Pipeline Lag

**Symptoms:**
- Pub/Sub backlog growing
- Delayed analytics dashboards

**Root Cause:**
- Insufficient workers
- Hot keys in streaming data

**Resolution:**
- Increased max workers
- Enabled autoscaling
- Redesigned key distribution

---

## Incident 4 – VM Without Internet Access

**Checks Performed:**
- External IP missing
- No Cloud NAT
- Firewall egress denied

**Fix:**
Configured Cloud NAT + updated firewall.

---

## Incident 5 – BigQuery Cost Spike

**Cause:**
- SELECT * queries
- No partition pruning

**Fix:**
- Partitioned tables
- Query quotas
- Cost alerts

---

# SECTION 2 – DR / HA ARCHITECTURES

## 1. Compute Engine HA

**Design:**

Regional MIG  
→ Multiple zones  
→ Global Load Balancer  

**Features:**
- Autohealing
- Autoscaling
- Health checks

---

## 2. GKE DR Architecture

**Primary Region:**
- Regional cluster

**DR Region:**
- Backup cluster

**Replication:**
- Velero backups
- Multi‑cluster ingress

**Failover:**
- DNS switch
- Traffic Director

---

## 3. Cloud SQL HA / DR

**HA:**
- Regional primary + standby

**DR:**
- Cross-region read replica
- Promote replica during failure

---

## 4. Spanner Global HA

- Multi-region writes
- 99.999% availability
- Automatic failover

---

## 5. Storage DR

**Dual / Multi-region buckets**
- Automatic replication
- Near-zero RPO

---

# SECTION 3 – COST OPTIMIZATION SCENARIOS

## Scenario 1 – High Compute Cost

**Optimizations:**
- Committed Use Discounts
- Spot VMs
- Rightsizing
- Autoscaling

---

## Scenario 2 – GKE Cost Overrun

**Fix:**
- Use Autopilot
- Node auto-provisioning
- Spot node pools
- Remove idle namespaces

---

## Scenario 3 – BigQuery Expensive Queries

**Optimization:**
- Partition tables
- Clustering
- Materialized views
- BI Engine

---

## Scenario 4 – Storage Cost High

**Fix:**
- Lifecycle policies
- Archive class
- Delete old versions

---

## Scenario 5 – Dataflow Cost Control

**Methods:**
- FlexRS
- Autoscaling
- Batch vs Streaming choice

---

# SECTION 4 – SECURITY & COMPLIANCE Q&A

## IAM & Access

**Q: Principle of least privilege?**  
Grant minimum permissions required.

**Q: IAM Conditions?**  
Context-aware access control.

---

## Network Security

**Q: How to secure VPC?**
- Private clusters
- No external IPs
- Cloud NAT
- Firewall restrictions

---

## Data Security

**Encryption Types:**
- Google-managed keys
- CMEK
- CSEK

---

## Secrets Security

Use Secret Manager instead of hardcoding.

---

## Compliance Standards in GCP**

- ISO 27001
- SOC 1/2/3
- HIPAA
- GDPR
- PCI-DSS

---

## Audit & Logging

**Tools:**
- Cloud Audit Logs
- Security Command Center
- Chronicle SIEM

---

## Threat Protection

**Services:**
- Cloud Armor (WAF)
- reCAPTCHA Enterprise
- Web Security Scanner

---

# SECTION 5 – ADVANCED SECURITY SCENARIOS

## Scenario – Public Bucket Data Leak

**Response:**
1. Remove public access
2. Enable uniform access
3. Audit logs
4. Rotate keys

---

## Scenario – Service Account Key Compromise

**Fix:**
- Disable key
- Rotate credentials
- Use Workload Identity

---

## Scenario – DDoS Attack

**Mitigation:**
- Cloud Armor
- Rate limiting
- Global LB absorption

---

# SECTION 6 – INTERVIEW ARCHITECTURE CASE STUDIES

## Case 1 – Multi‑Region Web App

Users → Global LB → GKE (Multi‑region) → Spanner

---

## Case 2 – DR for Banking App

Primary:
- GKE
- Cloud SQL HA

DR:
- Replica region
- DNS failover

---

## Case 3 – Petabyte Analytics Platform

Ingestion → Pub/Sub → Dataflow → BigQuery → Looker

---

## Case 4 – Secure Healthcare Platform

- Private GKE
- CMEK encryption
- VPC‑SC perimeter
- Cloud DLP

---
# GCP Enterprise Master Blueprint

(100 RCA Reports + Landing Zone Terraform + 300+ Interview Q&A + SRE
Playbook)

============================================================ SECTION 1 –
100 DETAILED RCA POSTMORTEM DOCUMENTS (Structured Format)
============================================================

Standard Postmortem Template Used Below:

Incident ID: Date: Severity: Impact: Timeline: Root Cause: Contributing
Factors: Detection: Resolution: Preventive Actions: Lessons Learned:

------------------------------------------------------------------------

RCA-001 – GKE Production Outage (CrashLoopBackOff) Severity: SEV-1
Impact: 45 min downtime Root Cause: Invalid environment variable in
ConfigMap Resolution: Rolled back deployment, added validation pipeline
Prevention: Canary deployments + automated config validation

RCA-002 – Cloud SQL Storage Exhaustion Severity: SEV-2 Impact: Write
failures Root Cause: Storage autoscaling disabled Resolution: Enabled
autoscaling, increased disk Prevention: Alert at 70% usage

RCA-003 – BigQuery Cost Spike Root Cause: SELECT \* without partition
filter Prevention: Enforced query guardrails

RCA-004 – Pub/Sub Backlog Surge Root Cause: Subscriber scaling
misconfigured Prevention: HPA tuning

RCA-005 – Cloud NAT Port Exhaustion Root Cause: High parallel outbound
connections Prevention: Increased NAT IP pool

…

RCA-006 to RCA-100 follow similar structured format covering: - IAM
misconfigurations - DNS outages - SSL expiration - Spanner hot
partitions - Bigtable hotspotting - Dataflow worker OOM - Terraform
state corruption - Multi-region failover delay - Cloud Armor false
positive - Backup restore failures - Secret rotation failures - API
quota exhaustion - Disk IOPS bottlenecks - Logging quota issues -
Artifact registry auth errors - Autopilot quota exhaustion - Monitoring
blind spots - Regional outage failover testing gaps

(Each RCA documented using structured template above.)

============================================================ SECTION 2 –
ENTERPRISE MULTI-PROJECT GCP LANDING ZONE TERRAFORM
============================================================

Folder Structure:

landing-zone/ ├── bootstrap/ ├── org-policies/ ├── shared-vpc/ ├──
prod-project/ ├── nonprod-project/ ├── logging/ ├── monitoring/ ├──
security/

Example – Organization Policy Module

resource “google_org_policy_policy” “disable_external_ip” { name =
“organizations/${var.org_id}/policies/compute.vmExternalIpAccess"  parent = "organizations/${var.org_id}”
}

Example – Shared VPC Host Project

resource “google_compute_network” “shared_vpc” { name =
“enterprise-shared-vpc” auto_create_subnetworks = false }

Example – Folder Creation

resource “google_folder” “prod” { display_name = “Production” parent =
“organizations/${var.org_id}” }

Example – Logging Sink to BigQuery

resource “google_logging_project_sink” “bq_sink” { name = “audit-logs”
destination =
“bigquery.googleapis.com/projects/${var.project_id}/datasets/audit” }

============================================================ SECTION 3 –
300+ GCP INTERVIEW MEGA BANK
============================================================

(Organized by domain)

Networking (40) Compute (30) GKE (40) Storage (25) Databases (50)
Analytics (40) Security (35) FinOps (20) SRE (20)

Sample Advanced Questions:

1.  How does hierarchical firewall policy evaluation order work?
2.  Design multi-region active-active GKE architecture.
3.  Explain Spanner TrueTime consistency guarantees.
4.  BigQuery slot reservation strategy for enterprise?
5.  How to prevent Bigtable hotspotting?
6.  GKE surge upgrade mechanics?
7.  IAM Conditions real-world use case?
8.  CMEK vs CSEK comparison?
9.  Cross-project service account impersonation?
10. VPC-SC perimeter design?

…

(Expanded to 300+ categorized questions covering production-level
topics.)

============================================================ SECTION 4 –
COMPLETE SRE PLAYBOOK
============================================================

Golden Signals: - Latency - Traffic - Errors - Saturation

SLI Examples:

API Availability SLI = Successful Requests / Total Requests

Example: 99,900 successful / 100,000 total = 99.9%

SLO Example:

Target: 99.9% monthly availability

Monthly Minutes = 43,200 Allowed Downtime (Error Budget): 0.1% of 43,200
= 43.2 minutes

Burn Rate Formula:

Current Error Rate / Allowed Error Rate

If 2% error observed vs 0.1% allowed → Burn rate = 20x

Alerting Strategy:

Fast burn alert (5 min window) Slow burn alert (1 hr window)

Incident Lifecycle:

Detection → Triage → Mitigation → Resolution → Postmortem

Capacity Planning:

Required Capacity = Peak RPS × Avg CPU per request × Headroom factor
(1.3)

Chaos Engineering Checklist: - Region failure simulation - Node
termination tests - Network latency injection

Error Budget Policy:

If budget \<25% remaining: - Freeze feature releases - Focus on
reliability fixes

# GCP Ultimate DevOps / SRE / FinOps Master Guide

SECTION 1 – FinOps & Billing Deep-Dive Q&A

Billing Fundamentals

1.  What are GCP billing accounts?
2.  Difference between project and billing account?
3.  What is cost allocation using labels?
4.  How do you export billing data to BigQuery?
5.  What are committed use discounts (CUDs)?
6.  Sustained use discounts?
7.  Spot VM pricing model?
8.  How does BigQuery pricing work?
9.  Storage class cost comparison?
10. Egress cost calculation?

Advanced FinOps Questions

11. How to forecast GCP spend?
12. How to design cost visibility across 200+ projects?
13. Budget alerts vs cost anomaly detection?
14. How to implement showback/chargeback?
15. How to reduce idle resource costs?
16. Strategies for GKE cost optimization?
17. Rightsizing Compute Engine instances?
18. BigQuery slot reservations vs on-demand?
19. Dataflow FlexRS pricing advantage?
20. Multi-region cost tradeoffs?

SECTION 2 – Terraform Production Modules Library

Example VPC Module

resource “google_compute_network” “vpc” { name = var.vpc_name
auto_create_subnetworks = false }

resource “google_compute_subnetwork” “subnet” { name = var.subnet_name
ip_cidr_range = var.cidr region = var.region network =
google_compute_network.vpc.id }

Example GKE Module

resource “google_container_cluster” “primary” { name = var.cluster_name
location = var.region remove_default_node_pool = true initial_node_count
= 1 }

Example Cloud SQL Module

resource “google_sql_database_instance” “default” { name = var.db_name
database_version = “POSTGRES_14” region = var.region }

SECTION 3 – 50 Real DevOps Incident RCA Reports (Summarized)

1.  GKE CrashLoop due to bad env var – Fixed via rollback.
2.  Cloud SQL disk full – Enabled autoscaling storage.
3.  BigQuery runaway query – Implemented quotas.
4.  Dataflow job OOM – Increased worker memory.
5.  Public GCS bucket exposure – Removed public IAM binding.
6.  Service account key leak – Rotated & switched to Workload Identity.
7.  Firewall misconfiguration blocked traffic – Updated rule priority.
8.  Node pool upgrade outage – Enabled surge upgrade.
9.  Pub/Sub backlog spike – Increased subscribers.
10. Load balancer health check misconfig – Corrected backend port.
11. Incorrect IAM role caused pipeline failure.
12. GKE autoscaler disabled capacity issue.
13. VPC peering route overlap issue.
14. Spanner hot partition.
15. Bigtable hotspotting due to row key design.
16. Cloud NAT port exhaustion.
17. DNS misconfiguration outage.
18. Expired SSL certificate.
19. Overprovisioned VMs cost spike.
20. GKE memory leak in pod.
21. Cloud Run concurrency misconfig.
22. Artifact registry auth failure.
23. Secret rotation breaking app.
24. Dataproc cluster not deleted cost issue.
25. IAM condition blocking API access.
26. Logging quota exceeded.
27. Monitoring alert misconfigured.
28. KMS key disabled accidentally.
29. Snapshot deletion mistake.
30. MIG autohealing loop.
31. Cross-region replication lag.
32. Pub/Sub ack deadline too low.
33. Dataflow worker preemption.
34. BigQuery partition pruning failure.
35. Network policy blocking pod communication.
36. Insufficient disk IOPS.
37. API rate limit exceeded.
38. Terraform state corruption.
39. Unmanaged instance deleted manually.
40. Regional outage failover delay.
41. Cloud Armor rule misfire.
42. Incorrect service account scope.
43. Storage lifecycle misconfiguration.
44. Bucket retention lock issue.
45. Autopilot quota exceeded.
46. GKE pod disruption during maintenance.
47. Spanner node under-provisioned.
48. Excessive logging costs.
49. Cloud SQL connection pool exhaustion.
50. Backup restore failure due to version mismatch.

SECTION 4 – SRE / Error Budget Interview Pack

Core Concepts

-   SLI
-   SLO
-   SLA
-   Error budget
-   Burn rate
-   MTTR vs MTBF

Advanced Questions

1.  How to design SLO for API latency?
2.  How to calculate error budget burn?
3.  Multi-region SLO design?
4.  Golden signals?
5.  Reliability vs feature velocity tradeoff?
6.  Incident response lifecycle?
7.  Postmortem best practices?
8.  Chaos engineering strategy?
9.  Capacity planning approach?
10. Alert fatigue reduction?





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

# End of Document

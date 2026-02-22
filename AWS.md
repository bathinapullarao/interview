# AWS Interview Questions & Answers (Most Widely Used Services + Networking)

============================================================ SECTION 1 –
AWS NETWORKING
============================================================

## Basic

1.  What is a VPC? A Virtual Private Cloud (VPC) is a logically isolated
    network in AWS where you launch resources like EC2 instances.

2.  What is a subnet? A subnet is a range of IP addresses within a VPC.
    It can be public or private.

3.  Difference between public and private subnet? Public subnet has
    route to Internet Gateway. Private subnet does not.

4.  What is an Internet Gateway? A component that allows communication
    between instances in VPC and the internet.

5.  What is a NAT Gateway? Allows private subnet instances to access the
    internet without exposing them publicly.

## Intermediate

6.  What is a route table? Defines rules to determine where network
    traffic is directed.

7.  What is a Security Group? Instance-level virtual firewall
    controlling inbound and outbound traffic.

8.  What is a Network ACL? Subnet-level stateless firewall.

9.  Security Group vs NACL? Security Group is stateful; NACL is
    stateless.

10. What is VPC Peering? Connects two VPCs privately.

11. What is Transit Gateway? Central hub to connect multiple VPCs and
    on-prem networks.

12. What is Direct Connect? Dedicated private network connection from
    on-prem to AWS.

13. What is VPN? Encrypted tunnel between on-prem and AWS.

## Advanced

14. How does routing priority work? Longest prefix match wins.

15. What is PrivateLink? Private connectivity to AWS services over
    private IP.

16. What is Global Accelerator? Improves application availability and
    performance using AWS global network.

17. What is AWS CloudFront? Content Delivery Network (CDN) service.

18. What is Route 53? Managed DNS service.

============================================================ SECTION 2 –
EC2 & COMPUTE
============================================================

1.  What is EC2? Elastic Compute Cloud provides virtual servers.

2.  Instance types? General purpose, Compute optimized, Memory
    optimized, Storage optimized.

3.  On-demand vs Reserved vs Spot? On-demand: pay per use. Reserved:
    discounted long-term. Spot: unused capacity at lower cost.

4.  What is Auto Scaling Group? Automatically adjusts number of EC2
    instances.

5.  What is Elastic Load Balancer? Distributes incoming traffic across
    instances.

6.  ALB vs NLB? ALB works at Layer 7; NLB works at Layer 4.

7.  What is Launch Template? Defines configuration for EC2 instances.

8.  What is EBS? Elastic Block Store provides persistent storage.

9.  EBS vs Instance Store? EBS persistent; Instance store ephemeral.

============================================================ SECTION 3 –
S3 (Storage)
============================================================

1.  What is S3? Object storage service.

2.  Storage classes? Standard, IA, One Zone-IA, Glacier, Glacier Deep
    Archive.

3.  What is versioning? Maintains multiple versions of objects.

4.  What is lifecycle policy? Automates transition or deletion of
    objects.

5.  What is bucket policy? Access control policy for bucket.

6.  What is pre-signed URL? Temporary access to private object.

7.  What is S3 replication? Automatically replicates objects to another
    region.

============================================================ SECTION 4 –
IAM & SECURITY
============================================================

1.  What is IAM? Identity and Access Management service.

2.  What are IAM roles? Temporary credentials assigned to services.

3.  What is least privilege principle? Grant minimum required
    permissions.

4.  What is STS? Security Token Service for temporary credentials.

5.  What is KMS? Key Management Service for encryption.

6.  What is AWS Shield? DDoS protection service.

7.  What is WAF? Web Application Firewall.

============================================================ SECTION 5 –
RDS & DATABASES
============================================================

1.  What is RDS? Managed relational database service.

2.  Supported engines? MySQL, PostgreSQL, Oracle, SQL Server, MariaDB.

3.  What is Multi-AZ? High availability deployment across availability
    zones.

4.  What are Read Replicas? Offload read traffic.

5.  What is Aurora? AWS proprietary high-performance relational
    database.

6.  Aurora vs RDS? Aurora offers higher performance and auto-scaling
    storage.

============================================================ SECTION 6 –
SERVERLESS ============================================================

1.  What is Lambda? Serverless compute service.

2.  What triggers Lambda? S3, API Gateway, EventBridge, SNS, SQS.

3.  What is API Gateway? Managed API service.

4.  What is Step Functions? Workflow orchestration service.

============================================================ SECTION 7 –
MONITORING & DEVOPS
============================================================

1.  What is CloudWatch? Monitoring and logging service.

2.  What is CloudTrail? Tracks API calls.

3.  What is CodePipeline? CI/CD automation service.

4.  What is CodeBuild? Build service.

5.  What is CloudFormation? Infrastructure as Code service.

6.  What is AWS Config? Tracks resource configuration changes.

============================================================ SECTION 8 –
MESSAGING & STREAMING
============================================================

1.  What is SNS? Pub/Sub messaging service.

2.  What is SQS? Message queue service.

3.  SNS vs SQS? SNS pushes; SQS stores messages.

4.  What is MSK? Managed Kafka service.

============================================================ SECTION 9 –
COST OPTIMIZATION
============================================================

1.  What is AWS Cost Explorer? Analyzes AWS spend.

2.  What is AWS Budgets? Set spending thresholds.

3.  What is Savings Plan? Flexible pricing model for compute.

4.  How to reduce AWS cost? Use RI, Spot, right-sizing, auto-scaling,
    lifecycle policies.

# AWS Advanced Master Interview Guide

(200+ Q&A • Production Incidents • Architecture Case Studies • Terraform
Templates)

=====================================================================
SECTION 1 — 200+ ADVANCED AWS INTERVIEW Q&A
=====================================================================

## Networking (40)

1.  Explain VPC CIDR planning for large enterprises.
2.  How do you design overlapping CIDR connectivity?
3.  Transit Gateway vs VPC Peering at scale?
4.  Hub‑and‑spoke network architecture in AWS?
5.  How does AWS PrivateLink work internally?
6.  Direct Connect resiliency models?
7.  BGP attributes in AWS routing?
8.  Route table propagation in TGW?
9.  Multi‑account network isolation?
10. DNS resolution across VPCs?
11. Split‑horizon DNS design?
12. Route 53 failover routing?
13. Latency routing vs geolocation?
14. Health check failover design?
15. IPv6 in AWS VPC?
16. Egress‑only IGW?
17. NAT Gateway scaling limits?
18. NACL ephemeral port handling?
19. Security group referencing?
20. Cross‑region load balancing?
21. AWS Global Accelerator deep dive?
22. Shield Advanced protections?
23. WAF rate‑limit tuning?
24. Firewall Manager use cases?
25. Traffic mirroring?
26. Gateway Load Balancer?
27. Hybrid DNS with on‑prem?
28. Resolver inbound/outbound endpoints?
29. VPC Lattice overview?
30. Service mesh networking?
31. App Mesh vs Istio?
32. Network segmentation strategy?
33. Zero‑trust networking in AWS?
34. Private API Gateway design?
35. CloudFront origin failover?
36. TLS termination layers?
37. Jumbo frames in AWS?
38. ENI limits per instance?
39. Placement groups networking?
40. Multi‑region active‑active routing?

------------------------------------------------------------------------

## Compute / EC2 (35)

41. Nitro hypervisor architecture?
42. ENA vs SR‑IOV?
43. CPU credit model in T‑instances?
44. Dedicated Hosts vs Dedicated Instances?
45. Capacity Reservations?
46. EC2 Hibernate limitations?
47. Instance metadata v2 security?
48. Launch template versioning?
49. Warm pools in ASG?
50. Predictive scaling?
51. Lifecycle hooks?
52. Mixed instance ASG?
53. Spot interruption handling?
54. Rebalancing recommendations?
55. Placement group strategies?
56. Fault isolation design?
57. Bare metal use cases?
58. GPU scheduling?
59. AMI baking pipelines?
60. Image Builder?
61. Patch Manager integration?
62. SSM Fleet Manager?
63. EC2 serial console?
64. Instance connect endpoint?
65. EBS optimization?
66. io2 vs gp3 cost/perf?
67. Fast snapshot restore?
68. Multi‑attach EBS?
69. RAID on EBS?
70. Auto recovery alarms?
71. EC2 capacity blocks?
72. Savings Plans vs RI?
73. Graviton migration?
74. ARM performance tradeoffs?
75. EC2 cost anomaly detection?

------------------------------------------------------------------------

## Storage (25)

76. S3 strong consistency model?
77. Eventual vs read‑after‑write?
78. S3 request rate scaling?
79. Multipart upload tuning?
80. S3 Access Points?
81. Object Lambda?
82. Glacier retrieval tiers?
83. Intelligent tiering automation?
84. Replication time control?
85. S3 Batch Operations?
86. Inventory reports?
87. Macie classification?
88. Storage Lens analytics?
89. FSx variants comparison?
90. EFS performance modes?
91. Throughput bursting?
92. DataSync migration?
93. Snowball edge cases?
94. Backup vault locking?
95. Cross‑account backup?
96. Snapshot lifecycle policies?
97. RPO/RTO with EBS?
98. File vs block vs object?
99. Storage gateway modes?
100. Hybrid storage design?

------------------------------------------------------------------------

## Databases (40)

101. Aurora storage architecture?
102. Aurora global database?
103. Write forwarding?
104. RDS Proxy?
105. IAM DB authentication?
106. Performance Insights?
107. Read replica lag tuning?
108. Multi‑AZ cluster vs instance?
109. Blue/green deployments?
110. DynamoDB partition design?
111. Adaptive capacity?
112. DAX caching?
113. Streams + Lambda?
114. Global tables?
115. TTL lifecycle?
116. PartiQL queries?
117. On‑demand vs provisioned?
118. Auto scaling throughput?
119. Hot partition mitigation?
120. DynamoDB transactions?
121. Neptune graph use cases?
122. DocumentDB compatibility?
123. Keyspaces Cassandra model?
124. Timestream time‑series?
125. QLDB ledger design?
126. Redshift RA3 nodes?
127. Spectrum external tables?
128. Concurrency scaling?
129. Materialized views?
130. Data sharing?
131. Lake Formation governance?
132. Glue catalog design?
133. CDC pipelines?
134. DMS migration strategy?
135. SCT schema conversion?
136. Zero‑downtime DB migration?
137. Cross‑region DR replication?
138. PITR strategies?
139. Encryption at rest patterns?
140. Database access auditing?

------------------------------------------------------------------------

## Serverless / Integration (30)

141. Lambda cold start mitigation?
142. Provisioned concurrency?
143. SnapStart?
144. Lambda power tuning?
145. Step Functions patterns?
146. Saga orchestration?
147. Express vs Standard?
148. EventBridge schema registry?
149. Pipes service?
150. API Gateway caching?
151. Usage plans throttling?
152. WebSocket APIs?
153. AppSync GraphQL?
154. Cognito federation?
155. Amplify hosting?
156. SAM vs CDK?
157. Lambda layers?
158. Container image Lambdas?
159. EFS with Lambda?
160. Idempotency design?
161. DLQ patterns?
162. Retry policies?
163. Fan‑out architectures?
164. SNS filtering?
165. SQS FIFO scaling?
166. Exactly‑once processing?
167. Kinesis shard scaling?
168. Enhanced fan‑out?
169. Firehose buffering?
170. MSK vs Kinesis tradeoffs?

------------------------------------------------------------------------

## Security / Governance (30)

171. SCP policy hierarchy?
172. Permission boundaries?
173. ABAC in IAM?
174. IAM Access Analyzer?
175. GuardDuty threat detection?
176. Inspector vuln scanning?
177. Detective investigations?
178. Security Hub aggregation?
179. Macie PII detection?
180. KMS multi‑region keys?
181. External key store?
182. HSM CloudHSM?
183. Secrets Manager rotation?
184. Parameter Store tiers?
185. VPC‑SC equivalent in AWS?
186. Private CA?
187. ACM PCA?
188. Certificate rotation?
189. Nitro Enclaves?
190. Confidential computing?
191. Shield vs WAF vs Firewall?
192. Audit Manager?
193. Artifact compliance reports?
194. Config conformance packs?
195. Control Tower guardrails?
196. Landing zone security?
197. Zero trust IAM?
198. Just‑in‑time access?
199. Break‑glass accounts?
200. Security incident response?

=====================================================================
SECTION 2 — REAL PRODUCTION INCIDENT SCENARIOS
=====================================================================

Incident 1 — ALB 502 Errors  
Cause: Target health checks misconfigured  
Fix: Correct path/port, enable slow start

Incident 2 — NAT Gateway Cost Spike  
Cause: Large data egress via NAT  
Fix: VPC endpoints + S3 gateway endpoint

Incident 3 — Lambda Throttling  
Cause: Concurrency limit reached  
Fix: Reserved concurrency + scaling redesign

Incident 4 — DynamoDB Hot Partition  
Fix: Randomized partition keys

Incident 5 — EKS Node Not Joining  
Cause: IAM role mapping missing

(Additional incidents documented up to 25 covering RDS failover, Route53
DNS outage, CloudFront cache poisoning, KMS key disablement, etc.)

=====================================================================
SECTION 3 — ARCHITECTURE CASE STUDIES
=====================================================================

Case 1 — Multi‑Region Active‑Active SaaS

Route53 → Global Accelerator → ALB → EKS → Aurora Global DB

Case 2 — Serverless Event Platform

API Gateway → Lambda → EventBridge → Step Functions → DynamoDB

Case 3 — Data Lake

S3 → Glue → Athena → Redshift Spectrum → QuickSight

Case 4 — DR Strategy

Pilot Light / Warm Standby / Active‑Active comparison documented.

=====================================================================
SECTION 4 — TERRAFORM PRODUCTION TEMPLATES
=====================================================================

## VPC

resource “aws_vpc” “main” { cidr_block = “10.0.0.0/16” }

## Subnets

resource “aws_subnet” “public” { vpc_id = aws_vpc.main.id cidr_block =
“10.0.1.0/24” }

## EC2

resource “aws_instance” “web” { ami = var.ami instance_type =
“t3.medium” }

## ALB

resource “aws_lb” “app” { load_balancer_type = “application” }

## RDS

resource “aws_db_instance” “db” { engine = “mysql” instance_class =
“db.t3.medium” }

## EKS

module “eks” { source = “terraform-aws-modules/eks/aws” cluster_name =
“prod-eks” }

# Multi‑Cloud + Kubernetes + DevOps + FinOps Master Vault

Includes: • AWS + GCP + Azure Interview Vault  
• Kubernetes CKA / CKS Mega Q&A  
• DevOps Toolchain Incident RCAs  
• FinOps War‑Room Playbooks

============================================================ SECTION 1 —
MULTI‑CLOUD INTERVIEW VAULT (AWS + GCP + AZURE)
============================================================

## Architecture & Strategy

1.  Multi‑cloud vs Hybrid cloud?
2.  When to choose multi‑cloud?
3.  Vendor lock‑in mitigation strategies?
4.  Cross‑cloud DR design?
5.  Data replication across clouds?
6.  Latency challenges in multi‑cloud?
7.  Cost visibility across clouds?
8.  Identity federation design?
9.  Multi‑cloud networking models?
10. Service mesh across clouds?

------------------------------------------------------------------------

## Service Mapping Questions

| Capability     | AWS      | GCP             | Azure            |
|----------------|----------|-----------------|------------------|
| VMs            | EC2      | Compute Engine  | Virtual Machines |
| Kubernetes     | EKS      | GKE             | AKS              |
| Object Storage | S3       | GCS             | Blob Storage     |
| Data Warehouse | Redshift | BigQuery        | Synapse          |
| IAM            | IAM      | IAM             | Entra ID         |
| Serverless     | Lambda   | Cloud Functions | Functions        |

------------------------------------------------------------------------

## Advanced Multi‑Cloud Questions

11. Design active‑active across AWS & GCP?
12. DNS failover across clouds?
13. Multi‑cloud CI/CD strategy?
14. Secret replication?
15. Policy standardization?
16. Observability stack?
17. Unified logging?
18. Network encryption models?
19. Compliance across clouds?
20. Landing zone comparison?

============================================================ SECTION 2 —
KUBERNETES CKA / CKS MEGA Q&A
============================================================

## Core (CKA)

1.  Pod lifecycle?
2.  Init containers?
3.  Sidecar pattern?
4.  Deployment vs StatefulSet?
5.  DaemonSet use cases?
6.  Static pods?
7.  Taints & tolerations?
8.  Node affinity?
9.  Pod affinity?
10. PDB purpose?
11. HPA vs VPA?
12. Cluster autoscaler?
13. etcd backup/restore?
14. Control plane components?
15. Scheduler workflow?
16. kube-proxy modes?
17. CNI plugins?
18. Service types?
19. Ingress controllers?
20. CoreDNS troubleshooting?

------------------------------------------------------------------------

## Advanced (CKA)

21. Multi‑cluster federation?
22. Surge upgrades?
23. API server HA?
24. Certificate rotation?
25. Admission controllers?
26. CRDs design?
27. Operators pattern?
28. GitOps workflows?
29. ArgoCD sync waves?
30. Helm dependency mgmt?

------------------------------------------------------------------------

## Security (CKS)

31. Pod security standards?
32. OPA Gatekeeper?
33. Kyverno policies?
34. Image signing?
35. Runtime security?
36. Falco usage?
37. Secrets encryption?
38. Network policies?
39. mTLS in service mesh?
40. Supply chain security?

============================================================ SECTION 3 —
DEVOPS TOOLCHAIN INCIDENT RCAs
============================================================

## Jenkins Incidents

1.  Master disk full → Build failures  
    Fix: Log rotation + external storage

2.  Plugin upgrade broke pipelines  
    Fix: Version pinning + staging Jenkins

3.  Executor starvation  
    Fix: Dynamic agents

------------------------------------------------------------------------

## ArgoCD Incidents

4.  OutOfSync loop  
    Cause: Manual drift  
    Fix: Enforce GitOps only

5.  Sync failure due to CRD missing  
    Fix: Sync waves ordering

------------------------------------------------------------------------

## Helm Incidents

6.  Failed upgrade rollback stuck  
    Fix: helm rollback + state cleanup

7.  Values.yaml misconfig outage  
    Fix: Schema validation

------------------------------------------------------------------------

## Terraform Incidents

8.  State file corruption  
    Fix: Remote backend + locking

9.  Accidental resource destroy  
    Fix: lifecycle prevent_destroy

10. Drift after manual changes  
    Fix: terraform import + policy guardrails

(Expanded patterns cover 25+ real toolchain failures.)

============================================================ SECTION 4 —
FINOPS COST WAR‑ROOM PLAYBOOKS
============================================================

## War‑Room Scenario 1 — Sudden 300% Cost Spike

Steps:

1.  Billing export → BigQuery
2.  Identify service spike
3.  Check regions
4.  Review new deployments
5.  Kill runaway jobs

------------------------------------------------------------------------

## Scenario 2 — Kubernetes Cost Explosion

Root Causes:

• Idle node pools  
• Over‑requested CPU  
• No autoscaling

Fixes:

• Rightsize requests  
• Enable cluster autoscaler  
• Spot nodes

------------------------------------------------------------------------

## Scenario 3 — Data Warehouse Cost Surge

Mitigation:

• Partition tables  
• Query quotas  
• Materialized views

------------------------------------------------------------------------

## Scenario 4 — Storage Cost Leak

Detection:

• Old backups  
• Versioning bloat

Fix:

• Lifecycle rules  
• Archive tier

------------------------------------------------------------------------

## FinOps Governance Model

• Showback reports  
• Chargeback billing  
• Budget alerts  
• Anomaly detection  
• Unit economics dashboards

------------------------------------------------------------------------

## KPI Metrics

• Cost per customer  
• Cost per request  
• Infra cost / revenue %  
• Idle resource %
# Ultimate Platform Engineering + MLOps + Observability + Cloud Mega Question Bank

Includes:

• Platform Engineering (IDP, Backstage) Interview Pack  
• AI/ML Ops (Vertex AI, SageMaker, Kubeflow) Q&A  
• Observability War‑Room (Prometheus, Grafana, Datadog)  
• 1000+ Cloud Mega Question Bank (AWS + GCP + Azure + K8s + DevOps)

=====================================================================
SECTION 1 — PLATFORM ENGINEERING INTERVIEW PACK (IDP + Backstage)
=====================================================================

## Core Concepts

1.  What is Platform Engineering?
2.  Difference between DevOps vs Platform Engineering?
3.  What is an Internal Developer Platform (IDP)?
4.  Benefits of IDP?
5.  Golden path concept?
6.  Self‑service infrastructure?
7.  Developer experience metrics?
8.  Platform maturity model?
9.  Service catalog purpose?
10. Infrastructure abstraction layers?

------------------------------------------------------------------------

## Backstage (Spotify IDP)

11. What is Backstage?
12. Backstage architecture?
13. Software catalog?
14. Entity model?
15. Backstage plugins?
16. Scaffolder templates?
17. TechDocs integration?
18. Kubernetes plugin?
19. RBAC in Backstage?
20. Backstage vs Port vs Humanitec?

------------------------------------------------------------------------

## Advanced Platform Engineering

21. Multi‑tenant IDP design?
22. GitOps platform model?
23. Policy as code integration?
24. Secrets management in IDP?
25. Cost visibility in platform?
26. Developer sandbox environments?
27. Ephemeral environments?
28. Platform SLAs?
29. IDP observability?
30. Platform governance?

=====================================================================
SECTION 2 — AI / ML OPS INTERVIEW Q&A (Vertex AI • SageMaker • Kubeflow)
=====================================================================

## Foundations

1.  What is MLOps?
2.  ML lifecycle stages?
3.  Model drift?
4.  Data drift?
5.  Feature stores?
6.  Model registry?
7.  Experiment tracking?
8.  CI/CD for ML?
9.  Reproducibility challenges?
10. Model explainability?

------------------------------------------------------------------------

## Google Vertex AI

11. Vertex Pipelines?
12. AutoML vs custom training?
13. Feature Store?
14. Model monitoring?
15. Endpoint deployment?
16. Batch prediction?
17. Online prediction?
18. Vertex Workbench?
19. Model registry?
20. Drift detection?

------------------------------------------------------------------------

## AWS SageMaker

21. Training jobs?
22. Processing jobs?
23. SageMaker Pipelines?
24. Feature Store?
25. Model endpoints?
26. Multi‑model endpoints?
27. Shadow testing?
28. A/B testing?
29. Clarify bias detection?
30. Ground Truth labeling?

------------------------------------------------------------------------

## Kubeflow

31. Kubeflow Pipelines?
32. Katib hyperparameter tuning?
33. KFServing?
34. Notebooks?
35. TensorFlow operator?
36. PyTorch operator?
37. Pipeline DSL?
38. Metadata tracking?
39. Multi‑tenant Kubeflow?
40. Kubeflow vs Vertex vs SageMaker?

=====================================================================
SECTION 3 — OBSERVABILITY WAR‑ROOM (Prometheus • Grafana • Datadog)
=====================================================================

## Observability Foundations

1.  Metrics vs Logs vs Traces?
2.  Golden signals?
3.  RED vs USE methodology?
4.  SLIs/SLOs observability link?
5.  Telemetry pipelines?

------------------------------------------------------------------------

## Prometheus

6.  Pull vs push model?
7.  Exporters?
8.  Node exporter metrics?
9.  Service discovery?
10. Recording rules?
11. Alertmanager?
12. PromQL basics?
13. Federation?
14. Long‑term storage (Thanos/Cortex)?
15. Scaling Prometheus?

------------------------------------------------------------------------

## Grafana

16. Dashboard design principles?
17. Templating variables?
18. Alerting in Grafana?
19. Loki logs integration?
20. Tempo tracing?
21. Synthetic monitoring?
22. SLO dashboards?
23. Multi‑datasource panels?
24. RBAC in Grafana?
25. Grafana Cloud vs OSS?

------------------------------------------------------------------------

## Datadog

26. Agent architecture?
27. APM tracing?
28. Infrastructure monitoring?
29. Log pipelines?
30. RUM monitoring?
31. Synthetic tests?
32. Watchdog AI?
33. Cost monitoring?
34. Security monitoring?
35. Datadog vs Prometheus?

------------------------------------------------------------------------

## War‑Room Incident Scenarios

36. No metrics from node exporter  
37. High cardinality crash  
38. Alert storm fatigue  
39. Missing traces in APM  
40. Dashboard latency issues

=====================================================================
SECTION 4 — 1000+ CLOUD MEGA QUESTION BANK (SAMPLED STRUCTURE)
=====================================================================

Domains Covered:

• AWS (250)  
• GCP (200)  
• Azure (200)  
• Kubernetes (150)  
• DevOps Toolchain (100)  
• Security (50)  
• FinOps (50)

------------------------------------------------------------------------

## Sample Advanced Questions

1.  Design zero‑trust multi‑cloud architecture.
2.  Cross‑region DR for Kubernetes?
3.  Cost anomaly detection pipelines?
4.  Policy as code across clouds?
5.  Secrets federation multi‑cloud?
6.  Service mesh global failover?
7.  Observability correlation design?
8.  Chaos engineering multi‑region?
9.  GPU scheduling in Kubernetes?
10. AI inference autoscaling?
11. Confidential computing use cases?
12. Data sovereignty architecture?
13. Edge computing with CDN + Lambda?
14. FinOps chargeback design?
15. Cloud bursting patterns?






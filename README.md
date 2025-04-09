# AWS-RDS-Aurora
heoretical Conclusion: AWS RDS Mini Project
This project demonstrates a foundational workflow for setting up a relational database in the cloud using Amazon RDS and securely connecting it to an EC2 instance. It encapsulates essential cloud computing practices related to compute, storage, networking, and security.

🏗️ Database as a Managed Service
By using Amazon RDS, you offload operational responsibilities such as patching, backups, and high availability. This contrasts with self-hosted databases (e.g., on EC2), where the user must manage the database engine and operating system manually.

🔐 Secure Architecture
Security was enforced using Security Groups. Instead of allowing open access, traffic was limited such that only the EC2 instance could communicate with the RDS database. This reflects real-world best practices in isolating services within a Virtual Private Cloud (VPC).

🔄 Data Connectivity
The EC2 instance acts as a client machine that connects to the MySQL database using standard networking protocols over port 3306. Installing a MySQL client allows the user to issue queries, manage schemas, and work with live data in a cloud-native way.

🧷 Backup and Recovery
Creating a manual snapshot of the RDS database captures its current state. Snapshots can be retained indefinitely and used for: Disaster recovery, Testing on cloned environments, Safe rollback before critical changes

This aligns with cloud-native design principles where infrastructure is resilient, reproducible, and recoverable.

📘 Summary: AWS Route 53 – Exam-Focused Notes
This document is a complete guide to Amazon Route 53, tailored for the AWS Solutions Architect – Associate Exam. It covers both foundational DNS concepts and key Route 53 features with detailed explanations and real-world AWS usage examples.

✅ Core DNS Concepts
What is DNS: Explains the Domain Name System and how it resolves domain names to IP addresses.

DNS Hierarchy: Breaks down URL components using an example (http://api.www.example.com.), clarifying protocol, FQDN, subdomains, SLD, TLD, and root.

✅ AWS Route 53 Overview
Introduction to Route 53 as a highly available, scalable DNS and domain registration service.

Highlights features like DNS resolution, domain registration, and health checks.

✅ DNS Records in Route 53
Explains key record components: Name, Type, TTL, and Value.

Describes common DNS record types (A, AAAA, CNAME, NS).

Clarifies how records map names to IPs or domains.

✅ Hosted Zones
Differentiates Public Hosted Zones (for internet-facing domains) and Private Hosted Zones (for internal VPC use).

✅ TTL (Time To Live)
Explains how TTL controls DNS caching.

High TTL: Better performance, slow propagation.

Low TTL: Faster propagation, more DNS queries — useful for dynamic environments.

✅ CNAME vs Alias
Compares usage and limitations.

Alias records are AWS-specific, support root domains (APEX), and are free within AWS.

CNAME is standard DNS, only works on subdomains.

✅ APEX Domain
Refers to the root of a domain (example.com without www).

Route 53 allows using Alias records at the APEX level, while standard CNAMEs are not allowed here.

✅ Routing Policies in Route 53
Explains 7 Routing Policy Types with examples and use cases:

Simple – Default, single resource.

Weighted – Distributes traffic by percentage (e.g., 70/20/10), great for testing or canary deployments.

Latency-based – Routes to the region with the lowest latency.

Failover – Primary/Secondary failover using health checks.

Geolocation – Routes based on user's country or region.

Geoproximity – Routes based on user proximity and traffic bias.

IP-based – Routes based on the source IP of the client.

✅ Using Route 53 with Third-Party Registrars
Shows how to configure Route 53 even if the domain is bought from another provider.

Steps include creating a Hosted Zone and updating NS records at the registrar to point to Route 53 name servers.

This document serves as a quick-reference, learning, and revision resource, aligning tightly with the topics and terminologies AWS expects you to know for the SAA-C03 certification.

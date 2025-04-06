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

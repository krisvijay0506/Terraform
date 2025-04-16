# 🔥 Top 100 Interview Questions & Answers – GCP Data Engineer (Terraform, TFE, Dataplex, CI/CD)

---

## 🔹 Terraform & Terraform Enterprise (TFE) - Basics & Core Concepts

1. **What is Terraform and how does it work?**  
   Terraform is an open-source Infrastructure as Code (IaC) tool that automates the provisioning of infrastructure by defining resources in a declarative language (HCL). It works by comparing the current infrastructure state with the desired configuration and applying the necessary changes.

2. **Explain the difference between Terraform and other configuration management tools (like Ansible, Puppet, Chef).**  
   Terraform is primarily used for infrastructure provisioning, whereas tools like Ansible, Puppet, and Chef are more focused on configuration management (e.g., managing server configurations after deployment).

3. **What is the primary advantage of using Terraform over other Infrastructure as Code tools?**  
   Terraform offers a cloud-agnostic approach with a consistent CLI and language (HCL), allowing you to manage multi-cloud infrastructure easily, whereas tools like CloudFormation are AWS-specific.

4. **What is the role of the `terraform init` command?**  
   `terraform init` initializes a working directory containing Terraform configuration files by downloading the necessary provider plugins and setting up backend configurations.

5. **How does `terraform plan` work?**  
   `terraform plan` generates an execution plan by comparing the current infrastructure state with the desired state described in the configuration files, showing the changes Terraform will make.

6. **What is a Terraform state file and how does it work?**  
   The state file (.tfstate) is a local file that tracks the current state of infrastructure managed by Terraform. It is used to map resources in the configuration files to real infrastructure resources.

7. **What is the significance of the `terraform apply` command?**  
   `terraform apply` applies the changes defined in the execution plan to the infrastructure, provisioning or updating the resources as needed.

8. **How do you manage infrastructure in different environments (Dev, Test, Prod) using Terraform?**  
   You can manage different environments by using separate workspaces, variables, or backend configurations for each environment, ensuring isolation and scalability.

9. **What are Terraform providers? Can you give examples?**  
   Providers in Terraform are plugins that allow Terraform to interact with different cloud platforms and services. Examples include AWS, Google Cloud, and Azure.

10. **How do you configure and use variables in Terraform?**  
    Variables in Terraform are defined using the `variable` block and can be passed via `terraform.tfvars` or as command-line arguments to customize the configuration.

---

## 🔹 Terraform Enterprise (TFE) - Advanced Concepts

26. **What is Terraform Enterprise, and how is it different from open-source Terraform?**  
   Terraform Enterprise (TFE) provides additional features like a web-based UI, governance with Sentinel policies, team collaboration, private module registry, and remote backends, whereas open-source Terraform is command-line based.

27. **What are Workspaces in Terraform Enterprise?**  
   Workspaces in TFE represent isolated environments where infrastructure configurations can be managed. Each workspace stores its own state and is independent from other workspaces.

28. **How does Terraform Enterprise handle team access and roles?**  
   TFE uses role-based access control (RBAC) to assign permissions to users, such as Admin, Operator, or User roles, which control what actions users can perform in workspaces.

29. **How do you configure a remote backend in Terraform Enterprise?**  
   You configure a remote backend in TFE by setting up a backend configuration that connects to the TFE instance, enabling centralized state management and collaboration.

30. **What are Sentinel policies in Terraform Enterprise?**  
   Sentinel is a policy-as-code framework that enforces compliance and governance rules on infrastructure changes in TFE, allowing custom policy enforcement before applying changes.

---

## 🔹 Google Cloud Platform (GCP) – Data Engineering Focus

46. **What is Google Cloud Platform, and which GCP services are commonly used in data engineering?**  
   GCP is a cloud platform offering services like BigQuery, Dataflow, Dataplex, Cloud Pub/Sub, Cloud Storage, and Dataflow for data engineering tasks such as ETL, data analysis, and storage.

47. **How does BigQuery work, and how would you design a data warehouse using BigQuery?**  
   BigQuery is a fully managed, serverless data warehouse that uses SQL for querying large datasets. Design involves organizing data into datasets, tables, and partitioning them for performance.

48. **What are the different ways you can load data into BigQuery?**  
   Data can be loaded into BigQuery using Cloud Storage (via GCS import), batch loading with `bq` CLI, or streaming inserts.

49. **Explain the concept of GCP’s Dataplex and its use cases.**  
   Dataplex is a unified data governance and management service that allows organizations to manage, secure, and analyze data across different storage systems, ensuring compliance and consistency.

50. **How do you manage metadata and data governance using Dataplex?**  
   Dataplex uses a central data catalog to manage metadata, ensuring data quality, privacy, and security policies across different data storage systems.

51. **Can you integrate Dataplex with other GCP services like BigQuery and Dataflow?**  
   Yes, Dataplex integrates seamlessly with BigQuery for data querying and Dataflow for data processing, enabling a fully managed data governance solution.

52. **What are the benefits of using Dataplex over manually managed data lakes?**  
   Dataplex provides centralized governance, automated data classification, and improved data quality, while reducing manual effort and complexity in managing data lakes.

53. **Explain the role of GCP's Dataflow in managing ETL pipelines.**  
   Dataflow is a fully managed service for stream and batch processing of data. It is commonly used for ETL tasks like transforming and loading data into BigQuery or Cloud Storage.

54. **What are GCP Pub/Sub and its use in data streaming?**  
   Pub/Sub is a messaging service used for building event-driven architectures. It allows real-time messaging between applications and is used to stream data into services like Dataflow or BigQuery.

---

## 🔹 CI/CD for Data Engineering & Infrastructure as Code

77. **What is CI/CD, and why is it important in data engineering?**  
   CI/CD stands for Continuous Integration and Continuous Deployment, which automate the testing, building, and deployment of applications and infrastructure, ensuring fast, reliable, and consistent updates.

78. **How would you integrate Terraform into a CI/CD pipeline?**  
   You integrate Terraform into a CI/CD pipeline by using tools like Jenkins, GitLab CI, or Cloud Build to run `terraform init`, `terraform plan`, and `terraform apply` during the pipeline execution.

79. **Explain how you would set up a CI/CD pipeline for deploying data engineering workloads on GCP.**  
   You would set up a pipeline to automate Terraform code deployment, data pipeline deployment (using Dataflow or Composer), and testing via a tool like Jenkins or Cloud Build.

80. **How do you manage state file locks and concurrency in a CI/CD pipeline with Terraform?**  
   Terraform uses remote state backends (e.g., S3, GCS) to lock the state file, preventing concurrent changes during execution and ensuring consistency in the pipeline.

81. **What tools can you use to automate Terraform deployment in a pipeline?**  
   Tools like Jenkins, GitLab CI, CircleCI, or Cloud Build can be used to automate Terraform deployment within a CI/CD pipeline.

82. **How do you automate data pipeline deployments using Terraform and CI/CD?**  
   You automate data pipeline deployments using Terraform to define resources like Dataflow jobs, BigQuery datasets, or Cloud Storage buckets, and trigger them in CI/CD pipelines using tools like Jenkins.

83. **What is the role of automated testing in CI/CD for infrastructure?**  
   Automated testing in CI/CD ensures that Terraform configurations are validated and tested before being deployed, preventing errors and ensuring infrastructure consistency.

84. **How do you handle rollback scenarios in a Terraform-based CI/CD pipeline?**  
   Rollbacks can be handled by maintaining versioned backups of state files or by using `terraform destroy` to revert resources to a previous state if necessary.

85. **What is GitOps, and how can it be used to deploy infrastructure and data pipelines?**  
   GitOps is a methodology where the desired state of infrastructure and applications is stored in Git, and changes are automatically applied via CI/CD pipelines when changes are committed.

---

## 🔹 Security & Compliance in GCP and Terraform

91. **How do you secure data in transit and at rest on GCP?**  
   GCP secures data in transit using HTTPS/TLS and at rest using encryption keys, which can be managed using Google Cloud Key Management Service (KMS).

92. **What are IAM roles and policies in GCP, and how would you configure them for data engineering?**  
   IAM roles define permissions for users to interact with GCP resources. You configure roles by assigning predefined roles or creating custom roles based on the principle of least privilege.

93. **How would you implement least-privilege access for a GCP data pipeline?**  
   You would assign specific IAM roles to users and service accounts, granting only the necessary permissions to interact with the data pipeline resources, and avoid broad permissions like `owner`.

94. **What are service accounts in GCP, and how are they used for managing permissions?**  
   Service accounts are special Google Cloud accounts used by applications or virtual machines to interact with GCP services, with permissions assigned through IAM roles.

95. **How does Terraform manage sensitive variables (e.g., passwords, keys)?**  
   Terraform manages sensitive variables using the `sensitive = true` attribute and by securely storing them in the state file or using external vault services like HashiCorp Vault.

96. **How do you prevent accidental destruction of critical infrastructure with Terraform?**  
   You can use `terraform plan` to preview changes before applying them and enable resource protection in Terraform with lifecycle rules like `prevent_destroy`.

97. **What is the concept of resource drift in Terraform, and how do you handle it?**  
   Resource drift occurs when the actual state of resources diverges from the state file. It can be handled by running `terraform refresh` to update the state and reapply the configuration.

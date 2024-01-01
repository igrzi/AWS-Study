# Saving Plans

Saving Plans are **flexible price options**, which are more cost-effective than **On-Demand**, offering *specific usage* at a rate measured in USD per hour. They come with a commitment ranging from 1 to 3 years, resulting in potential savings of up to 72%.

![Saving Plans](/static/Savings_Plan_Diagram.png)

# Supported Services

- **Amazon EC2**
- **AWS Fargate**
- **AWS Lambda**
- **Amazon SageMaker**

# Saving Plans Types

When creating a Saving Plan for a specific category, it's important to note that it can't be used across different services. Despite having 4 services, there are only 3 categories of Saving Plans.

- **EC2 Instances Saving Plans**
- **Compute Savings Plans** (Covering EC2, AWS Fargate, and AWS Lambda)
- **SageMaker Savings Plans**

# How does it work?

Before diving into Saving Plans, a prerequisite is enabling **Cost Explorer** within AWS.

### What is *Cost Explorer*?

Cost Explorer is a service that validates your workspace and recommends cost-saving options. It provides tips on optimizing your workspace, with the analysis taking approximately 24 hours.

# Important Topics

Savings Plans offer discounted prices in *exchange for commitment*. Commitment terms cannot be altered post-payment. As your usage changes, you have the option to purchase ***Additional Saving Plans***.

- You can increase your workload hours with Additional Saving Plans, but reducing them is not possible.

- *EC2 Instances* and *Compute* plans apply to EC2 instances in Amazon EMR, Amazon EKR, and Amazon ECS. However, **Saving Plans** do not cover Amazon EKS charges, though the underlying EC2 instances are included.
- Prices for Saving Plans running SUSE Linux Enterprise Servers (SLES) differ from those of Reserved Instances (RI).
- Saving Plans aren't available in China regions.
- Saving Plans do not apply to puncutal usage or RIs covered usage.

# Saving Plans or RIs?

### Saving Plans

- Usage in **Computational solutions**, like EC2, Fargate or Lambda.
- Compute Savings Plans **allow changes** in instance family, Operational Systems (OS), size, locations and regions.
- Automatic environment adaptation.
- Discount on utilization of **Fargate and/or SageMaker**.
- Flexible environment and less management/monitoring.

### Reserved Instances

- Usage in **Database solutions**, like RDS, Redshift or Elasticsearch.
- Plan to use **at least 75%** of the time of your contract.
- Utilization on environments that have apps that are always "online".
- When you need a specific instance category and OS.
- Less flexible and more management/monitoring.
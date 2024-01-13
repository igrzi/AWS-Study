# Tags

They are ***Key:Pairs*** that allow you to **categorize** your resources in different ways, like by ambient, owner, etc.

Widely used for "mass" resource management:
- System Manager
- IaC
- Configuration Management

They allow for a ***more detailed billing control***. They also do not have semantic meaning, they are just interpreted as a *character sequence*.  

They are attributed ***manually*** for your resources, and allow you to work with [ABAC](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction_attribute-based-access-control.html).

## What is Attribute-Based Acess Control (ABAC)?

ABAC is a security model that determines access to resources based on attributes associated with identities, resources, and the current environment.

Instead of relying solely on fixed roles, *ABAC* considers various attributes to make access decisions.

### Key Concepts:

- **Attributes:** These are characteristics associated with identities (users, roles) and resources (EC2 instances, S3 buckets). Examples include department, job title, or project.

- **Policies:** ABAC policies define the access rules based on attributes. For instance, a policy might grant access only to users with the attribute "Department" set to "Engineering."

- **Access Decisions:** When a request is made, AWS evaluates the attributes against the defined policies to make access decisions.

## Example:

Consider a scenario where only users with the attribute "Role" set to "Admin" can terminate EC2 instances. The ABAC policy would look like this:

```json
{
  "Version": "2024-01-04",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "ec2:TerminateInstances",
      "Resource": "*",
      "Condition": {
        "StringEquals": {
          "aws:RequestTag/Role": "Admin"
        }
      }
    }
  ]
}

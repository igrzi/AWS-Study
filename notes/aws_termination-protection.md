# Shutdown Behaviour
The Shutdown Behaviour determines what happens when you shutdown an instance. 

We have ***two main shutdown behaviours***:
- Stop  | You **can** reinitialize your instance.
- Terminate | You **can't** reinitialize your instance.

# Termination Protection
This protection starts **disabled**, but can be turned on when creating/editing an instance.

This preventes accidental termination of an instance. The button even becomes disabled.

For more about ***instance states*** check [here.](/notes/aws_ec2_instances-states.md)

## Example:
Suppose you have an important production instance. Enabling Termination Protection ensures that the instance cannot be terminated accidentally, providing additional safeguards for your critical resources.

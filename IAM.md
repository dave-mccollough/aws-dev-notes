## IAM

#### IAM provides the following:

- Centralized control of your AWS Account
- Shared access to your AWS Account
- Granualar Permissions
- Identity Federation
- Multifactor Authentication
- Allows you to provide temporary access to users, devices, and services as necessary
- Allows you to setup a password rotation policy
- Integrates with most AWS services
- Supports PCI DSS Compliance

#### Terms

- Users
- Groups - Collection of users
- Roles - Created and assigned to AWS resources
- Policy Documents - JSON document that defines one or more permissions.  Can be attached to user, group or role

#### IAM Policy Simulator
https://policysim.aws.amazon.com

- Test the effects of IAM policies before committing them to production
- Validate the policy works as expected
- Test policies attached to existing users

#### Other Notes
- IAM is Universal
- The root account is simply the account created when you first setup your AWS account - Provides omplete access
- New users have no permissions when they are first created
- New users are assinged a **Access Key ID**  and **Secret Access Keys** when they are created.
    - These are not the same as the password and you cannot use them to login to the AWS console
    - They can be used to access AWS via the command line and APIs
- The **Secret Access Key** is only viewable when it is created.  Save in a secure location.  If lost, you will need to regenerate.  The **Access Key ID** is visible in the console.
- Setup MFA on root account
- Create and customize password rotation policies
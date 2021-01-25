## AWS CLI - Allows you to interact with AWS resources using the Command Line

### Links and Documentation
[AWS Docs](https://aws.amazon.com/cli/)
[CLI Reference](https://docs.aws.amazon.com/cli/latest/reference/)

### CLI Tips
- Least Privilege
    - Only give users the minimun amount of access they need to do their job.
    
- Groups
    - Use groups to manage permissions.  Users will inherit the permissions of the group they are assigned to.  Group permissions are assigned using policy documents.

- Secret Access Key
    - You will only see this once.  If you do not save it, you can delete the Access Key ID and Secret Access Key and regenrate.  You will need to run AWS configure again after regenerating your keys.
    - Create one Access Key Pair per developer/user.
    - The CLI can be installed on either Mac, Windows or Linux
    
### CLI Pagination
- You can control the number of items outputed from the CLI command.  By default, AWS uses a page size of 1,000.
- AWS makes an API call per 1,000 objects listed (if your S3 bucket had 3,000 items in it and you listed them, AWS would make 3 API calls to S3)
- API calls may time out when making API calls
    - To fix this, append --page-size to your command to request a smaller number of items (AWS will make more requests in the background, but return fewer items per request)
        - aws s3api list-objects --bucket my-bucket --page-size 100
    - You can also append the --max-items option to return fewer items to the CLI outpt
        -aws s3api lsit objects --bucket my-bucket --max-items 100
# AWS Immersion Day Workshop Labs
## Compute

### Auto Scaling with CloudFormation
   - Create basic EC2 web server with userdata.txt
   - Edit template to allow t3.micro for use with free tier then set as default
   - Create AMI from EC2 instance
   - Setup auto scaling group using AMI for launch template, attach new SG for ASG
   - Create new ALB with target group, attach new SG for ALB
   - Configure inbound rules for SGs
   - Test with DNS and CPU load generator ✅
## Network
###  VPC and Security Groups
   - Created VPC with two subnets and associated with route tables
   - Added SG with ICMP and SSH inbound rules
   - Launched two EC2 instances in different AZs. Connected to EC2-1 and pinged EC2-2 to test connectivity.
   - Installed tidy to pretty print curl command with:

```sh
curl -s example.com | tidy -indent -wrap 80
```
## Security
### IAM
   - Deployed EC2 instances with tags
   - Added IAM policy to user that allows EC2 actions for instances with dev tag
   - Created user group with new user and attached policy to test limited permissions by attempting to stop EC2 instance without dev tag
   - Created S3 buckets, IAM role with permissions to view one of the buckets. Assigned role to EC2 instance and tested with `aws s3 ls`

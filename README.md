# AWS Immersion Day Labs
### Compute
##### Basic EC2 Web Server
   - Use userdata.txt

##### Auto Scaling with CloudFormation
   - Edit template to allow t3.micro for use with free tier then set as default
   - Create AMI from EC2 instance
   - Setup auto scaling group using AMI for launch template, attach new SG for ASG
   - Create new ALB with target group, attach new SG for ALB
   - Configure inbound rules for SGs
   - Test with DNS and CPU load generator ✅
### Network
#####  VPC and Security Groups
   - Created VPC with two subnets and associated with route tables
   - Added SG with ICMP and SSH inbound rules
   - Launched two EC2 instances in different AZs. Connected to EC2-1 and pinged EC2-2 to test connectivity.
   - Installed tidy to pretty print curl command with:

```bash
curl -s example.com | tidy -indent -wrap 80
```
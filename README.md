# AWS Immersion Day Labs

#### Basic EC2 Web Server
   - Use userdata.txt


#### Auto Scaling with CloudFormation

   - Edit template to allow t3.micro for use with free tier then set as default
   - Create AMI from EC2 instance
   - Setup auto scaling group using AMI for launch template, attach new SG for ASG
   - Create new ALB with target group, attach new SG for ALB
   - Configure inbound rules for SGs
   - Test with DNS and CPU load generator ✅
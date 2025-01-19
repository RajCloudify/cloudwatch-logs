#### Configuring Amazon Coudwatch in EC2  ###########

1. Launch EC2 Instance
2. Attach I AM Role
3. Connect EC2 instance
4. Configure and Install Cloudwatch agent 


#### Configuring and install Cloudwatch agent ####

#### After completing steps 1,2,3 :- ###

_Linux commands in EC2 to Configure_

1. yum install amazon-cloudwatch-agent -y ----> (Installing Cloudwatch-agent)

2. Go to the opt directory and create a json file and configure
   
3. _Navigating to opt directory command_  _vi /opt/aws/amazon-cloudwatch-agent/bin/config.json_
       [https://github.com/RajCloudify/cloudwatch-logs/blob/main/config.json] (config.json)
   
   #### (_NOTE:-_ _Mention the Name,Stream Name and Region accoridnly_) ####

4. To configure and start the Amazon Cloudwatch Agent on the EC2 using the configuration file run 
  the following Linux command

   #### sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-ctl -a fetch-config -m ec2 -c file:/opt/aws/amazon-cloudwatch-agent/bin/config.json -s #######

5. CloudWatch has been successfully configured; you can verify it by navigating to the CloudWatch service in the AWS Management Console and checking the log group for the specified stream name.



  
   


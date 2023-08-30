/ [Home](index.md)

## Devops Tasks

Tasks:
1. Create simple EC2 by using CloudFormation with specific IPs enabled in the security Group.

2. Install Jenkins on EC2 

3. Create a Jenkins Job: git clone a repo and run a specific file
	Use Groovy for this

4. Jenkins Job: git clone a flask app and run it through jenkins
	Use Groovy for this

5. Create an Image from a running EC2 instance

6. Launch an instance with recently created instance

7. Install Vector on Ubuntu
	<br>
	[ref](https://rajasgs.github.io/wiki/vector.html)

08. Create Launch template by using recent EC2 that you have created. 

09. Automate the EC2 new Launch template version with new changes in the Ec2 on specific repository

10. Create S3 folder and upload a multiple files into S3 folder. Show the files with CloudFront

11. Create Aurora-Postgres DB 

12. Provide EC2 Bastion for the DB you have created recently.

13. Connect your flask logs to Kibana by using Vector 

14. Create Autoscaling group which will scale up based on the SQS messages. 
	<br>
	Each instance should consume 5 messages per minute.
	<br>
	Max 3 instances should be used for testing
	
15. AWS Alarm should be created when only 20% space in EC2. User should get an email when such situation occurs.

16. Setup ECS cluster and test 2 Microservices

17. Add 2 env values in AWS Param store and retrieve them in Python file from EC2

18. Microservices - Docker compose should consume AWS Param store values.

19. Apache Flink should be tested on EC2

20. Pritunl should be setup on EC2

21. Gitlab should be setup on EC2 (On premise Gitlab)

22. Journalctl should be analyzed by Apache Flink

23. Random log file should be analyzed by Apache Flink




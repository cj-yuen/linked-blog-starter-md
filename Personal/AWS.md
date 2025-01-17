#platform

>Amazon Web Services (AWS) = cloud-computing platform & API's

## Core Services
### Compute
<u>EC2</u> $-$ stock standard virtual server (rent by hour/day/year)
	full stack web service that you want to host 
		ie. Python Flask app, NodeJS Express server, WordPress website, etc.

<u>Lambda</u> $-$ function letting you run code serverlessly (use whenever you need it, pay by the millisecond) ==free (w/monthly limits)==
	 ie. somebody calls your API/once an hour & you want to run a function 

### Storage
<u>S3</u> $-$ Simple Storage Service (AWS version of Dropbox)
	file storage 
		ie. image, text,, video

### Database
<u>RDS</u> $-$ managed [[SQL]] database 

<u>DynamoDB</u> $-$ serverless database ==free (w/monthly limits)==

### Networking & Content Delivery
<u>CloudFront</u> $-$ typical  content delivery network (CDN) ==free (w/monthly limits)==
	service/static website & want to distribute around the world @edge locations

<u>API Gateway</u> $-$ allows developers to create/publish/maintain/monitor/secure API's
	works well w/Lambda as you can hook it up & have an http endpoint to call that Lambda function 

### Application Integration
<u>SQS</u> $-$ Simple Queue Services ==free (w/monthly limits)==
	managed message queues 


## Examples
1) To-do list website 
	static front-end & severless functions 
![[Pasted image 20240522121037.png]]


## Usage
1) AWS Console <u>(beginning)</u>
	go to website & click around (good for starting out but prb want to automate)
2) AWS CLI <u>(automate a little)</u> 
	from terminal (debugging & one-off operations & some level of program access)
3) AWS SDK <u>(programming)</u>
	app code & talk to AWS
	*SDK's available for all major programming languages*
4) Infrastructure as Code (CDK) <u>(advanced users)</u> 
	write infrastructure as code
	something like Terraform?

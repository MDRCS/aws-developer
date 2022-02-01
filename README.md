# aws-developer
- AWS Certified Developer AKA DVA-C01

- There is over 30 AWS services.

![aws-services](./static/aws-services.png)

## 1- AWS Global Infrastructure :
    
    - aws regions
    - aws availibility zones
    - aws data centers
    - aws edge locations/point of presence

    this is a cool websites that shows availibility of cloud providers world wide. 
    https://www.cloudinfrastructuremap.com/
    
    % Question 1: How to choose a region ?
    
    + Complience : sometimes we have data governance constraints to not allow data to be 
                    stored outside of a region (e.g : France Bank data doesn't have permission to be stored in USA)
    + Services Availabilty : Not all aws services are available in all regions.
    + Latency : The closest the data center the lower is the latency.
    + Pricing : Pricing differ from region to region.

![How to choose a region](./static/regions.png)

    % Availablity Zones :
    - Evry Region have multiple availability zones (min: 2, max: 6)
    - They are seperated, isoleted from disaster.
    - They are connected, with high bandwidth, and ultra-low latency.

![AZ](./static/az.png)
    
    + NB: you can check aws services availibilty by region thought this website :
    https://aws.amazon.com/fr/about-aws/global-infrastructure/regional-product-services/

    - Scopes of AWS services :
    + Amazon EC2 (Infrastucture as a service)
    + Amazon Elastic beanstalk (Platform as a service)
    + Amazon Lambda (Function as a service)
    + Amazon rekognition (Software as a service)


### 2- Amazon IAM Identity & Access Management (Users, Groups, Policies):
    - First IAM service doesn't require a region selection, it's a global service.
      ( e.g EC2 is a regional service )

    1- The root user of the account should not be used or shared by different teams instead we should create 
        other users (IAM users) assigned to groups, and have limited privileges thought different services.
    2- there is policies that define each user how many permissions he have.

![](./static/policy.png)
![](./static/policies-inheritence.png)
![](./static/iam-policy-structure.png)
    
    NB: you can create your own policies thought Visual Editor you choose effects, resources and you are done.
    
![](./static/create-policy.png)

    2-1 IAM MFA - Multi Factor Authentication :
    MFA = your password + a device you own

    - Main benefits of MFA :
    + Even your password is hacked or stolen no one could login to your account 
      cuz it's protected by that device that you own.
    
### - There is too many options to use MFA with IAM users :    

![](./static/MFA.png)

    2-1-1 Hands-on to setup MFA for a given user :

    1- go to security credentials.
    2- Click on Assigned MFA
    3- Select Virtual MFA
    4- Check the list of mobile apps compatible with aws accounts.
    (I prefer using Authy cuz it's multi-device)
    5- Click on generate QR code.
    6- Scan the qr code from your device.
    7- you will get multiple tokens that will expire in 30 seconds 
       entre two of them to validate connectivity between Authy and AWS Account.
    8- sign-out and sign-in to make sure its working

    Congrats you re done.

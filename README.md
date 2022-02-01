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


    


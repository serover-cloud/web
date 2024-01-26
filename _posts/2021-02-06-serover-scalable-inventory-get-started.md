---
layout: post
title:  "Get started in minutes"
permalink: /implementation-overview/
categories: [ Implementation, services, get-started ]
image: assets/images/implementation.jpg
featured: true
---

Implementation and maintenance of enterprise class software can be challenging even for most mature process-oriented organizations. Most of the inventory service provides available in market require extensive server provisioning, which could take weeks. Apart from provisioing, the implementation may require extensive mapping exercise and then development in client systems to call Inventory Service.   With Serover Scalable Inventory you can hit in the ground running in minutes. Our team has built Serover Scalable Inventory as a self service SaaS solution and is deployed on serverless architecture on AWS. So, you can start using our APIs instantly upon sign up. 

Here are the high level steps to get started :

* Self-service provision via AWS marketplace
* Integrate with your ecosystem using our simple to use REST endpoints
* Enhancements & Ongoing Support

The cloud-native, self-service SaaS environments are provisioned immediately. The platform offers predictable pricing, performance, flexibility and the ability to elastically scale to meet changing demand.

## Provision

Though you can sign up for a free trial on AWS marketplace, we recommend following steps before sign up to fully utilize the product features.

+ Prior to provisioning, work with our team for a free discovery consultation to evaluate system landscape and desired use cases
+ Identify integration needed to meet all use cases
+ Before committing to final purchase, our team can prepare a tailored demo of the product 

If your business needs meet our product then please go to AWS marketplace and subscribe for the Serover Inventory at following location
- https://aws.amazon.com/marketplace/pp/B093LMZMGJ


## Integrate with your ecosystem
+ Integrate with Serover Inventory Solutions in few easy steps below

1. Once registred for subscription at AWS Marketplace, you will get an email title __Welcome to Serover Inventory Solution!__. This email contains *__token endpoint__*, *__api key__*, *__client id__* and *__client secret__*. Please save these values as sensitive information and do not share.
2. You need to generate an base64 encoded string with client id and client secret. You can use following command to generate it

```
echo -n '<client id>:<client secret>' | openssl base64
``` 
3. Now you need to generate oauth token to access serover APIs. To generated JWT token please make POST request to token endpoint using above base64 encoded string as below 

```
curl -X POST <token endpoint> \
-H 'authorization: Basic <Base64 Encoded String>' \
-H 'content-type: application/x-www-form-urlencoded' \
-d 'grant_type=client_credentials&scope=transactions%2Fall'
```

4. You oauth token is valid for 1 hour and needs to regenerated before that to access APIs. 
5. Pass api key as __x-api-key__ and oauth token as __Authorization__ in headers for API call.

## Enhancements & Ongoing Support
+ We will continue to work with you after we deliver the product and transition to your support team for ongoing maintenance

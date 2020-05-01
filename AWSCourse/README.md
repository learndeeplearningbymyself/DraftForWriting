Summarize AWS Certified Developer - Associate

## AWS Fundamental

### AWS Regions and AZs

<img src="https://user-images.githubusercontent.com/43769314/80077071-f7a3ae80-8587-11ea-833f-dd43c9f68f81.png" width="720">

### IAM

<img src="https://user-images.githubusercontent.com/43769314/80079283-093a8580-858b-11ea-9ada-cfd3b059e152.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80080022-fc6a6180-858b-11ea-8a13-d00a4be19a2c.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80080242-510ddc80-858c-11ea-96ad-880356d72021.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80081825-6be15080-858e-11ea-9bc6-4c948bdb615d.png" width="720">

### EC2

<img src="https://user-images.githubusercontent.com/43769314/80325734-51022b00-8871-11ea-9431-7889a295ce4f.png" width="720">

**0.0.0.0/0**: means every IPs
**Key pair** give you access, log in to EC2 instance
**ec2-user** is basically the linux user into the Amazon linux machine

**Permissions 0644**, "**.pem"  are too open => your keys maybe leak

==> $chmod 0400 **.pem (0400 means "Allows the owner to read")

### Security Group

<img src="https://user-images.githubusercontent.com/43769314/80338172-b0befd00-8896-11ea-9d95-8739be21767c.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80338473-5a05f300-8897-11ea-9780-b5905cacf5fa.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80338583-a0f3e880-8897-11ea-811d-772235a4a9aa.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80338705-fa5c1780-8897-11ea-9d7f-57edabcbc1b6.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80339459-a5210580-8899-11ea-9ea5-22051c8f7db2.png" width="720">

### Private, Public, Elastic IP

<img src="https://user-images.githubusercontent.com/43769314/80339807-62136200-889a-11ea-9427-6b3209073d38.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80339871-87a06b80-889a-11ea-9c73-c344ca2cb45c.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80339978-b9193700-889a-11ea-8ddb-bbe3c4c19a1c.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80340677-0a75f600-889c-11ea-8a52-73655ff5a4b9.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80342870-e5838200-889f-11ea-9eef-1a01f9012c8e.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80345543-3ac19280-88a4-11ea-9084-2bfc70715348.png" width="720">

### EC2 Launch Modes

<img src="https://user-images.githubusercontent.com/43769314/80350538-d73b6300-88ab-11ea-8c4d-6930e328ccae.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80350644-0225b700-88ac-11ea-9f7a-535f3674ca98.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80351066-a9a2e980-88ac-11ea-82d7-c46ead3e9bf3.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80351251-fd153780-88ac-11ea-92c3-3e089498e578.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80353998-1ddf8c00-88b1-11ea-80fe-1f45290a0d97.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80354570-e02f3300-88b1-11ea-9144-3939770efac0.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80354664-0228b580-88b2-11ea-807e-6930ada6a1b3.png" width="720">

### EC2 - Good things to know and the checklist

<img src="https://user-images.githubusercontent.com/43769314/80355033-824f1b00-88b2-11ea-92c3-bf07fc5d2da2.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80355450-17eaaa80-88b3-11ea-9928-bbe5ac1dfe5a.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80355687-5aac8280-88b3-11ea-9081-28da369e9ddd.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80356000-c989db80-88b3-11ea-9615-3bf0274f9ffb.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80356161-05bd3c00-88b4-11ea-8359-07d449ce1ebb.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80356299-3ac98e80-88b4-11ea-8f15-4039064a9dfa.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80356467-795f4900-88b4-11ea-87e8-347128cde0a9.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80356624-ad3a6e80-88b4-11ea-8b8a-9ba570dfe80d.png" width="720">

## Load Balancer, Auto Scaling, EBS

### Load Balancer

<img src="https://user-images.githubusercontent.com/43769314/80445265-c42d9f00-894e-11ea-8785-6dd636583ee7.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80445420-2c7c8080-894f-11ea-972c-5e44a143dc61.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80445579-9eed6080-894f-11ea-9e07-8fce01c27357.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80445667-d0662c00-894f-11ea-9b92-4191c81f67a1.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80452097-75890080-8960-11ea-89d6-a17070261f5f.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80452540-73737180-8961-11ea-9b7d-8d3e06acd734.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80452860-1a580d80-8962-11ea-9df1-0d53f864ac45.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80453130-9fdbbd80-8962-11ea-98e3-85d197261771.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80453865-0c0af100-8964-11ea-9137-bfc76c4dc245.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80453953-30ff6400-8964-11ea-95a6-1181ed704c6f.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80454036-58563100-8964-11ea-94cf-1b7ece6beb26.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80454168-994e4580-8964-11ea-80f6-b44a4f270dcd.png" width="720">

### Auto Scaling

<img src="https://user-images.githubusercontent.com/43769314/80464825-4f219000-8975-11ea-831c-45e92b90b024.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80465844-aecc6b00-8976-11ea-934a-08e76807dab1.png" width="720">

> Load balancer and Auto Scaling are always work hand-in-hand

<img src="https://user-images.githubusercontent.com/43769314/80466329-5fd30580-8977-11ea-8545-52253fdfb5c8.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80467303-98271380-8978-11ea-8652-470d2ecd29fd.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80467480-cf95c000-8978-11ea-92e3-4401eedfb468.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80467669-1edbf080-8979-11ea-96b7-055eca6dc6bf.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80467930-8134f100-8979-11ea-8f7c-6057e56ebd73.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80468213-de30a700-8979-11ea-8b84-d1471de704c0.png" width="720">

### EBS Volumes

<img src="https://user-images.githubusercontent.com/43769314/80772816-e3b50980-8b92-11ea-8953-006540530c91.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80772975-75247b80-8b93-11ea-92e7-f7eaa03b3990.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80773089-c896c980-8b93-11ea-9040-031ab292dba6.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80773210-2aefca00-8b94-11ea-8375-781b5ab199c6.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80773260-52469700-8b94-11ea-979a-01931332e61e.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80773314-8326cc00-8b94-11ea-8c3f-7aa9f6a03bef.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80773422-d6008380-8b94-11ea-848f-d5bb2c92268c.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80773920-58d60e00-8b96-11ea-98a8-0f95de337a76.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80773971-88851600-8b96-11ea-8650-3a39d392f06a.png" width="720">

### Route 53

<img src="https://user-images.githubusercontent.com/43769314/80785437-386c7a80-8bbb-11ea-95fb-87834dc794a4.png" width="720">

## Lambda

### Serverless

Serverless == FaaS (Function as a Service) - you don't see, provision server, someone manages server for you

We leave more of the management of the architect and infrastructure to AWS and we just implement the code

<img src="https://user-images.githubusercontent.com/43769314/79814886-50bde780-83ba-11ea-8b2f-1adcce0b498d.png" width="720">

### Lambda overview

<img src="https://user-images.githubusercontent.com/43769314/79821623-3986f600-83ca-11ea-81ca-28a6fac7b645.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79822543-5c1a0e80-83cc-11ea-9a0c-4ff6621a4812.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79821974-0d1fa980-83cb-11ea-874f-fc8e96e34bba.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79822176-84553d80-83cb-11ea-9c9e-6f3a1d616550.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79822313-d1391400-83cb-11ea-98e0-94b5f93e66b3.png" width="720">

### Lambda Concurrency, Throtting and DLQ

<img src="https://user-images.githubusercontent.com/43769314/79823463-dba8dd00-83ce-11ea-86a0-72e166bbaddd.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79830447-5c240980-83e0-11ea-997d-6945438f2bf6.png" width="720">

### Lambda Limit Values

<img src="https://user-images.githubusercontent.com/43769314/79835956-8975b500-83ea-11ea-92c0-7b3f37ba9d3e.png" width="720">

### Lambda versions, aliases

<img src="https://user-images.githubusercontent.com/43769314/79836666-6d264800-83eb-11ea-8507-e61fcbe79d2e.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79837346-369cfd00-83ec-11ea-9665-c167c3e36c3d.png" width="720">

### Lambda and CloudFormation

<img src="https://user-images.githubusercontent.com/43769314/79841250-1e2fe100-83f2-11ea-9ea7-6b5138e7ad3e.png" width="720">

### Lambda /tmp space

<img src="https://user-images.githubusercontent.com/43769314/79846218-22abc800-83f9-11ea-933b-9c00123ff491.png" width="720">

### Lambda best practices

<img src="https://user-images.githubusercontent.com/43769314/79846602-9b128900-83f9-11ea-9b51-6296a3972534.png" width="720">

### Lambda@Edge

<img src="https://user-images.githubusercontent.com/43769314/79935048-e88d0580-848e-11ea-933c-7ce10b7da920.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79935149-2722c000-848f-11ea-9fa8-6f75541f55c9.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79935240-5fc29980-848f-11ea-909b-913815332dde.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79935311-94ceec00-848f-11ea-9c62-f4fb8d0742bc.png" width="720">

## DynamoDB

### Overview

<img src="https://user-images.githubusercontent.com/43769314/79938411-7e2c9300-8497-11ea-8da4-08b68796c171.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79950838-a2499d80-84b2-11ea-846e-0ea20839f82b.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79951398-927e8900-84b3-11ea-8c88-8269775903ac.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79952426-5ba97280-84b5-11ea-8a08-c2748bd4faec.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79952808-f1dd9880-84b5-11ea-98f8-8122fffdd532.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79953149-66183c00-84b6-11ea-99ee-9a0cc7281d75.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79953307-98c23480-84b6-11ea-867a-09d67b722fff.png" width="720">

### DynamoDB - Provisioned Throughput

<img src="https://user-images.githubusercontent.com/43769314/79957506-a084d780-84bc-11ea-8874-d745716719f1.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79957930-46d0dd00-84bd-11ea-88d9-87a89d327498.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79958457-e7270180-84bd-11ea-9d23-879f27403aab.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79958727-3ff69a00-84be-11ea-91a5-cc5f44583bdf.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79959152-bdbaa580-84be-11ea-8b50-1e69950ce566.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79959389-0d996c80-84bf-11ea-85a5-4aca7f7db737.png" width="720">

### Basic APIs

<img src="https://user-images.githubusercontent.com/43769314/79960672-a5e42100-84c0-11ea-8e6b-8f4b20490ade.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79960858-e479db80-84c0-11ea-99bb-970e3a897651.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79961250-6407aa80-84c1-11ea-9765-1b5d9512782b.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79961455-b9dc5280-84c1-11ea-870b-d0e0bfe8c628.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79961707-10499100-84c2-11ea-981e-e08ceeb3780e.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79962078-936ae700-84c2-11ea-9a19-535e559ec2e9.png" width="720">

### DynamoDB GSI + LSI

We can use LSI + user_id to get and sort the results directly (local because it "local" to the partition key)

<img src="https://user-images.githubusercontent.com/43769314/79964178-49cfcb80-84c5-11ea-86cc-c250db3e4140.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79964428-adf28f80-84c5-11ea-9330-cbd747324f5f.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79964628-f14cfe00-84c5-11ea-8223-bd1d91f70363.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79964812-32451280-84c6-11ea-8e43-2063a399b27b.png" width="720">

### DynamoDB Concurrency

<img src="https://user-images.githubusercontent.com/43769314/80049573-40d70c80-854e-11ea-935d-fc0eba0af7e4.png" width="720">

### DynamoDB DAX

<img src="https://user-images.githubusercontent.com/43769314/80056675-b697a400-855f-11ea-945f-7845e5861327.png" width="720">

### DynamoDB Streams

<img src="https://user-images.githubusercontent.com/43769314/80057295-25c1c800-8561-11ea-97b7-3c73552ea953.png" width="720">

### DynamoDB TTL

<img src="https://user-images.githubusercontent.com/43769314/80068237-39c5f380-857a-11ea-9570-ccc732395930.png" width="720">

### DynamoDB CLI

<img src="https://user-images.githubusercontent.com/43769314/80069006-907ffd00-857b-11ea-8023-1b74aa25c230.png" width="720">

### DynamoDB Transactions

"all or nothing" means if get error, transactions will be canceled, if don't get any errors => success

<img src="https://user-images.githubusercontent.com/43769314/80071588-dccd3c00-857f-11ea-8228-ddb5f83e489d.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80072106-bbb91b00-8580-11ea-83a9-2c171b894904.png" width="720">

### DynamoDB - Security & Other Features

<img src="https://user-images.githubusercontent.com/43769314/80072400-28ccb080-8581-11ea-9541-37b4423bf916.png" width="720">

## API-Gateway

We can define for each root of API Gateway which lambda function should be called

### Mapping templates

<img src="https://user-images.githubusercontent.com/43769314/79718368-dc7e3800-8316-11ea-812e-d6e64481d7d5.png" width="720">

### API Gateway Swagger

<img src="https://user-images.githubusercontent.com/43769314/79722842-bf9a3280-831f-11ea-9647-f016133f0b4a.png" width="720">

### API Gateway Cache

<img src="https://user-images.githubusercontent.com/43769314/79726051-253ced80-8325-11ea-9f70-adf716a3bd3c.png" width="720">

### API Gateway Monitoring

<img src="https://user-images.githubusercontent.com/43769314/79726342-98466400-8325-11ea-8314-8d6caaa29587.png" width="720">

### API Gateway Others

<img src="https://user-images.githubusercontent.com/43769314/79728161-726e8e80-8328-11ea-8c76-9dec21b4a7ad.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79728358-c7120980-8328-11ea-818c-d08456ab6792.png" width="720">

### API Gateway - Security

<img src="https://user-images.githubusercontent.com/43769314/79729221-1e64a980-832a-11ea-9eb6-92d148aefa6f.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79729405-64217200-832a-11ea-83d3-e9057eb76c4b.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79729628-acd92b00-832a-11ea-949a-3650aa4b2320.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79729874-004b7900-832b-11ea-91da-5ab0bc076624.png" width="720">

### AWS Cognito

<img src="https://user-images.githubusercontent.com/43769314/79731976-fecf8000-832d-11ea-8db6-5564abc274db.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79732217-553cbe80-832e-11ea-804c-2ac142d50eaf.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/79732531-c7150800-832e-11ea-929d-a7daf2147af8.png" width="720">

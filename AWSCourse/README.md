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

At least two (public) subnets must be specified when creating new Load Balancer

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

<img src="https://user-images.githubusercontent.com/43769314/81536058-dde6d180-93a5-11ea-8b2f-6a117bb3866b.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81536417-7aa96f00-93a6-11ea-9eb0-8827acc27dbe.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81536451-87c65e00-93a6-11ea-8438-bb7980255612.png" width="720">

Web browser must wait until the IP that be sent back from Route53 exipred to get the new one

<img src="https://user-images.githubusercontent.com/43769314/82000997-00723680-9695-11ea-9a7e-35aa4fd8e19d.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82007546-77173000-96a5-11ea-80f0-c8663ecf192a.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82008060-af6b3e00-96a6-11ea-9582-734cbe9f2eab.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82008608-235a1600-96a8-11ea-9dc1-361c6f4e4573.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82016045-1b57a180-96bb-11ea-83dd-4ff1aca351ab.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82016601-5908fa00-96bc-11ea-80fe-da674b1db93e.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82018967-48a74e00-96c1-11ea-98f1-cb4b0206a4c9.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82027792-be1a1b00-96cf-11ea-914b-4eaa4af78da5.png" width="720">

Multi Value: if once Route is "unhealthy", request will be redirected to the "healthy" once

### VPC

> We will have a default VPC for each launching EC2 instance

<img src="https://user-images.githubusercontent.com/43769314/82030079-e8210c80-96d2-11ea-9f68-8eb9df9a81c3.png" width="720">

By Default, we have one "public subnet" per AZ

<img src="https://user-images.githubusercontent.com/43769314/82030262-2c141180-96d3-11ea-9a11-66239e2bc430.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82030660-b52b4880-96d3-11ea-9079-127deae09f88.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82031347-b9a43100-96d4-11ea-9707-e6cb477ff884.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82031703-3c2cf080-96d5-11ea-9bab-c2900e21af47.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82113321-1d3f6480-9790-11ea-829e-e240bb72b30c.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82113367-77402a00-9790-11ea-8e0a-db6a001da500.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82113411-d2721c80-9790-11ea-837a-0081bd4b1efa.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82113520-955a5a00-9791-11ea-8ab9-2200960c2b84.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82113639-8cb65380-9792-11ea-8456-deca4393264e.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82113683-d56e0c80-9792-11ea-9a2c-0892325b8c4e.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82774943-2fe92600-9e81-11ea-84da-1c16b6025c38.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82775011-632bb500-9e81-11ea-86a0-ea5acfa387cf.png" width="720">

EC2 Security Group is state-ful

Network ACL: Like a firewall, state-less, you can set up your own allow or deny rules, blocked IP address here

<img src="https://user-images.githubusercontent.com/43769314/82776240-3e394100-9e85-11ea-8f55-3ba6520e3362.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82781955-27e7b100-9e96-11ea-9c1c-ca3ae9fbc2d1.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82782053-60878a80-9e96-11ea-9b4a-b98a7115c1fd.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82782157-9dec1800-9e96-11ea-97ed-fa06cc582a6b.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82782386-2a96d600-9e97-11ea-8383-c75f51a194f9.png" width="720">

- Think of a VPC as a logical datacenter in AWS
- Consists of Virtual Private Gateway, Route Tables, Network, Access Control Lists, Subnets, and Security Groups
- 1 Subnet = 1 Availability Zone
- 1 internet gateway attach to 1 VPC
- All created Subnet will not be public by default
- 1 Subnet - 1 Route table

<img src="https://user-images.githubusercontent.com/43769314/82785163-fe7e5380-9e9c-11ea-835f-15a9bab3d48e.png" width="720">

ICMP in SG (Security Group): We want to ping EC2 instance in current SG from our another SG

NAT instance is just an EC2 instance, NAT gateway allow your private subnet access to the outside network - Have to disable source/ destination check for NAT gateway

"blackhole" in Route table means: the instance doesn't exist

<img src="https://user-images.githubusercontent.com/43769314/82791496-d7c61a00-9ea8-11ea-95ae-60bb10507af1.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82791919-88ccb480-9ea9-11ea-8ccc-4e488789d07b.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82792069-c5001500-9ea9-11ea-95aa-b8fd36eebd93.png" width="720">

Created Network ACL denies everything by default

Have to put DENY rule(s) before ALLOW rule(s) by "#Rule order"

<img src="https://user-images.githubusercontent.com/43769314/82850772-9f6e1c80-9f38-11ea-946d-50ccab5c8651.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82850827-cc223400-9f38-11ea-83d4-16042e077f00.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82851109-afd2c700-9f39-11ea-974b-62dc64e7a83b.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82851163-e4df1980-9f39-11ea-8fa8-f29e4923db51.png" width="720">

Bastion is a way of SSH into your private instances

<img src="https://user-images.githubusercontent.com/43769314/82857006-abfb7080-9f4a-11ea-80e8-d748fee2e0ec.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82857990-8cb21280-9f4d-11ea-8516-5404b5374ef8.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82858000-976ca780-9f4d-11ea-941e-e8b76346a1a4.png" width="720">

### CloudFront

<img src="https://user-images.githubusercontent.com/15076665/82114314-06e8d700-9797-11ea-95e5-f59982e095d9.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82114353-4e6f6300-9797-11ea-89d0-af7d56993fab.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82114395-97271c00-9797-11ea-9e72-34b92fedfdfe.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82114449-cfc6f580-9797-11ea-87ef-ce9b679dd8cb.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82114585-85924400-9798-11ea-9897-a24f6af6e0d5.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82114612-b83c3c80-9798-11ea-83d1-0c70a278ceb6.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82114642-ed488f00-9798-11ea-9b0e-1c7205344872.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82115784-dfe2d300-979f-11ea-9a21-109070656cab.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82115799-fab54780-979f-11ea-8f06-a7880625a7e5.png" width="720">

Using HTTPs to ensure that everything will be secured

In first 3 hours: Cloudfront Domain will re-direct to origin URL (Ex: S3)

<img src="https://user-images.githubusercontent.com/15076665/82115893-a52d6a80-97a0-11ea-963f-dd47df0f4a53.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82116157-90ea6d00-97a2-11ea-90f0-d8bb9846d14a.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82116189-c727ec80-97a2-11ea-9c53-9f49accf172a.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82116230-2f76ce00-97a3-11ea-98c9-6078743bfa95.png" width="720">

### ECS

<img src="https://user-images.githubusercontent.com/15076665/82119859-c9974000-97bc-11ea-9faf-b6057bc847b4.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82120921-50035000-97c4-11ea-852d-5cf4c0a2e5ba.png" width="720">

Service Type "REPLICA" in ECS service means: we will run many tasks as possible, ""DAEMON" => 1 task. Service will launch our already defined task

<img src="https://user-images.githubusercontent.com/15076665/82134079-82e22e00-982e-11ea-9f5f-eea6f087c3fe.png" width="720">

### ECR

<img src="https://user-images.githubusercontent.com/15076665/82136789-16762780-984c-11ea-8f20-bb7f03bf54d5.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82138153-35c78180-9859-11ea-8a4a-1132dfa44d0f.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82138557-504f2a00-985c-11ea-8ac4-19509cf9b6d0.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82138702-67424c00-985d-11ea-9331-03830f152b0c.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82138745-b8ead680-985d-11ea-942c-ad9cc4929400.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82138789-197a1380-985e-11ea-921e-173e9f0b1b77.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82138821-51815680-985e-11ea-8cd9-d71f78b976b1.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82138847-88576c80-985e-11ea-9e9f-8b94db888a20.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82138896-d79d9d00-985e-11ea-8d98-178ff5f83ca4.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82139654-75e03180-9864-11ea-895a-1dc7065ef1e4.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82139679-aaec8400-9864-11ea-9eb7-10cad6a7f234.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82139744-16365600-9865-11ea-88a7-4e0f2fea13df.png" width="720">

"Target capacity %" in Capacity Provider means if ~% "busy" EC2 instances reach, the new EC2 instance will be created

<img src="https://user-images.githubusercontent.com/15076665/82140055-de7cdd80-9867-11ea-8300-784330ef8b37.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82140075-1ab03e00-9868-11ea-84e6-ccb60f409112.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82140096-46332880-9868-11ea-94cd-252737996053.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82140118-6cf15f00-9868-11ea-98ff-19d797a63c1a.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82140159-a033ee00-9868-11ea-8810-002650995742.png" width="720">

### ElasticBeanStalk

<img src="https://user-images.githubusercontent.com/15076665/82140724-c73fef00-986b-11ea-860e-dcf3d80a2a9b.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82140754-fb1b1480-986b-11ea-8024-79403a390c05.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82140831-8bf1f000-986c-11ea-9f60-59faae370a9b.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82140856-c9ef1400-986c-11ea-90cb-594df65cfa67.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82278270-cb335480-99c4-11ea-81f5-faed23c8647f.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82280668-5cf19080-99ca-11ea-9f31-ed284275d634.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82280754-92967980-99ca-11ea-8b86-fe6257f30fa1.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82280909-f5881080-99ca-11ea-85d3-66b19b697679.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82281066-5dd6f200-99cb-11ea-9f7a-ae15e02e1c1e.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82281179-ab535f00-99cb-11ea-8b6f-f0cfe9d6bc83.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82281491-6c71d900-99cc-11ea-883f-775d610d7f06.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82299901-0f3c4e80-99f1-11ea-8727-12c1d682502a.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82330216-7ff96000-9a1d-11ea-9b5d-31487101a062.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82331359-fa76af80-9a1e-11ea-90cb-7af5a1c00016.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82332080-eb443180-9a1f-11ea-90b5-28e32a2c99d5.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82332517-77eeef80-9a20-11ea-9a9a-22773ce901ce.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82332663-a53b9d80-9a20-11ea-8c22-109c98a74374.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82332855-e59b1b80-9a20-11ea-8f42-5e6c409677fd.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82333114-3ca0f080-9a21-11ea-9c28-c6f0b8195118.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82393939-ad2c2980-9a82-11ea-9c06-abaf18e2df8e.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82393939-ad2c2980-9a82-11ea-9c06-abaf18e2df8e.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82394075-f67c7900-9a82-11ea-90ee-58bcc17cbe97.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82409457-c5af3a80-9aa8-11ea-99e0-a4609cbdb2ff.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82410008-f17ef000-9aa9-11ea-8627-3bfa9e1c7bbd.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/82411920-a36beb80-9aad-11ea-83bc-eef054719ba2.png" width="720">

### RDS

<img src="https://user-images.githubusercontent.com/43769314/81537599-69f9f880-93a8-11ea-8303-6ac7b638c2c3.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81537724-9ada2d80-93a8-11ea-8f69-b52845193232.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81544852-00331c00-93b3-11ea-8e5a-9c7833e4207b.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81545792-60768d80-93b4-11ea-9a0a-eb63d6b8d3b8.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81767009-59659180-9512-11ea-8bc7-f0f5d5d7c73d.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81767106-916cd480-9512-11ea-94bf-9862761b4f6b.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81767263-ea3c6d00-9512-11ea-8015-5b75948524c3.png" width="720">

Difference between replica (for load balancing) and standby (Multi AZ) (for back-up or disaster recovery)

<img src="https://user-images.githubusercontent.com/43769314/81776359-a1dc7980-9529-11ea-89ce-9c8956f83c27.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81776616-17484a00-952a-11ea-89d7-59ff297b34b4.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81776752-5a0a2200-952a-11ea-961b-562210ff5faf.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81776885-a6edf880-952a-11ea-84dc-f5897434700a.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81777040-ffbd9100-952a-11ea-9aa4-3595115afff7.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81777273-76f32500-952b-11ea-945b-61ec74ad5c05.png" width="720">

### Amazon Aurora

<img src="https://user-images.githubusercontent.com/43769314/81885201-c93c5080-95d4-11ea-9d87-a606266adf04.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81885384-394ad680-95d5-11ea-8868-646100749beb.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81885911-56cc7000-95d6-11ea-81b7-e032df2a66f2.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81885980-83808780-95d6-11ea-891c-0689970702b5.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81886056-b4f95300-95d6-11ea-8165-615be71a18fd.png" width="720">

Aurora scale base on demand

<img src="https://user-images.githubusercontent.com/43769314/81888320-13750000-95dc-11ea-8350-0c23c6b12dca.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81889767-5a182980-95df-11ea-8c3e-aea10cdf3628.png" width="720">

### AWS ElastiCache Overview

<img src="https://user-images.githubusercontent.com/43769314/81890741-a7959600-95e1-11ea-9c9d-699d24e0253a.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81907347-8ee9a800-9602-11ea-9f78-4fb0484e3ddf.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81907501-d53f0700-9602-11ea-83a7-c28d13c70448.png" width="720">

Auto Failover means: if one downs, you can failover (use) to another one.

<img src="https://user-images.githubusercontent.com/43769314/81907831-56969980-9603-11ea-90f9-baebc742587e.png" width="720">

Redis AUTH Token need for application to connect to Redis

<img src="https://user-images.githubusercontent.com/43769314/81909579-c27a0180-9605-11ea-9e3b-7fe948732ba7.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81909886-32888780-9606-11ea-957a-5eb35e055cc0.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81910794-5e583d00-9607-11ea-9a5a-c29b810de80f.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81911276-0d951400-9608-11ea-8fe9-601ea9f27380.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81911385-31585a00-9608-11ea-9bc3-fe002eaf1f90.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81911813-bfccdb80-9608-11ea-9b9a-1cffda025be3.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81912053-08849480-9609-11ea-8582-93831a2128cc.png" width="720">

## Route 53

<img src="https://user-images.githubusercontent.com/43769314/81915028-00c6ef00-960d-11ea-8f7e-1f7ad4590465.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/81915430-86e33580-960d-11ea-92f8-517ed0e6f1f3.png" width="720">

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

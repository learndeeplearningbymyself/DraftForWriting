Summarize AWS Certified Developer - Associate

## AWS Fundamental

### AWS Regions and AZs

<img src="https://user-images.githubusercontent.com/43769314/80077071-f7a3ae80-8587-11ea-833f-dd43c9f68f81.png" width="720">

### IAM

<img src="https://user-images.githubusercontent.com/43769314/80079283-093a8580-858b-11ea-9ada-cfd3b059e152.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80080022-fc6a6180-858b-11ea-8a13-d00a4be19a2c.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80080242-510ddc80-858c-11ea-96ad-880356d72021.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/80081825-6be15080-858e-11ea-9bc6-4c948bdb615d.png" width="720">

> Roles are more secure than storing your access key and secret access key on individual EC2 instance

> Roles are universal, you can use it in any region

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

### EC2 Placement Groups

<img width="720" src="https://user-images.githubusercontent.com/15076665/92477020-d7188000-f21a-11ea-8237-dd51790f28ce.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92477286-5017d780-f21b-11ea-9a30-61a950913fb6.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92477433-92411900-f21b-11ea-8ac0-7b6bf30c067f.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92477563-c74d6b80-f21b-11ea-8860-ac4c6c89b319.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92542221-2c887780-f283-11ea-8ced-be421e0b3946.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92542378-9012a500-f283-11ea-91a5-fa00716a90c6.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92542728-863d7180-f284-11ea-9686-6d06cac0c463.png">

> Spread placement groups have a specific limitation that you can only have a maximum of 7 running instances per Availability Zone

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

**EC2** and **EBS volume** are always in the same availability zone

**gp2**: root volume - where EC2s OS be installed
**snapshot** is a photograph of the disk

> If we terminate an EC2 instance, the root volume of it will be terminated too, but additional volumes that attach to it will continue to exist

<img width="720" src="https://user-images.githubusercontent.com/15076665/92440305-41173200-f1e7-11ea-998d-da1142479362.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92440314-46747c80-f1e7-11ea-9fb6-905e768bbd03.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92440318-47a5a980-f1e7-11ea-907d-5ed3337a1bdb.png">

## Load Balancer, Auto Scaling, EBS

### Load Balancer

- **X-Forward-For** header: client public IP address (IPv4)
- 504 error means: Gateway has timed out --> Application layer or Database layer can have some problems

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

> The default delete-on-termination behaviour depends on whether the volume is a root volume, or an additional volume. By default, the DeleteOnTermination attribute for root volumes is set to 'true.'

> For an instance that is already running, the DeleteOnTermination attribute must be changed using the CLI.

### AMI

<img width="720" src="https://user-images.githubusercontent.com/15076665/92440989-5b054480-f1e8-11ea-9d11-5d90c48912bd.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92441529-58efb580-f1e9-11ea-9f4a-26ca53c36a0e.png">

With EBS volume, if something has gone wrong, you can stop instance and start it again at another hypervisor

<img width="720" src="https://user-images.githubusercontent.com/15076665/92443884-18923680-f1ed-11ea-833a-608be7b1ea1c.png">

### Encrypted root device volumes & Snapshot

<img width="720" src="https://user-images.githubusercontent.com/15076665/92449790-87738d80-f1f5-11ea-81a6-b7725dbe4386.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92449929-b689ff00-f1f5-11ea-9d45-2c859d4f81f9.png">

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

ICMP (Ping)

<img src="https://user-images.githubusercontent.com/15076665/82811899-ca228b80-9ecc-11ea-8aa5-028a28b00daa.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/82812118-3d2c0200-9ecd-11ea-90b3-c02084a0e6b3.png" width="720">

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

Service Type "REPLICA" in ECS service means: we will run many tasks as possible, ""DAEMON" => 1 task (for monitoring). Service will launch our already defined task

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

### Cloudwatch 101

<img width="720" src="https://user-images.githubusercontent.com/15076665/92450549-88f18580-f1f6-11ea-83c1-b16c1282d837.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92450852-e554a500-f1f6-11ea-8894-9990c511b58a.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92450857-e685d200-f1f6-11ea-8a69-3ed36c92f5f8.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92451033-28af1380-f1f7-11ea-9c0f-b12327950ea8.png">

<img width="720" alt="Screen Shot 2020-09-08 at 17 46 00" src="https://user-images.githubusercontent.com/15076665/92454163-2fd82080-f1fb-11ea-9102-7d8d86a05b65.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92454375-6ada5400-f1fb-11ea-910e-70a879ac3871.png">

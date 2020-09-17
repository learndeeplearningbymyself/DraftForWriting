Summarize AWS Certified Developer - Associate

### Database 101

RDS has two key features:
- Multi AZs - for disaster recovery
- Read replica - performance

If one RDS has failed, EC2 will automatically update DNS to point to another RDS (Multi AZs)

<img src="https://user-images.githubusercontent.com/15076665/92550044-a3c70700-f295-11ea-9a02-2ae6ca73080d.png" width="720">
(Multi AZs)

<img src="https://user-images.githubusercontent.com/15076665/92550274-218b1280-f296-11ea-835e-04e402b88782.png" width="720">
(Read replicas)

RDS runs on Virtual Machine and you can not access to that machine by SSH

<img src="https://user-images.githubusercontent.com/15076665/92680252-629e2800-f365-11ea-9690-bb62e100ff96.png" width="720">

### RDS Backup

<img src="https://user-images.githubusercontent.com/15076665/92680554-130c2c00-f366-11ea-8695-21e63e6cd16a.png" width="720">

RDS Automated backup is default and the backup data is stored at S3

<img src="https://user-images.githubusercontent.com/15076665/92680734-9af23600-f366-11ea-9505-b1250b33f1b0.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92687846-38edfc80-f377-11ea-806a-e102a025432f.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92688311-1dcfbc80-f378-11ea-8d75-b9ad141b3161.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92688580-87e86180-f378-11ea-8c9f-58c130ed2bc9.png" width="720">

Multi AZ is available for the following databases:
- SQL Server
- Oracle
- MySQL Server
- PostgreSQL
- MariaDB

<img src="https://user-images.githubusercontent.com/15076665/92689952-ffb78b80-f37a-11ea-9d7a-39cecea04420.png" width="720">

Read replica is available for the following databases:
- Oracle
- MySQL Server
- PostgreSQL
- MariaDB
- Aurora

<img src="https://user-images.githubusercontent.com/15076665/92690098-44dbbd80-f37b-11ea-9c0f-9b3d1a3ccc1e.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92690151-69d03080-f37b-11ea-8250-4b665cb2cd60.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92694246-bae32300-f381-11ea-9f72-c82ee943ed87.png" width="720">

### DynamoDB

<img src="https://user-images.githubusercontent.com/15076665/92695507-81131c00-f383-11ea-8945-1f998fb8acd2.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92695882-14e4e800-f384-11ea-9b52-55d0c9be23c8.png" width="720">

(One second rule for strong consistency)

<img src="https://user-images.githubusercontent.com/15076665/92696012-43fb5980-f384-11ea-9c19-0c8689bc6b83.png" width="720">

### Advanced DynamoDB

<img src="https://user-images.githubusercontent.com/15076665/92696241-8de43f80-f384-11ea-897b-5668a7c43780.png" width="720">

- Trandition cache has only read-cache
- DAX has both (read-cache, write-cache)

<img src="https://user-images.githubusercontent.com/15076665/92696488-eb788c00-f384-11ea-80db-e15e254ab3fd.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92697644-7e65f600-f386-11ea-892a-fc67c7f3e84f.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92697894-c1c06480-f386-11ea-9c6a-a540c9e931c5.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92698141-fd5b2e80-f386-11ea-8f0b-d242856476ab.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92698300-2bd90980-f387-11ea-910c-ba8327ab84d3.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92698610-925e2780-f387-11ea-8a90-c073f289e64a.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92699194-3fd13b00-f388-11ea-9406-7a3df68e8961.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92700153-72c7fe80-f389-11ea-81d3-0638dbab2b5e.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92700683-0ef20580-f38a-11ea-8477-9bc849bc77d0.png" width="720">

### Redshift

<img src="https://user-images.githubusercontent.com/15076665/92986602-26023600-f4f7-11ea-9f74-88dfeaf658b6.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92986663-84c7af80-f4f7-11ea-9ed9-a2ba7b4465ac.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92989116-98c9dc00-f50c-11ea-9620-b571dbe5f4e2.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92989191-548b0b80-f50d-11ea-885f-56d2259fed4f.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92989214-8ac88b00-f50d-11ea-91ac-11ec5ded5709.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92989238-c8c5af00-f50d-11ea-8759-12c10be122cf.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92989265-1a6e3980-f50e-11ea-895a-6a17893a96de.png" width="720">

### Aurora

<img src="https://user-images.githubusercontent.com/15076665/92989327-7933b300-f50e-11ea-88a7-09b6fbe118d6.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92989347-b5ffaa00-f50e-11ea-95d6-a50bf125c702.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92989393-0aa32500-f50f-11ea-8947-e17905e1d545.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92989442-6c638f00-f50f-11ea-9ad1-acfe02e6bd3b.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92989481-a896ef80-f50f-11ea-8d30-1a97568b10a3.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92989711-30312e00-f511-11ea-8d0f-098ff9837244.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92989750-71294280-f511-11ea-9bd4-1c1385845fa8.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92989775-aa61b280-f511-11ea-8f2d-5f9f9899b05d.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92989786-bc435580-f511-11ea-8c24-85b2643649c1.png" width="720">

> Create Aurora Replica from MySQL: create Reader, Writer replica

<img src="https://user-images.githubusercontent.com/15076665/92990473-c8321600-f517-11ea-93f4-8c17836c0875.png" width="720">

### ElasticCache

<img src="https://user-images.githubusercontent.com/15076665/92990508-04657680-f518-11ea-86a9-d28577fb0e9b.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92990527-28c15300-f518-11ea-9e4b-92ca78eedba0.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92990574-7a69dd80-f518-11ea-976f-ff4307287689.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92990591-940b2500-f518-11ea-96c7-087bb580cad9.png" width="720">

### AWS DMS (Database migration service)

<img src="https://user-images.githubusercontent.com/15076665/92990606-bb61f200-f518-11ea-8e8b-ae38081d75a0.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92990889-d3d30c00-f51a-11ea-94b1-e5bf638b4b18.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92990927-067d0480-f51b-11ea-819c-4e5d32064beb.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92990960-45ab5580-f51b-11ea-94de-c93ab726be37.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92991042-bce0e980-f51b-11ea-820a-df6d5201798a.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92991120-514b4c00-f51c-11ea-8a50-307784912e50.png" width="720">

### Caching stategies on AWS

<img src="https://user-images.githubusercontent.com/15076665/92991134-822b8100-f51c-11ea-8549-7fc582a46cc9.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92991171-d59dcf00-f51c-11ea-806b-c9e1b9a1636d.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92991190-1269c600-f51d-11ea-8859-7aea4e110361.png" width="720">

### EMR overview

<img src="https://user-images.githubusercontent.com/15076665/92991388-717c0a80-f51e-11ea-80bc-03d2d8866c1e.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92991407-983a4100-f51e-11ea-89f1-cf0fe5dfd337.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92991466-e2232700-f51e-11ea-8257-db0149943434.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92991486-0aab2100-f51f-11ea-85ff-e251c50ebace.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92991518-4ba33580-f51f-11ea-82ce-8d143644f3b1.png" width="720">

Logs are stored at Master node, if you lose Master node all logs will be losed too. And this is the solution:

<img src="https://user-images.githubusercontent.com/15076665/92991552-9de45680-f51f-11ea-92c8-b27138baac31.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92991590-f61b5880-f51f-11ea-9c51-71e19a6fb0ee.png" width="720">

### Database Summary

<img src="https://user-images.githubusercontent.com/15076665/92995344-c11dfe80-f53d-11ea-947a-dd78a442638b.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92995381-1823d380-f53e-11ea-9b22-3bb48eae8031.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92995393-37bafc00-f53e-11ea-95b2-19170e41eee5.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92995415-79e43d80-f53e-11ea-9bc1-2346d50bc9bc.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92995438-b44dda80-f53e-11ea-8bea-fd6d8bdceffd.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92995650-3a1e5580-f540-11ea-8bac-6238b7fb7e09.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92995681-794ca680-f540-11ea-8670-718d1d2960e9.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/92995723-cfb9e500-f540-11ea-91ca-6b9223bc155a.png" width="720">

## Advanced IAM

### IAM Policies

<img src="https://user-images.githubusercontent.com/15076665/93007866-c5333600-f5a8-11ea-911c-42288ae75e7e.png" width="720">

> When we have two or three colons, that means the resource is global so the region or account id can be omitted.

Policy is JSON Document and has the list of the statements (each statement matches an AWS API request - any actions you perform against AWS: start EC2 instance, create DynamoDB table, ...)

We have two types of policy:
1. Identity policy: attached to user, group or role (permission)
2. Resource policy: attached to resource (EC2, DynamoDB - permission to resource)

Policies have no effect until attached

An example of policy

> Sid: human readable string

<img src="https://user-images.githubusercontent.com/15076665/93007960-2c9db580-f5aa-11ea-87d9-29db4215f2db.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/93007960-2c9db580-f5aa-11ea-87d9-29db4215f2db.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/93008052-3d9af680-f5ab-11ea-9ea5-6cafc394540d.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/93008103-02e58e00-f5ac-11ea-8d97-223f5ea9f053.png" width="720">

## Route53

### Simple Routing

Set TTL in Edit record set (Route53): 100ms <=> if you go to ap-northeast-1 instance, it will keep you there in 100ms (TTL)

<img src="https://user-images.githubusercontent.com/15076665/93008336-886a3d80-f5ae-11ea-99f9-8a4ebbc4ad35.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/93008618-b0a76b80-f5b1-11ea-8791-60c796b62112.png" width="720">

### Weighted Routing

<img src="https://user-images.githubusercontent.com/15076665/93008711-c23d4300-f5b2-11ea-84a1-fc7e45a70dac.png" width="720">

### Latency-based Routing

<img src="https://user-images.githubusercontent.com/15076665/93008811-26143b80-f5b4-11ea-9826-8b585d25d223.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/93008823-4fcd6280-f5b4-11ea-92ec-c04ffffee402.png" width="720">

### Failover Routing 

<img src="https://user-images.githubusercontent.com/15076665/93008883-0b8e9200-f5b5-11ea-8821-8c38c2541d20.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/93008915-70e28300-f5b5-11ea-9a6b-7c4a99373f6e.png" width="720">

### Geolocation Routing

<img src="https://user-images.githubusercontent.com/15076665/93008950-ff570480-f5b5-11ea-83aa-7fcb039173ba.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/93008964-231a4a80-f5b6-11ea-8c39-cf75a60ca8e3.png" width="720">

### Geoproximity Routing

<img src="https://user-images.githubusercontent.com/15076665/93009457-6d062f00-f5bc-11ea-8ed2-be7541af0d27.png" width="720">

### Multivalue answer policy

Same with simple routing with only one key different (allow you to put a health check on each record)

The difference between A and CNAME records is:
- A: same with your yellow pages (PeopleName - PhoneNumber)
- CNAME: same with your nickname (batman or superman, etc...)

<img src="https://user-images.githubusercontent.com/15076665/93009615-16015980-f5be-11ea-80f6-6712f1a37ab4.png" width="720">

<img src="https://user-images.githubusercontent.com/15076665/93009632-43e69e00-f5be-11ea-85f7-ea8dc4cc40ec.png" width="720">

## VPC

### Global accelerator

<img width="720" src="https://user-images.githubusercontent.com/15076665/93206155-ee63ea00-f793-11ea-8f6b-8312d31df978.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93206415-54e90800-f794-11ea-965f-02ff5498259e.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93206618-a6919280-f794-11ea-8f47-decb03cb1123.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93206717-d2147d00-f794-11ea-8cff-ba6cc987e42d.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93206957-2fa8c980-f795-11ea-8da7-b9afaac196f7.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93207112-6f6fb100-f795-11ea-9103-2df5f9720fc5.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93207215-9b8b3200-f795-11ea-90b1-bf07d3c80197.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93207451-f3299d80-f795-11ea-9a27-e5b00c8619b1.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93207623-31bf5800-f796-11ea-9484-36d5dafa1fa5.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93209283-dcd11100-f798-11ea-8080-6149821025a3.png">

### VPC Endpoint

Two types:
- Interface Endpoints
- Gateway Endpoints: support S3 and DynamoDB

Go to outside via VPC endpoint not by NAT Gateway

<img width="720" src="https://user-images.githubusercontent.com/15076665/93209777-8adcbb00-f799-11ea-8f86-7a020b68e24d.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93282404-4f79d500-f809-11ea-84e9-475b6df83f88.png">

### AWS Privatelink

<img width="720" src="https://user-images.githubusercontent.com/15076665/93285503-f19cbb80-f80f-11ea-9574-9f38bf0b55f6.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93285675-65d75f00-f810-11ea-9c83-7f7ee4434b7f.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93285811-b51d8f80-f810-11ea-81fd-a59b1ab82a20.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93285898-e9914b80-f810-11ea-9160-6bbf86546eb3.png">

### AWS Transit gateway

<img width="720" src="https://user-images.githubusercontent.com/15076665/93286194-9b307c80-f811-11ea-959a-ddc96e8482f3.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93286258-cb781b00-f811-11ea-8986-3bdbc097ca3d.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93286344-024e3100-f812-11ea-97be-311493a98c88.png">

### AWS Network cost

<img width="720" src="https://user-images.githubusercontent.com/15076665/93286604-9b7d4780-f812-11ea-9542-baa418b8c865.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93286705-c5366e80-f812-11ea-98c7-e241bece9669.png">

### Exam tips

<img width="720" src="https://user-images.githubusercontent.com/15076665/93289855-5fe67b80-f81a-11ea-9e07-92ccbb88c040.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93289982-a63bda80-f81a-11ea-87ee-5f672ed2b643.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93290074-e0a57780-f81a-11ea-9c87-79bbb07660b0.png">

> NAT gateway does not behind the Security group, it exists on it own

<img width="720" src="https://user-images.githubusercontent.com/15076665/93290205-2b26f400-f81b-11ea-89fb-17bd97d4dbb8.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93290578-02532e80-f81c-11ea-8b41-1cbbb655e0e9.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93290670-33336380-f81c-11ea-98d8-50ae9ee96677.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93290750-6118a800-f81c-11ea-99c3-87a9e600bc80.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93290843-9c1adb80-f81c-11ea-9451-a0acb7cf6937.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93290951-d6847880-f81c-11ea-83c3-fa07e31f98a1.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93291017-fcaa1880-f81c-11ea-930b-c3b281106b68.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93291065-1fd4c800-f81d-11ea-9029-c091aa5e880f.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/93291130-3f6bf080-f81d-11ea-9607-8bdb71d58937.png">


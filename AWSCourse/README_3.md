Summarize AWS Certified Developer - Associate

### Database 101

RDS has two key features:
- Multi AZs - for disaster recovery
- Read replica - performance

If one RDS has failed, EC2 will automatically update DNS to point to another RDS (Multi AZs)

<img width="720" src="https://user-images.githubusercontent.com/15076665/92550044-a3c70700-f295-11ea-9a02-2ae6ca73080d.png">
(Multi AZs)

<img width="720" src="https://user-images.githubusercontent.com/15076665/92550274-218b1280-f296-11ea-835e-04e402b88782.png">
(Read replicas)

RDS runs on Virtual Machine and you can not access to that machine by SSH

<img width="720" src="https://user-images.githubusercontent.com/15076665/92680252-629e2800-f365-11ea-9690-bb62e100ff96.png">

### RDS Backup

<img width="720" src="https://user-images.githubusercontent.com/15076665/92680554-130c2c00-f366-11ea-8695-21e63e6cd16a.png">

RDS Automated backup is default and the backup data is stored at S3

<img width="720" src="https://user-images.githubusercontent.com/15076665/92680734-9af23600-f366-11ea-9505-b1250b33f1b0.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92687846-38edfc80-f377-11ea-806a-e102a025432f.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92688311-1dcfbc80-f378-11ea-8d75-b9ad141b3161.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92688580-87e86180-f378-11ea-8c9f-58c130ed2bc9.png">

Multi AZ is available for the following databases:
- SQL Server
- Oracle
- MySQL Server
- PostgreSQL
- MariaDB

<img width="720" src="https://user-images.githubusercontent.com/15076665/92689952-ffb78b80-f37a-11ea-9d7a-39cecea04420.png">

Read replica is available for the following databases:
- Oracle
- MySQL Server
- PostgreSQL
- MariaDB
- Aurora

<img width="720" src="https://user-images.githubusercontent.com/15076665/92690098-44dbbd80-f37b-11ea-9c0f-9b3d1a3ccc1e.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92690151-69d03080-f37b-11ea-8250-4b665cb2cd60.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92694246-bae32300-f381-11ea-9f72-c82ee943ed87.png">

### DynamoDB

<img width="720" src="https://user-images.githubusercontent.com/15076665/92695507-81131c00-f383-11ea-8945-1f998fb8acd2.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92695882-14e4e800-f384-11ea-9b52-55d0c9be23c8.png">

(One second rule for strong consistency)

<img width="720" src="https://user-images.githubusercontent.com/15076665/92696012-43fb5980-f384-11ea-9c19-0c8689bc6b83.png">

### Advanced DynamoDB

<img width="720" src="https://user-images.githubusercontent.com/15076665/92696241-8de43f80-f384-11ea-897b-5668a7c43780.png">

- Trandition cache has only read-cache
- DAX has both (read-cache, write-cache)

<img width="720" src="https://user-images.githubusercontent.com/15076665/92696488-eb788c00-f384-11ea-80db-e15e254ab3fd.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92697644-7e65f600-f386-11ea-892a-fc67c7f3e84f.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92697894-c1c06480-f386-11ea-9c6a-a540c9e931c5.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92698141-fd5b2e80-f386-11ea-8f0b-d242856476ab.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92698300-2bd90980-f387-11ea-910c-ba8327ab84d3.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92698610-925e2780-f387-11ea-8a90-c073f289e64a.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92699194-3fd13b00-f388-11ea-9406-7a3df68e8961.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92700153-72c7fe80-f389-11ea-81d3-0638dbab2b5e.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92700683-0ef20580-f38a-11ea-8477-9bc849bc77d0.png">

### Redshift

<img width="720" src="https://user-images.githubusercontent.com/15076665/92986602-26023600-f4f7-11ea-9f74-88dfeaf658b6.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92986663-84c7af80-f4f7-11ea-9ed9-a2ba7b4465ac.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92989116-98c9dc00-f50c-11ea-9620-b571dbe5f4e2.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92989191-548b0b80-f50d-11ea-885f-56d2259fed4f.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92989214-8ac88b00-f50d-11ea-91ac-11ec5ded5709.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92989238-c8c5af00-f50d-11ea-8759-12c10be122cf.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92989265-1a6e3980-f50e-11ea-895a-6a17893a96de.png">

### Aurora

<img width="720" src="https://user-images.githubusercontent.com/15076665/92989327-7933b300-f50e-11ea-88a7-09b6fbe118d6.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92989347-b5ffaa00-f50e-11ea-95d6-a50bf125c702.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92989393-0aa32500-f50f-11ea-8947-e17905e1d545.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92989442-6c638f00-f50f-11ea-9ad1-acfe02e6bd3b.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92989481-a896ef80-f50f-11ea-8d30-1a97568b10a3.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92989711-30312e00-f511-11ea-8d0f-098ff9837244.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92989750-71294280-f511-11ea-9bd4-1c1385845fa8.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92989775-aa61b280-f511-11ea-8f2d-5f9f9899b05d.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/92989786-bc435580-f511-11ea-8c24-85b2643649c1.png">

> Create Aurora Replica from MySQL: create Reader, Writer replica

<img width="720" src="https://user-images.githubusercontent.com/15076665/92990473-c8321600-f517-11ea-93f4-8c17836c0875.png">

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

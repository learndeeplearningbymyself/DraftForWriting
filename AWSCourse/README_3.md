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

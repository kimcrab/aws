## 1. Route 53
- In AWS, the most common records are
  - A: hostname to IPv4
  - AAAA: hostname to IPv6
  - CNAME: hostname to hostname
  - Alias: hostname to AWS resource
- TTL is mandatory for each DNS record
- CNAME is not for ROOT domain.
- If you buy domain on 3rd party website, you need to update NS records on 3rd party website to use Route 53 name servers.


## 2. S3
- Buckets are defined at the region level.
- It is best practice to version your buckets.
- Do not put your credentials on EC2. Use IAM Roles instead.
- S3 Storage Classes
  - S3 Standard-General Purpose: mobile application, content distribution
  - S3 Standard-Infrequent Access(IA): data store for disaster recovery, backups
  - S3 One Zone-Infrequent Access: same as IA but data is stored in a single AZ
  - S3 Intelligent Tiering: S3 Standard + Automatically moves objects based on access patterns.
  - Glacier: minimum storage duration of 90 days.
  - Glacier Deep Archive: minimum storage duration of 180 days.

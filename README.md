#  Wordpress installation via bastion server using AWS-CLI



#### Configure AWS CLI using the below command.

```sh
$ aws configure
AWS Access Key ID [None]:XXXXXXXXXXXX 
AWS Secret Access Key [None]: XXXXXXXXXXXXXXXX
Default region name [None]: us-east-2
Default output format [None]: json

```

#### Creating VPC.

```sh
$ aws ec2 create-vpc--cidr-block 172.16.0.0/16 --query Vpc.VpcId --output text
vpc-03085adf5b5ffa75e
```

Create a subnet in your VPC with a 172.16.0.0/18 CIDR block.  (Here, I am creating it in the us-east-2a availability zone.  If no availability zone is specified, a subnet will be created in any of the availability zones in the us-east-2 region)

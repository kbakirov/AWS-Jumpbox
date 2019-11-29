# AWS-Jumpbox Install
## **Aim:**
> From "Jumpbox" *(aka Bastion host)* access to "Final instance" which is located in private subnet and ping "google.com".

### Below is the architecture of Jumpbox:

![Architecture](Architecture_of_Jumpbox.png)

## **Defining Services:**
|    Services     | Given name         | IPv4 |
|      ---       |  ---         |  --- |
| `VPC`          | GlobalVPC    | 10.0.0.0/16 |
| `Internet Gateway` | IGWGlobal    | Attached to GlobalVPC  |
|`Public Subnet` | PublicGlobal | 10.0.1.0/24|
|`Private Subnet`| PrivateGlobal| 10.0.2.0/24|
|`Jumpbox`       | Jumpbox      | 54.197.7.194 (public)|
|`NAT Instance`  | NAT Instance | 18.206.89.131 (public)|
|`Final Instance`| Final Instance| 10.0.2.55 |

## **Steps to install:**
### **1 step**
> Create a VPC

GlobalVPC with IPv4 10.0.0.0/16

> Attach Internet Gateway

![VPC](VPC.png)



### **2 step**
> Create Public Subnet

PublicGlobal with IPv4 10.0.1.0/24

> Launch 2 EC2 instances in a Public Subnet

>>"Jumpbox" with automatically assigned public IPv4 54.197.7.194

>>To launch "NAT instance" we have to choose "amzn-ami-vpc-nat" in Community AMIs with ID - ami-00a9d4a05375b2763 (picture attached below).

![NAT](NAT_instance.png)

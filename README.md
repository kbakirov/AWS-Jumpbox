# AWS-Jumpbox Install
## **Aim:**
> From "Jumpbox" *(aka Bastion host)* access to "Final instance" which is located in private subnet and ping "google.com".

### Below is the architecture of Jumpbox:

![Architecture](Architecture_of_Jumpbox.png)

## **Defining objects:**
|    Services     | Given name         | IPv4 |
|      ---       |  ---         |  --- |
| `VPC`          | GlobalVPC    | 10.0.0.0/16 |
| `InterGateway` | IGWGlobal    | Attached to GlobalVPC  |
|`Public Subnet` | PublicGlobal | 10.0.1.0/24|
|`Private Subnet`| PrivateGlobal| 10.0.2.0/24|
|`Jumpbox`       | Jumpbox      | 54.197.7.194 (public)|
|`NAT Instance`  | NAT Instance | 18.206.89.131 (public)|
|`Final Instance`| Final Instance| 10.0.2.55 (no public)|

## **Steps to install:**
> We create a VPC

# VPC DESIGN

To design and set up a Virtual Private Cloud with both public and private subnets.Implement routing, security groups, and network access control lists(NACLs) to ensure proper communication and security within the VPC. Working in the AWS eu-west-1 (Ireland) region.

Creating VPC
Log-in to AWS and navigate to AWS management console. Select VPC and set it up with the requirements.

![image](https://github.com/user-attachments/assets/dbcd4989-0183-4e87-ad22-f4f1218fbdca)
![image](https://github.com/user-attachments/assets/ffd0a033-c0f6-40ba-8182-1dc4c00ffdd1)

Creating Subnets:
Create both pblic and private subnet by selecting create subnet and use the ID of already created VPC.

Public Subnet

![image](https://github.com/user-attachments/assets/5e92c112-6579-4bb8-8ffa-1746571cbe8d)

Private Subnet

![image](https://github.com/user-attachments/assets/62d91894-cc89-4278-9c81-25c4df1b62b2)

Configuring and attaching Internet gateway(IGW) to the VPC
![image](https://github.com/user-attachments/assets/09d11010-d1d7-4cc7-b31a-6f09ed7e7247)

Configuring Route Tables and associating it with subnets:

Public Route Table association with route to IGW 

![image](https://github.com/user-attachments/assets/0d37c621-3161-43e4-bb69-af117568a4af)
![image](https://github.com/user-attachments/assets/c3ea196f-f7fa-4ef1-94e2-04dec811e322)

Private route table association

![image](https://github.com/user-attachments/assets/f242a207-aaef-4fcc-be94-6b51a3ef1fd2)

Configuring and creating NAT gateway in the public subnet with Elastic IP

![image](https://github.com/user-attachments/assets/612fc086-9d17-4e43-9236-62b18a5b6460)
![image](https://github.com/user-attachments/assets/5d9d89fc-b563-448b-94a1-be098dffe26b)

Updating private route table to route traffic to the NAT gateway

![image](https://github.com/user-attachments/assets/912320cd-4beb-40f4-8434-59dd39cff3e4)

Setting up security groups:

Security group for public instances

![image](https://github.com/user-attachments/assets/233a530c-3375-4253-a1b6-cae9e1c04669)
![image](https://github.com/user-attachments/assets/afcf8df8-012c-464f-91a3-e3ef128f09e8)
![image](https://github.com/user-attachments/assets/896c0744-54f8-4ec5-8f60-a5ea50234bcb)
![image](https://github.com/user-attachments/assets/cdd3ce7e-fc5f-478a-bd48-6f08433970b1)
![image](https://github.com/user-attachments/assets/035f8ac3-7b78-4860-bc4d-2c4ffec96682)

Security group for private instances

![image](https://github.com/user-attachments/assets/5337b73c-c894-40bd-a464-5d5e4d5ee957)
![image](https://github.com/user-attachments/assets/dc0b6c23-cc9e-47b3-8442-631f8586f68d)
![image](https://github.com/user-attachments/assets/c4876e9c-163e-40e4-86ad-e16215d0db6a)

Network ACLs(NACLs):

Public Subnet NACL

![image](https://github.com/user-attachments/assets/20434fe3-622e-4085-8812-a84d18a86675)
![image](https://github.com/user-attachments/assets/91421bb3-875b-4b32-9d77-cfaf3b16e734)

Private Subnet NACL
![image](https://github.com/user-attachments/assets/d7698789-af5f-4031-8ca5-0ef4c6ed8d65)

![image](https://github.com/user-attachments/assets/e3c50deb-7a30-4ced-bff8-da7f57517546)


Launching EC2:

Launching EC2 instance in the Public subnet

![image](https://github.com/user-attachments/assets/2ef592c7-0823-4abc-a69c-940b140c245e)
![image](https://github.com/user-attachments/assets/1463830a-5e41-45f9-b936-ec2a39a639c7)
![image](https://github.com/user-attachments/assets/74af37ea-7367-4fbf-927e-80feaee8cc3e)




Launching EC2 instance in the Private subnet

![image](https://github.com/user-attachments/assets/16dd50f6-abc1-40d3-a50a-ad443604a7bb)
![image](https://github.com/user-attachments/assets/eb8e0ef4-ee22-4506-99e4-65587b3b1645)

PURPOSE AND FUNCTION OF COMPONENTS

Virtual Private Cloud(VPC): This is a logicaly, secure isolated environment within a public cloud that allows organizations to define and control their own virtual network. It is a private cloud hosted within a pupblic cloud providers infrastructure like AWS.

Subnets: 
Pupblic subnet: It is a subnet associated with a route table that has a route to internet gateway. It allows resources within it to access the public internet and be accessible from it.
Private subnet: It is a network segment within a VPC that does not have a direct route to the internet. The resources within it require a Network Address Translation(NAT)device to connect to the internet. 

Internet gateway(IGW):
NAT gateway:
Route Tables:
Security groups:
Network access control list(NACLs): Used to add additional security to subnets.



























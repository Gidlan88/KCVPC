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
























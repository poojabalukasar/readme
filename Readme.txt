Q.1
Ans:Basic aspects of AWS elastic compute cloud(EC2):
1.aws ec2 provides scalable computing capacity in the aws cloud.
2.by using ec2 service of aws we can create instance of virtual machines and easily configuer the capacity of instance as per user requirement.
3.ec2 also allows users to build apps to automate scaling according to changing needs and peak perides and makes it simple to
 deploy virtual servers and manage the storages.
4.the pricing of ec2 service is based on hours and size of an istance,region and operating system(Amazon Machine Image).

Q.2
Ans:
1.open AWS console.
2.select region in which we want to create virtual machine instance.
3.in servies select compute servie and in compute service select ec2 service.
4.in instances------click on launch instance there are 7 steps to create instance
1.choose an Amazon machine image(AMI)
ex:red hat enterprise linux
2.choose an instance type
ex:t2.micro
3.configure instance-------network type,avability zone etc.
4.add storage-------add hard disk
5.add tag--------this field is optional  
6.configure security group-------add  security 
7.review------show all details we were selected   
then select key pair either existing or create new key pair and then select key pair that you created.
then select aknowledgement check box and then choose launch instance.
view the instances-----show the instance we created.
To connect the instance .........
select the instance and click on connect then select either ec2-user or root user .



Q.3
Ans:
1.launch ec2 instance.
2.connect ec2 instance----either ec2-user or root user.
3.to install apache server 
   #yum install http* -y
   #systemctl start httpd
   #systemctl enable httpd
   #systemctl restart httpd


Q.4
Ans:
 create ec2 instance:
1.launch the ec2 instance with network  choose the VPC that the RDS DB  instance uses .
2.choose the  alltrafic protocol security group.

configure the RDS MySQL DB  instance
1.create database instance of MySQL in same VPC and same security group.
 
connect the RDS MySQL DB instance from ec2 instance:

1.select ec2 instance click on connect and connect throgh root user.
#sudo su 
#yum install mysql -y
#mysql -h endpoint -u username -p
endpoint--------RDS MySQL instance endpoint 
-u username -------username of database
then enter password
connect.      



Q.5
Ans:
1.register the custom domain with route53
2.create two buckets using amazon s3 service.
3.configure your root domain bucket for website hosting.
4.configure your subdomain bucket for website redirect.
5.configure logging for website traffic.
6.upload index and website content.
7.edit s3 block public access settings.
8.attach a bucket policy.
9.test the domain endpoint.



Q.6
Ans:there are two ways to host website from aws by usings ec2 service:
1.create aws  ec2 instance with web site code.--------hit it using instance public IP address.

2.create aws ec2 instance and connect it using either ec2-user or root user.
then install apache server 
#yum install http -y
#systemctl start httpd
#systemctl enable httpd
#echo hello this is my website..............................!!!!!!!!!!!!!!!!!!!!!!!! > /var/www/html/index.html
#systemctl restart httpd
then host the website by using the public IP address or DNS server.



Q.7
Ans:in aws process some key factors are same regions and availability zones.
same VPC and subnet.
security group according to protocol service.

Q.8
Ans:
clean up the project environment is very important because in aws every service has specified cost.
to avoid more cost alway terminate or stop the used services is important.
alway see the running services and it is not in used then terminate it.
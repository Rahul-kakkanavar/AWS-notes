# AWS-notes/creating EBS & attaching it 
to attach the EBS(ELASTIC BLOCK STORAGE) to EC2 instance 
1.create an EC2 instance 
2.go to storage after instance start runing 
3.creat a EBS vloume 
4.take the remote control 
5.1st commond:- sudo su -
6.2nd commond:- lsblk -l
7.  we have EBS volume or disk name:- /dev/xvdf/ 
    now we are going to creat a partition in it 
    only partition we are creating :- /dev/xvdf1
8. run a commond:- fdisk /dev/xvdf
   we will enter in it 
9.the pess:- p (partition)
10. it will shown no partition in it 
11. now press n (to creat new partition in the volume)
12. now it will ask for what kind of partition you want 
    #primary partition (0 primary, 0 extended, 4 free)    
    #extended (containor for logical partition)
13.in order to get primary partition press p
    after pressing asks for (1-4; default 4) 
14.now press 1
15. now press 2time enter that means you are taking entire 15gb;
    space 
16. for saving press w and enter 
17. we need to fromate this partition 
    you need to assign a file system to this partition 
18. commond:- mkfs. xfs /dev/xvdf1 
19. pysicaly it is attaced 
 but to attaced to your os we have to you make one directry here 
20. write a commond:- mkdir /mnt/dd1
21. next "mount dev/xvdf1 /mnt/dd1"
22. now this is successfully mounted to you os 
23. now to change the directy "cd /mnt/dd1"
    now you are in new connected disk 

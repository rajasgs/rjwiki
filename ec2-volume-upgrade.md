/ [Home](index.md)

## How to upgrade volumne in Ec2


- Log into the AWS Management Console

- Make sure that the Instance that you wish to change is not currently running

- Navigate to Elastic Block Store > Volumes

- Check the box next to the Volume that needs more space

- Click the More… drop down list and select Create Snapshot

- Enter a Name and a Description

- Navigate to Elastic Block Store> Snapshots

- Monitor the progress of the Snapshot for completion

- Once complete, navigate back to Elastic Block Store > Volumes

- Click Create Volume

- Enter the desired size for the new volume

- Make sure that you select the same Availability Zone for your instance

- Select the Snapshot that you just created

- Click Yes, Create

- Monitor the progress of the Volume for completion

- Once complete, Check the box next to the Volume that is currently connected to the Instance

- Make sure that no other Volumes are selected

- Click the More… drop down list and select Click the More… drop down list and select Detach Volume

- Uncheck the box selected and check the box next to the new Volume

- Click the More… drop down list and select Click the More… drop down list and select Attach Volume

- Select the Instance that you wish to change

- Change the value in Device from xvdf  to /dev/sda1

- Click Yes, Attach

- Navigate to Instances and start your Instance

- Once you are satisfied that the volume works, feel free to delete the Snapshot and old Volume if you like


[AWS Change Disk](http://www.messor.com/increase-disk-size-for-an-ec2-instance-in-aws/)
# openstack_instanceVM_guide

STEPS TO CREATE AN INSTANCE WITH HORIZON DASHBOARD

Step 1: Access and login into Horizon Dashboard

  - Access URL Address in browser:  http://192.168.50.12/horizon
  
  - Login with Openstack user account


Step 2: Launch an instance

  Open page Project → Compute → Instances and then click button Launch Instance
	
	In tab Details, fill out the required fields
	
	In tab Access & Security, select an imported keypair or import a new keypair to ssh to 	instance.
	
	To import a new keypair:
		- copy and paste in Public Key field the contents of the public key file in the machine which you want to ssh from.  
		  (The public key file default is /home/<username>/.ssh/id_rsa.pub)
		- fill out the keypair name

	In tab Networking, selected network is your internal network.


Step 3: Associate Floating IP

	Select Associate Floating IP from Actions Column of the instance

	Click to (+) button

	Select Pool as your external network to Allocate IP
	

Step 4: SSH to your instance

  You must point your private key suitable with you keypair which you chossed in step 2

  With ubuntu image, the command line is:

  ssh -i <your_private_key> ubuntu@<your_instance_IP>

# flask - project
Agenda:
Using Terraform to create a VM in Google Cloud.
Starting a basic Python Flask server.

Tools used :
Terraform

Steps:
Creating a project in google cloud platform.
Setting up a service account key (key type : json ), which Terraform will use to create and manage resources in this Google Cloud project.
  Setting up terraform :
    - Creating a main.tf (The contents of this file describe all of the Google Cloud resources that will be used in the project.)
    - Download the latest version of the Google cloud terrafrom provider and build a .terraform directory.

Creating a compute instance:
  - Initialize terraform again to download and install an extra plugin for naming a random instance id.
  - Get the preview of what will be craeted
  - Run (terraform apply) through which terraform call the Google cloud API's to create an instance.
  - Now instance is created.
SSh access to compute engine instance :
  - Add a public SSH key to the Compute Engine instance to access and manage it by modifying a terraform file.
  - Again see the preview of what is going to be implemented
  - Apply the changes.

Use a terraform varaible which is helper to expose the instance's ip address.
Apply the changes 
Get the instance ip address
Making sure firewall rule to be in place before you can use SSH to connect to the instance.
Validate everything by connecting the ip address with SSH.

Building a Python flask server app:
- Building an app so that you can have a single file describing your web server and test endpoints.
- Adding a new python file with a greeting and running it
- Confirm the greeting is returned by running curl ( flask serves traffic through - localhost:5000 ).
- Open the port 5000 on the instance through a change in terraform file and review the plan and apply to create the firewall rule.
- Point the ip and port to browser to confirm the server is up and running.

Destroying all the resourses in terraform file using command terraform destroy.


    
    

# Introduction To Linux Admiistration and Shell Scripting # 

## **Capstone Project: Shell Script for AWS IAM Management.** ##

Before diving straight into the project, let's briefly discuss what Shell Script and AWS IAM is about.

### Shell Script. ###
Shell scripting is a text file with a list of commands that instruct an operating system to perform certain tasks.
 A shell is an interface that interprets, processes, and executes these commands from the shell script. It can be particularly helpful to automate repetitive tasks, helping to save time and reduce human error. 

 ### AWS IAM Management ###
 AWS Identity and Access Management (IAM) is a web service that helps you securely control access to AWS resources. With IAM, you can manage permissions that control which AWS resources users can access.
  You use IAM to control who is authenticated (signed in) and authorized (has permissions) to use resources. IAM provides the infrastructure necessary to control authentication and authorization for your AWS accounts.

Having explained what Shell Scripting and AWS IAM mean, we can therefore see the connectivity of these 2 as  writing some shell script that will automate IAM in our AWS console.

### Project Scenario ###

Datawise Solutions requires efficient management of AWS
Identity and Access Management (IAM) resources. The company is expanding its team and needs to onboard five new employees to access AWS resources securely.

### Purpose ###

In this capstone project, you will extend your shell scripting capabilities by creating more functions that extends the
"aws_cloud_manager.sh" script.

### Objectives: ###

1. Script enhancement
2. Define IAM user names array
3. Create IAM users
4. Create IAM group
5. Attach administrative policy to group
6. Assign users to group

Note: The ability to execute anything on this project, is the exsitence execution of our previous mini project that deals with  **Setting up secure authentication to AWS API.**


![use](<Shell-Scripting Pics/1.Use-text-editor.jpg>)
First step to take on is to open your local terminal and create your file that the script will sit in with a text editor.
There are lot of text editors to make use of e.g Vi, Vim, nano, even vscode, e.t.c. 
I decided to use nano text editor as it is my choice, which means you can also make use of any other text editor of your choice that you're use with.
The name given to our file as instructed in the project is "aws_cloud_manager.sh"

![script](<Shell-Scripting Pics/2.The-Script.jpg>)
![script](<Shell-Scripting Pics/3The-Script2.jpg>)
The image above here describes a well detailed script for this project. Please ignore numbering arrangement and focus on every single writing of the script for a better understanding.

To exit out of this nano text editor, you'll need to use `^X`, and then an option to press X and enter key.



![Exe](<Shell-Scripting Pics/4.Execute.jpg>)
Before any/the script could be able to run after writing it, there must be an initiation of an executing permission with the use of command `chmod +x` .


![Run](<Shell-Scripting Pics/5.Run-script.jpg>)
This is the command to run the script.

![ll](<Shell-Scripting Pics/6.Error.jpg>)

This is an error from a wrong configuration of CLI. 
Remember in our previous mini project whereby we configured CLI, by getting the Access Key and Secret Access Key of an IAM user. But here, we want to create an IAM user in our AWS console(Root user).
As it is known in default settings, that you can't create an IAM User in an AWS IAM User account without a given permission to do so in our Root User.




    
  ![alt text](<Shell-Scripting Pics/8.Access-keys.jpg>)
  Troubleshooting the error is to have a right configuration by getting the Access Key and Secret Access Key of our AWS Root User account.
 We'd need to go into our AWS console and create the access key for configuration.

 ![TS](<Shell-Scripting Pics/9.error@troubleshoot.jpg>)
 `aws configure` is the command to use. 
    Then you will input the details you got from the Rrecent configuration with a correct region name. You'll get another error in the image above if you input the incorrect region name.

![Out](<Shell-Scripting Pics/10.Outcome.jpg>)
![Out2](<Shell-Scripting Pics/11.Outcome2.jpg>)
This is the output result of the script on the local terminal.


![console](<Shell-Scripting Pics/12.interface.jpg>)
![face](<Shell-Scripting Pics/13.Interface2.jpg>)
This is the GUI outcome of the script.

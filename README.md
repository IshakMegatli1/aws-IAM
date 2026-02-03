# aws-IAM
<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Cloud Security with AWS IAM

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-security-iam)

**Author:** ElHalouf  
**Email:** shakyleboss@gmail.com

---

![Image](http://learn.nextwork.org/lively_blue_beautiful_jellyfish/uploads/aws-security-iam_1c864649)

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate Identity and access management in AWS using EC2 instances

### Tools and concepts

Services I used were EC2 instances, IAM, policies, users, usergroups and IAM policy Simulator. 

### Project reflection

This project took me approximately 2h

---

## Tags

### What I did in this step

In this step, I will launch an EC2 instance in AWS

### Understanding tags

Tags are labels attached to AWS resources for organization

### My tag configuration

The tag I’ve used on my EC2 instances is called ENV The value I’ve assigned for my instances are production and development

![Image](http://learn.nextwork.org/lively_blue_beautiful_jellyfish/uploads/aws-security-iam_2e0e5a5d)

---

## IAM Policies

### What I did in this step

In this step, I will create IAM policies because I need to limit the permissions of certain people on my team

### Understanding IAM policies

IAM Policies are rules for who has permission to do what with the resources

### The policy I set up

For this project, I’ve set up a policy using JSON

### Policy effect

I’ve created a policy that allows all actions 

### Understanding Effect, Action, and Resource

The Effect, Action, and Resource attributes of a JSON policy means if actions are allowed or denied, a list of actions and to what resource it's applied

---

## My JSON Policy

![Image](http://learn.nextwork.org/lively_blue_beautiful_jellyfish/uploads/aws-security-iam_1c864649)

---

## Account Alias

### What I did in this step

In this step, I will create an aws account alias to simplify sign in to the AWS Management Console for users

### Understanding account aliases

An account alias is a way to chang your AWS console's login URL with a memorable name

### Setting up my account alias

Creating an account alias took me 10 minutes Now, my new AWS console sign-in URL is ishakmegatli

![Image](http://learn.nextwork.org/lively_blue_beautiful_jellyfish/uploads/aws-security-iam_0eb4439b)

---

## IAM Users and User Groups

### What I did in this step

In this step, I will create IAM groups and users to manage users permission and give a way for my users to login

### Understanding user groups

IAM user groups are a way to group our users to give them the permissions that are associated with that group

### Attaching policies to user groups

I attached the policy I created to this user group, which means users within that user group will have the permissions that are granted by that policy

### Understanding IAM users

IAM users are long term identities for aws

---

## Logging in as an IAM User

### Sharing sign-in details

The 2 ways are console passwords and access keys

### Observations from the IAM user dashboard

Once I logged in as my IAM user, I noticed that there were resources I couldn't access.

![Image](http://learn.nextwork.org/lively_blue_beautiful_jellyfish/uploads/aws-security-iam_6f2ab446)

---

## Testing IAM Policies

### What I did in this step

In this step, I will log into the intern's IAM user because I need to test the intern's access

### Testing policy actions

I tested my JSON IAM policy by trying to delete both of my EC2 instances with the intern's account 

### Stopping the production instance

When I tried to stop the production instance I got an error. This was because the new user does not have permission to stop the production instance

![Image](http://learn.nextwork.org/lively_blue_beautiful_jellyfish/uploads/aws-security-iam_0e7a9d6a)

### Stopping the development instance

Next, when I tried to stop the development instance it got deleted. This was because the user was in a usergroup where the policy allowed users within that usergroup to delete the resources with the development tag

![Image](http://learn.nextwork.org/lively_blue_beautiful_jellyfish/uploads/aws-security-iam_1811801c)

---

## IAM Policy Simulator

To extend my project, I'm going to use the IAM policy simulator to test my policies faster.

### Understanding the IAM Policy Simulator

The IAM Policy Simulator is useful for testing your policies fast

### How I used the simulator

I set up a simulation for the new user (intern) for the dev environment policy. I tested the StopInstances action and the DeleteTags action, I had to change the instance and add the development tag for it to work. 

![Image](http://learn.nextwork.org/lively_blue_beautiful_jellyfish/uploads/aws-security-iam_069d8a621)

---

---

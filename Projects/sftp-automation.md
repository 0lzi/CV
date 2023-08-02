# SFTP Automation

## About

This project came about when we had an influx of requests to create/disable or reset passwords for SFTP users. Intead of running a bash script that was located on the SFTP server to manage User creation I decided to utilize Stackstorm which we used for other automations.

# Roles

My role was to automate the task of creating and modifiying users between the sftp servers.

The automation was created with several 'packs'. Each pack achieved a different task

- Create New User
- Password Reset User
- Disable User
- Enable User

I also wanted a way to store the user passwords securley for easier retrival for the requester so we intergated Hashicorp vault into the automation to store the passwords.

I wanted to add an extra feature that tracked tasks, as when we had a request for a password reset we would get a request saying the password they have doesnt work and we had no way to easily trace that back. So as part of the automation a hidden file was created to track each action the automation takes against a user.

# Difficulties

The most difficult part was to create a Stackstorm pack from scratch only by viewing other packs and using Stackstorms own documentation.

[Home](../index.md)
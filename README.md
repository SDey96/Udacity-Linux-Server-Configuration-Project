# Udacity - Linux Server Configuration Project

An Udacity Full Stack Web Developer II Nanodegree Project.

## About

This tutorial will guide you through the steps to take a baseline installation of a Linux server and prepare it to host your Web applications. You will then secure your server from a number of attack vectors, install and configure a database server, and deploy one of your existing Flask-based Web applications onto it.

In this project, I have set up an Ubuntu 18.04 image on a DigitalOcean droplet. The technical details of the server as well as the steps that I have taken to set it up can be found in the succeeding sections.

### Technical Information About the Project

- **Server IP Address:** 127.0.0.1
- **SSH server access port:** 2200
- **SSH login username:** grader
- **Application URL:** http://127.0.0.1

## Steps to Set up the Server

### 1. Create the RSA Key Pair

On your local machine, you will first have to set up the public and private key pair. This key pair will be later used while securely logging in with SSH. While the private key will be kept with you in your local machine, the public key will be stored in the server.

To generate a key pair, run the following command:

   ```console
   $ ssh-keygen
   ```

The whole process would look like this:

```console
subhadeep@subhadeep-VirtualBox:~$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/home/subhadeep/.ssh/id_rsa): /home/subhadeep/.ssh/udacity_project
Created directory '/home/subhadeep/.ssh'.
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/subhadeep/.ssh/udacity_project.
Your public key has been saved in /home/subhadeep/.ssh/udacity_project.pub.
The key fingerprint is:
SHA256:JnpV8vpIZqstoTm8aaDAqVmGSF/tGhtDfXAfL2fs/U8 subhadeep@subhadeep-VirtualBox
The key's randomart image is:
+---[RSA 2048]----+
|                 |
|       . . .     |
|      o + o +    |
| .   o o = o =   |
|+.o o o S . = .  |
|+o+. =.= .   . . |
|o= o.oB.=       E|
|+   *=.= +     ..|
|   .oo.o+ .     o|
+----[SHA256]-----+
```

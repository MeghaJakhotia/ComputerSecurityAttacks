# [SEED Attack Labs](https://seedsecuritylabs.org/) 

These labs cover some of the most common vulnerabilities and attacks exploiting these vulnerabilities. All the labs are presented in the form of PDF files, containing some screenshots.

## Table of Contents 

- [Getting Started](#getting-started)
- [Motivation](#motivation)
- [List of Attacks](#list-of-attacks)
- [Key Learnings](#key-learnings)
- [References](#references)


## Getting Started

These instructions will get you to set up the environment on your local machine to perform these attacks.

Step 1: Create a new VM in Virtual Box.\
Step 2: Download the image [SEEDUbuntu-16.04-32bit.zip](https://seedsecuritylabs.org/lab_env.html) from here.\
Step 3: Use the Virtual Machine Hard Disk file to setup your VM.\
Step 4: Configure the VM.

The [link](https://seedsecuritylabs.org/lab_env.html) contains a document that can be used to set up the VM without any issues.

## Motivation
The labs were completed as a part of the Computer Security (CSE643) course at Syracuse University. The course is well structured to understand the concepts of Computer Security.

## List of Attacks

1. **Environment Variable and Set-UID Vulnerability**
>*Description:* Set-UID is an important security mechanism in Unix operating systems. When a Set-UID program runs, it assumes the owner's privileges. For example, if the program's owner is root, then when anyone runs this program, the program gains the root's privileges during its execution. This can be very well exploited, as seen in the lab. The lab also demonstrates the effect of environment variables on the behavior of Set-UID programs.

2. **Buffer Overflow Vulnerability**
>*Description:*  Buffer overflow is defined as the condition in which a program attempts to write data beyond the boundaries of pre-allocated fixed-length buffers. This vulnerability can be utilized by a malicious user to alter the flow control of the program, even execute arbitrary pieces of code. The task in this lab is to develop a scheme to exploit the buffer overflow vulnerability and finally gain the root privilege.

3. **Shellshock Attack**
>*Description:* In this attack we launched the shellshock attack on a remote web server and then gained the reverse shell by exploiting the vulnerability.

4. **Race Condition Vulnerability**
>*Description:* A race condition occurs when multiple processes access and manipulate the same data concurrently, and the outcome of the execution depends on the particular order in which the access takes place. If a privileged program has a race-condition vulnerability, attackers can run a parallel process to “race” against the privileged program, with an intention to change the behaviors of the program. The task is to exploit this vulnerability and gain root privilege.

5. **Dirty COW Attack**
>*Description:* A case of race condition vulnerability that affected Linux-based operating systems and Android. We launch this attack to modify /etc/passwd file - which should not be modified without appropriate privileges and methods.

6. **Meltdown and Spectre Attack**
>*Description:* In both of these attacks, we exploit the vulnerability in the hardware protection mechanism implemented in most CPUs. Since the flaw exists in the hardware, it is very difficult to fundamentally fix the problem, unless we change the CPUs in our computers. These two attacks demonstrate the exploitation and give a greater depth of understanding in hardware security.

7. **Format String Vulnerability**
>*Description:* The format-string vulnerability is caused by code like printf(user input), where the contents of the variable of user input are provided by users. When this program is running with privileges (e.g., Set-UID program), this printf statement becomes dangerous, because it can lead to one of the following consequences: (1) crash the program, (2) read from an arbitrary memory place, and (3) modify the values of in an arbitrary memory place. The last consequence is very dangerous because it can allow users to modify internal variables of a privileged program, and thus change the behavior of the program. The task is to develop a scheme to exploit the vulnerability.

8. **Cross-Site Request Forgery Attack**
>*Description:* In this lab, we will be attacking a social networking web application using the CSRF attack. The open-source social networking application called Elgg has countermeasures against CSRF, but we have turned them off for this lab. We also study the most common countermeasures of this attack.

9. **Cross Site Scripting Attack**
>*Description:* In this lab, we need to exploit this vulnerability to launch an XSS attack on the modified Elgg, in a way that is similar to what Samy Kamkar did to MySpace in 2005 through the notorious Samy worm. The ultimate goal of this attack is to spread an XSS worm among the users, such that whoever views an infected user profile will be infected, and whoever is infected will add you (i.e., the attacker) to his/her friend list.

10. **SQL injection Attack**
>*Description:* In this lab, we have created a web application that is vulnerable to the SQL injection attack. Our web application includes the common mistakes made by many web developers. Our goal is to find ways to exploit the SQL injection vulnerabilities, demonstrate the damage that can be achieved by the attack, and master the techniques that can help defend against such type of attacks.

11. **Android Repackaging Attack**
>*Description:* Repackaging attack is a very common type of attack on Android devices. In such an attack, attackers modify a popular app downloaded from app markets, reverse engineer the app, add some malicious payloads, and then upload the modified app to app markets. Users can be easily fooled because it is hard to notice the difference between the modified app and the original app. Once the modified apps are installed, the malicious code inside can conduct attacks, usually in the background. We gain hands-on experience on the Android Repackaging attack.

12. **Android Device Rooting Attack**
>*Description:* The objective of this lab is two-fold. First, through this lab, we get familiar with the process of device rooting and understand why certain steps are needed.  Second, the entire rooting mechanism involves many pieces of knowledge about the Android system and operating system in general, so it serves as a great vehicle for us to gain such in-depth system knowledge. In this lab, we develop a complete rooting package from scratch and demonstrate how to use the package to root the Android VM.

## Key Learnings

- These attack labs give us the idea of fundamental principles of computer system security, including authentication, access control, capability leaking, security policies, sandbox, software vulnerabilities, and web security.

- Identifying the vulnerabilities and exploiting them. Further work on countermeasures as a security solution to the problem.


## References

1. http://www.cis.syr.edu/~wedu/Teaching/CompSec/labs.html
2. Computer Security: A Hands-on Approach by Wenliang Du 


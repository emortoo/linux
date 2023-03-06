# Users 

<details>
<summary>How to create a new user</summary><br>

`useradd [username]` or `adduser [username]`: This command allows administrators to create a new user account in the system. The user's information is inputted and saved to the user database.
<br>
  * Note : this command requires root or administrative privileges to execute, as indicated by the "sudo" at the beginning of the command.
  
````
sudo useradd johndoe
sudo adduser janedoe
````

</details>

<details>
<summary>How to delete an existing user</summary><br>

`userdel [username]`: This command allows administrators to delete a user account from the system. This should be used with caution and only if the user account is no longer needed.<br>
  * Note : this command requires root or administrative privileges to execute, as indicated by the "sudo" at the beginning of the command.
  
````
sudo userdel johndoe
````

</details>

<details>
<summary> How to verify if user exist </summary><br>

`cat /etc/passwd` : This command is a Linux command that would display the contents of the "/etc/passwd" file, which is a system file that stores information about user accounts on the system.<br>

````
cat /etc/passwd
````
`johndoe:x:1001:1010::/home/johndoe:/bin/bash` <br>

Each line in the file represents a user account and contains several fields separated by colons, including the username, password (encrypted or "x" indicating shadow passwords are used), user ID, group ID, home directory, login shell, and any additional information about the user.

However, please note that the password field in this file only stores an encrypted version of the password or an "x" character indicating that the password is stored in a separate file called "/etc/shadow" for security reasons. Therefore, you cannot retrieve the actual password from this file.
  
</details>

<details>
<summary>How to check user ID</summary><br>

`id [username]`: This command allows administrators to look up a user's ID number in the system. This can be useful for referencing a specific user in other commands.

````
id johndoe
````
`uid=1001(johndoe) gid=1001(johndoe) groups=1001(johndoe),1002(devops)`
  
</details>
<details>

<summary>How to modify users acoount</summary><br>

`usermod`: This command allows administrators to modify a user's account information (such as their name, ). This can be useful if a user has updated their information or if the administrator needs to correct an error. <br>

* Note : this command requires root or administrative privileges to execute, as indicated by the "sudo" at the beginning of the command.

````
sudo useradd [options] [username] 
````

Here, [options] refers to the various options available for modifying user account information, and [username] is the name of the user whose account information you want to modify.

[options]<br> 
`-c`: This option is used to add or change the comment for the user account. For example, to add a comment to the user "johndoe", you would use the following command:

````
sudo usermod -c "John Doe" johndoe 
````
`-d`: This option is used to change the home directory for the user account. For example, to change the home directory for the user "johndoe" to /home/janedoe, you would use the following command:

````
sudo usermod -d /home/janedoe johndoe 
````

`-s`: This option is used to change the default shell for the user account. For example, to change the default shell for the user "johndoe" to /bin/bash, you would use the following command:

````
sudo usermod -s /bin/bash jdoe 
````

`-l`: This option is used to change the username for the user account. For example, to change the username for the user "johndoe" to "janedoe", you would use the following command:

````
sudo usermod -l janedoe johndoe 
````
</details>

<details>
<summary>How to switch from one user to another </summary><br>

`su - [username]`: This command allows users to switch between different user accounts in the system. This can be useful if multiple users are sharing a computer or if an administrator needs to access a user's account for troubleshooting purposes.<br>

Note : this command requires root or administrative privileges to execute, as indicated by the "sudo" at the beginning of the command.

````
sudo su - root
````
</details>

<details>
<summary>How to access users home directory</summary><br>

`su [username]` : This command allows users to switch between different user home directories in the system. This can be useful if multiple users are sharing a computer or if an administrator needs to access a user's account for troubleshooting purposes.<br>
  
Note : this command may requires a password or root or administrative privileges to execute
  
````
su  janedoe
````
</details>

<details>
<summary>How to set users password</summary><br>

`passwd [username]` : This command allows admistrators to set a password for user accounts in the system. This can be useful if multiple users are sharing a computer to prevent  access to other user's account.

Note : this command requires root or administrative privileges to execute, as indicated by the "sudo" at the beginning of the command.
````
sudo passwd johndoe 
````
</details>

<details>
<summary>How to check users with password asigned to thier account </summary><br>

`cat /etc/shadow ` : This command allows admistrators to check user accounts that has been assigned a password in the system. 

Note : this command requires root or administrative privileges to execute, as indicated by the "sudo" at the beginning of the command. 
````
sudo cat /etc/shadow
````

</details>

<details>
<summary> How to add a user to a group </summary><br>
  
`usermod -a -G [groupname] [username]` : This command allows admistrators to assign users to a group. <br>

Note : this command requires root or administrative privileges to execute, as indicated by the "sudo" at the beginning of the command. 
````
sudo usermod -a -G deveops johndoe 
````
</details>
  

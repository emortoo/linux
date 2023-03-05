# Users 

<details>
<summary>How to create a new user</summary><br>

`useradd` or `adduser`: This command allows administrators to create a new user account in the system. The user's information is inputted and saved to the user database.<br>
`command`<br>
````
useradd [username]
adduser [username]
````
* Note : Only users with adminstrative privilages (sudo) will be able to add users to a system 

</details>

<details>
<summary>How to delete an existing user</summary><br>

`userdel [username]`: This command allows administrators to delete a user account from the system. This should be used with caution and only if the user account is no longer needed.<br>
`command` 
````
userdel <username> 
````
* Note : Only users with adminstrative privilages (sudo) will be able to add users to a group in the system 

</details>

<details>
<summary>How to verify if user exist </summary><br>

`cat /etc/passwd` : This command allows administrators to check if a user account already exists in the system. This can be helpful to prevent duplicate accounts from being created.

`result`
````
johndoe:x:1001:1010::/home/johndoe:/bin/bash
````
* Note : Only users with adminstrative privilages (sudo) will be able to add users to a group in the system 

</details>

<details>
<summary>How to check user ID</summary><br>

`useradd id`: This command allows administrators to look up a user's ID number in the system. This can be useful for referencing a specific user in other commands.
`command` 
````
userid  <username>
````
</details>
<details>

<summary>How to modify users acoount</summary><br>

`usermod`: This command allows administrators to modify a user's account information (such as their name, ). This can be useful if a user has updated their information or if the administrator needs to correct an error.

````
useradd [options] [username] 
````

Here, [options] refers to the various options available for modifying user account information, and [username] is the name of the user whose account information you want to modify.

[options]<br> 
`-c`: This option is used to add or change the comment for the user account. For example, to add a comment to the user "jdoe", you would use the following command:

````
usermod -c "John Doe" jdoe 
````
`-d`: This option is used to change the home directory for the user account. For example, to change the home directory for the user "jdoe" to /home/jdoe2, you would use the following command:

````
usermod -d /home/jdoe2 jdoe 
````

`-s`: This option is used to change the default shell for the user account. For example, to change the default shell for the user "jdoe" to /bin/bash, you would use the following command:

````
usermod -s /bin/bash jdoe 
````

`-l`: This option is used to change the username for the user account. For example, to change the username for the user "jdoe" to "jdoe2", you would use the following command:

````
usermod -l jdoe2 jdoe 
````
</details>

<details>
<summary>How to switch from one user to another </summary><br>

`su - [username]`: This command allows users to switch between different user accounts in the system. This can be useful if multiple users are sharing a computer or if an administrator needs to access a user's account for troubleshooting purposes.

````
su - janedoe
````
</details>

<details>
<summary>How to access users home directory</summary><br>

`su username` : This command allows users to switch between different user home directories in the system. This can be useful if multiple users are sharing a computer or if an administrator needs to access a user's account for troubleshooting purposes.

````
su - janedoe
````
</details>

<details>
<summary>How to set users password</summary><br>

`passwd [username]` : This command allows admistrators to set a password for user accounts in the system. This can be useful if multiple users are sharing a computer to prevent  access to other user's account.

````
passwd [username] 
````
</details>

<details>
<summary>How to check users with password asigned to thier account </summary><br>

`cat /etc/shadow ` : This command allows admistrators to check user accounts that has been assigned a password in the system. 

````
passwd [username] 
````
* Note : Only users with adminstrative privilages (sudo) will be able to add users to a group in the system 

</details>

<details>
<summary>How to add user to a group<summary><br>

`usermod -a -G [groupname] [username]` : This command allows admistrators to set a password for user accounts in the system. This can be useful if multiple users are sharing a computer to prevent  access to other user's account.
````
usermod -a -G deveops jdoe 
````
* Note : Only users with adminstrative privilages (sudo) will be able to add users to a group in the system 

</details>
<br>


# Groups

## create group 
## add group 
## dell group 
## modify group 



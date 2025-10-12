1)what is user management? why it is used?<br>

2)if you've access to linux server, can you decrypt passwords of users on linux machine? (or) same question in another way i.e. so as an administrator, you shared username and password to a developer, after 1 month developer forgot the password. so can you restore the old password of the developer?<br>
A) In both cases, Answer is NO.<br>
  Although you've encrypted password here, this is highly encrypted. so as part of this encryption shadow-256(SHA-256), so there is a hasing done and this is one way encryption so decryption is not  possible.so,even though you've access to a linux server, you can go to this file (/etc/shadow), look at the encrypted password, but you cannot decrypt it. if someone forgets the password, there is no way to restore the old password. there are some tools in the internet. which promises to do it. However, they are not at all safe. they can decrypt basic passwords but they are not allowed to use in the organization.

3)what is difference between  useradd and adduser?
A)useradd is useful when you are writing scripts. when we writing shell or python scripts, we need a command that creates a user and goes to the next instruction of shell script.
=> In Interactive way, it doesn't want a tool or command to prompt inputs or to ask inputs from you.
=> useradd is a quick way of creating the users where it doesn't prompt for details. it doesn't ask user fullname or it doesn't even create the home directory.
=> add user created home directory for user name. it also takes a lot of user information.


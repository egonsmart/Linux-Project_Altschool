Linux-Project_Altschool
Linux assigment 
Create a User
I created a user named "pastor" using the useradd command: sudo useradd  pastor
i set a password for the user "pastor" using the passwd command: sudo passwd pastor 
Set Expiry Date for the User
the expiry date of 2 weeks for the user "pastor" was created using the command: sudo -e $(2023-09-01) pastor 
To check the password history and account aging information: chage -l pastor
Prompt User to Change Password on Login
I Used the chage command to prompt user to change passwd on login sudo chage -d 0 pastor 
To check if the user "pastor" is prompted to change their password on login: su pastor 
Attach User to a Group
I attached the user "pastor" to a group called "altschool" using the usermod command: sudo usermod -aG altschool pastor
To verify the user's group membership: command: groups pastor 
Allow Group to Run 'cat' Command on /etc/
I edited the sudoers file to allow the "altschool" group to run the cat command on /etc/: sudo visudo to Add the following line on the SSH: %altschool ALL=(ALL:ALL) /bin/cat /etc/
Create Another User without a Home Directory
I created a user named "church" without a home directory using command: useradd --no-create-home church 

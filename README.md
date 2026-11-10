# Cyber-Projects
Lab File Permission Overview.    
    Step 1: Creating Groups and Users, I started by creating three distinct user groups in my terminal using the groupadd command: employee, payroll, and admin.   I then added my own primary user account to the system as a custom group (jgait001).   Next, I created three users—sophia, olivia, and emma—using useradd, configured their home directories, and set their passwords.   I assigned sophia to the employee group, olivia to the payroll group, and emma to the admin group. I also added all three users to my jgait001 group using usermod -aG to verify their group memberships.   Step 2: Creating and Securing the Project DirectoryI created a shared directory at /home/cyse_project using sudo mkdir.   I changed the ownership of this directory to my user account (jgait001) using sudo chown.   To secure the folder, I set the permissions to 770 using sudo chmod, meaning that the owner and members of the group have full read, write, and execute permissions, while others have no access.   Step 3: Task A (Working with Standard Group Permissions)I switched to the user sophia (sudo su sophia) and created a file named Sophia_homework inside her home directory containing my name, "Justin Gaither".   I copied this homework file into the shared directory /home/cyse_project/.   When I checked the permissions and ownership, the file was owned by sophia and the employee group. Because the directory inheritance was standard, other users in different groups (like emma from admin) could still read the file based on its default permissions (-rw-r--r--).   Step 4: Task B (Testing the SGID Bit)Back as the root/student user, I enabled the SetGroupID (SGID) bit on the shared directory by running sudo chmod g+s /home/cyse_project.   I switched back to sophia and copied the file again as Sophia_homework2 into the shared folder.   With the SGID bit enabled, any new files created in this directory automatically inherit the group ownership of the parent directory rather than the creator's primary group, ensuring collaborative consistency.   Step 5: Task C (Removing the SGID Bit)Finally, I removed the SGID bit from the shared directory by running sudo chmod g-s /home/cyse_project.   I logged in as sophia one last time to copy Sophia_homework3 into the shared directory.   This reverted the folder behavior back to default, where newly created files take on the user's default primary group instead of forcing inheritance from the shared parent folder. 
    
Help Desk Ticket 1 overview.
A manager named Tom Wilson submitted a help desk ticket requesting an access update for his employee, Kavita Patel, who was transferring from the Engineering department to IT Infrastructure. To complete the request, I removed Kavita's access to Engineering and granted her the appropriate permissions for IT Infrastructure. After updating her access, she was able to access the files and resources associated with her new department.
Key Skills Demonstrated
- User account and access management
- Department permission changes
- Access control
- Understanding employee transfers
- Following help desk ticket requests
- Updating user permissions
  
Help Desk Ticket 2 overview.
Brian Scott, an employee in the Operations department, reported that his computer was running slowly. I remotely connected to his device to investigate the performance issue and identify possible causes. During troubleshooting, I identified a potential virus issue and updated the system. I also discovered that the computer was running low on available disk space, so I performed a disk cleanup to remove unnecessary files and free up storage. Next, I ran a virus and threat protection scan to check for potential security threats.
After completing these troubleshooting steps, Brian's computer was working properly again.
Key Skills Demonstrated
- Remote desktop troubleshooting
- Computer performance troubleshooting
- System updates
- Disk cleanup and storage management
- Virus and threat protection scanning
- Basic malware troubleshooting
- Problem identification and resolution

  Help Desk Ticket 3 overview.
  Issue: David Lee from the Customer Support department reported that his headset audio was repeatedly cutting in and out during interviews and meetings. The headset worked properly when connected to his phone via Bluetooth but experienced issues on his work computer. Troubleshooting and Resolution: I remotely connected to David’s computer and opened Device Manager to identify his headset. I searched for the headset model and found an available driver update. I downloaded and installed the updated driver, then restarted the computer to apply the changes. Outcome: The headset connectivity issue was resolved, allowing David to use his headset properly during meetings and interviews.
Technical Skills Demonstrated
- Remote desktop troubleshooting
- Windows Device Manager
- Hardware and driver troubleshooting
- Driver installation and updates
- Help desk ticket resolution
- Technical problem-solving

Help Desk Ticket 4 overview
Issue: Beth Collins from the Sales department reported that she was unable to access her department's shared network folder.
Troubleshooting and Resolution: I accessed the IT documentation to locate the correct Sales department shared folder on the file server. I then remotely connected to Beth's workstation, opened Windows File Explorer, and mapped the shared network folder to her computer. Outcome: Successfully restored Beth's access to the Sales department's shared files, resolving the issue and completing the support ticket.
Technical Skills Demonstrated
- Remote desktop support
- Network drive mapping
- Windows File Explorer
- File server navigation
- IT documentation
- Shared folder troubleshooting
- Help desk ticket resolution




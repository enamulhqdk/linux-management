Task 1: Create Users
Tupu:

Command:
```
bash
Copy
Edit
sudo adduser tupu
```
Description: Created a user tupu with a home directory and a password.
```
Lupu:

Command:
bash
Copy
Edit
sudo useradd -m -d /home/lupu -s /bin/bash -g lupu lupu
```
Description: Created a user lupu with a custom home directory and added it to the group lupu.
```
Hupu:

Command:
bash
Copy
Edit
sudo useradd --system --shell /bin/false hupu
```
Description: Created a system user hupu with a disabled login shell.
Task 2: Add Users to the Sudoers Group
```
Commands:
bash
Copy
Edit
sudo usermod -aG sudo tupu
sudo usermod -aG sudo lupu
```
Description: Added tupu and lupu to the sudo group to give them administrative privileges.
Task 3: Create Directory /opt/projekti
```
Commands:
bash
Copy
Edit
sudo mkdir -p /opt/projekti
sudo chgrp projekti /opt/projekti
sudo chmod 2770 /opt/projekti
```
Description: Created the /opt/projekti directory with restricted access for the group projekti. The setgid bit ensures inherited permissions for newly created files and directories.
Task 4: Verify Permissions
```
Command:
bash
Copy
Edit
ls -ld /opt/projekti
Output:
bash
Copy
Edit
drwxrws--- 2 root projekti ...
```
Description: Confirmed that /opt/projekti has the correct permissions (2770) and group ownership is set to projekti.
Task 5: Explanation
What was done:

Assigned the users tupu and lupu as part of the projekti group to control access.
Ensured only these users could list, read, and modify files within /opt/projekti.
Why it works:

The chmod 2770 command restricts access to the directory to only the owner and group members.
The chgrp projekti ensures all users in the projekti group can access the directory.
Adding setgid bit (chmod 2770) ensures all files and subdirectories created within /opt/projekti inherit the projekti group ownership.
Final Steps:
Save the file as assignment.md.
Take screenshots of:
Commands used for each task.
Verification outputs, e.g., permissions.
Commit and push your Markdown file to your GitHub repository.
Copy the repository URL and submit it.
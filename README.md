# Born2bRoot

Quick setup — if you’ve done this kind of thing before
or	
https://github.com/maysasu/Born2bRoot.git
Get started by creating a new file or uploading an existing file. We recommend every repository include a README, LICENSE, and .gitignore.

…or create a new repository on the command line
echo "# Born2bRoot" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/maysasu/Born2bRoot.git
git push -u origin main
…or push an existing repository from the command line
git remote add origin https://github.com/maysasu/Born2bRoot.git
git branch -M main
git push -u origin main
…or import code from another repository
You can initialize this repository with code from a Subversion, Mercurial, or TFS project.

--

AppArmor is a security module for Linux that provides mandatory access control (MAC) capabilities. It was originally developed by Novell (now owned by Micro Focus) and is now a part of the Linux kernel. AppArmor allows administrators to restrict the permissions of individual applications, limiting their access to system resources such as files, network connections, and other processes.

AppArmor works by defining security profiles for each application that specify the permissions and restrictions that should be enforced. These profiles are typically stored in files in the /etc/apparmor.d/ directory. Each profile consists of a set of rules that define which system resources the application can access and how it can access them. For example, a profile might allow an application to read a particular file, but not write to it.

When an application starts up, the AppArmor module checks its security profile to determine what permissions it should have. If the application attempts to access a resource that is not allowed by its profile, the AppArmor module blocks the access and generates an audit log entry. This helps to prevent security breaches by limiting the damage that can be done by a compromised application.

AppArmor is often used in combination with other security modules such as SELinux to provide additional layers of protection. Together, these modules can help to ensure the security and integrity of a Linux system.


--

Preventing root user from connecting via SSH can be done by modifying the SSH configuration file on the server. Here are the steps:

Log in to the server as a user with sudo privileges.

Open the SSH configuration file for editing. On Debian-based systems, the file is located at /etc/ssh/sshd_config.

Find the line that starts with PermitRootLogin and change its value to no. If the line is commented out, uncomment it first and then change the value. The updated line should look like this:

perl
Copy code
PermitRootLogin no
Save the changes to the SSH configuration file and exit the editor.

Restart the SSH service to apply the changes. On Ubuntu or Debian-based systems, the command is:

Copy code
sudo systemctl restart ssh
After completing these steps, the root user will no longer be able to connect to the server using SSH. It is recommended to create a separate user account with sudo privileges for remote administration, and use that account to log in via SSH. This can help improve security by limiting the attack surface of the server.

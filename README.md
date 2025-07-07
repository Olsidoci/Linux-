# 🐧 Linux File Permissions & Authorization

## 📄 Project Description

This project simulates a real-world scenario in which I serve as a security professional managing file permissions for a research team in a large organization. My responsibility is to ensure that file access permissions across a Linux-based system align with the organization’s security policies. Through this project, I demonstrate my ability to investigate existing file permissions, interpret permission strings, identify misconfigurations, and apply appropriate changes using Linux command-line tools.

The goal is to enhance system security by restricting unauthorized access and ensuring sensitive data is protected based on user roles.

---

 🧪 Tasks & Linux Commands

🔍 Check File and Directory Permissions

```bash
ls -la projects/

📌 Describe the Permissions String

Example: -rw-rw-r--
- → regular file
rw- → user has read and write access
rw- → group has read and write access
r-- → others have only read access

This permission string helps determine which entities (user, group, others) have access and what type of access they have.

✏️ Change File Permissions for Security Compliance

chmod o-w project_k.txt
ls -la project_k.txt

🕵️‍♂️ Secure Hidden File .project_x.txt

chmod u-w .project_x.txt
chmod g-w .project_x.txt
chmod g+r .project_x.txt
ls -la .project_x.txt

🔐 Restrict Access to the drafts/ Directory

chmod g-x projects/drafts/
ls -la projects/

⚙️ Commands Used

Command	Description
ls -la	Lists all files, including hidden, with permissions
chmod	Modifies file and directory permissions
chmod o-w	Removes write access for others
chmod u-w, g-w, g+r	Adjusts user/group read/write access

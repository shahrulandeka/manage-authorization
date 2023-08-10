<h1>[Mini] Manage Authorization</h1>

<h2>Description</h2>
In this lab example, I run through how to configure authorization of Users, Groups and Others, using Linux commands.<br/>
Setting appropriate access permissions is critical to protecting sensitive information and maintaining the overall security of a system.
<br/>
At the end of this lab, I would have practical experience in: <br/>
- Examining file and directory permissions, <br/>
- Change permissions on files, and <br/>
- Change permissions on directories.

<h2>Languages and Utilities Used</h2>

- <b>Bash Shell</b> 
- <b>Oracle VM Virtual Box</b>

<h2>Environments Used </h2>

- <b>Windows 10 Pro</b> (22H2)

<h2>Program walk-through:</h2>

<p align="center">
Launch the utility: <br/>
  For this example, we are researcher2 user, and are part of the research_team group.
<img src="https://i.imgur.com/clP882o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
1. For this example, i must explore the permissions of the "projects" directory and the files it contains:
 <br/>
  First, I navigate to the projects directory. <br/>
  Then, I type in "ls -l" to list the contents and permissions of the "projects" directory.<br/>
  We should be able to see that the research_team is the group that owns the files in the "projects" directory.
<img src="https://i.imgur.com/M6iVGBF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
2. Type in "ls -a" to check whether any hidden files exist in the "projects" directory: <br/>
  The project file ".project_x.txt" should be the hidden file, as indicated by the "." infront of the file name.
<img src="https://i.imgur.com/z7POxDm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
3. For this example, I must determine whether any files have incorrect permissions and then change the permissions as needed:  <br/>
  After typing "ls -la", I can see that project_k.txt has read and write permissions for the owner type of others. <br/>
  Note* "ls -la" is to list the contents, permissions AND hidden files of the current working directory.
<img src="https://i.imgur.com/SepqY8S.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
4. I intend to change the permissions of the file identified in the previous step, so that the owner type of other doesn't have write permissions:  <br/>
  Type in "chmod o-w project_k.txt". This removes the write permissions of the owner type of others.
<img src="https://i.imgur.com/0x4vsS3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
5. Suppose that project_m.txt is a restricted file, whereby only the user should have the read, write and execute permissions exclusively:  <br/>
  On the highlighted text, we can see that the group has read only permissions on project_m.txt.
<img src="https://i.imgur.com/rByv8d2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
6. I use the chmod command to remove the read permissions of the group:  <br/>
  I double check with "ls -la" to verify the change of permissions for the specified file (project_m.txt).
<img src="https://i.imgur.com/PFHEKf1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
7. Suppose that project_x.txt is an archived file, and should not be written to by anyone(except read permissions by user and group):  <br/>
<img src="https://i.imgur.com/FtYdNcO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
8. Change the permissions of the user and group with the = command:  <br/>
<img src="https://i.imgur.com/OiBEQtX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

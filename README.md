
![image](https://github.com/jameswsm/sharing-resources/assets/170709350/ad40a500-1383-4130-88e8-f5bbd20feaf2)
</p>

<h1>Sharing resources over the network</h1>
Tutorial for sharing resources over a network<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Users and Computers

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Microsoft Azure Active Subscription (Creation of Reasearch Group, VMs, Virtual Networks, Subnets)
- Active Directory running in Azure on a virtual machine (DC1)
- Client machine running in Azure on a VM (Client1) and joined to the domain

<h2>Steps: 1 - 8</h2>

![image](https://github.com/jameswsm/sharing-resources/assets/170709350/ccda024f-0d67-4522-ab7d-dc5651e503be)
<p>
Step 1: Log into Domain Controller (ex: DC1) as domain admin account (ex: james_admin) -> Minimize
</p>
<br />

![image](https://github.com/jameswsm/sharing-resources/assets/170709350/8a104b12-8520-42cb-83b4-a849a9462883)
<p>
Step 2: Log into Client1 as a normal user (ex: bes.jom)
</p>
<br />

![image](https://github.com/jameswsm/sharing-resources/assets/170709350/ef6162c1-f237-43f6-9927-dc76ebed2ea4)
<p>
Step 3: On DC1 -> Navigate to C:\  drive -> create 4 folders: "read-access", "write-access", "no-access", "accounting"
</p>
<br />

![image](https://github.com/jameswsm/sharing-resources/assets/170709350/141fe68e-e8de-41cd-8f9b-8e98d7384ffa)
<p>
Step 4: In the "read-access" folder, create a text file(ex: read only!) with text inside that says "hello" 
</p>
<br />

![image](https://github.com/jameswsm/sharing-resources/assets/170709350/7509af26-a0b5-424c-b686-4580a9683f1e)
<p>
Step 5: Set permissions for Folder: "read-access", Group: "Domain Users", Permission: "Read"
</p>
<p>
read-access -> Properties -> Sharing -> Share... -> enter "domain users" -> Add -> Share -> Done
</p>

![image](https://github.com/jameswsm/sharing-resources/assets/170709350/01538997-7ed5-43db-aa05-4f086ab37970)
<p>
Step 6: Set permissions for Folder: "write-access", Group: "Domain Users", Permissions: "Read/Write"
</p>
<p>
write-access -> Properties -> Sharing -> Share... -> enter "domain users" -> Add -> Permission Level: Read/Write -> Share -> Done
</p>

![image](https://github.com/jameswsm/sharing-resources/assets/170709350/e74d64b1-0a0b-4bd6-90af-0855882ebda8)
<p>
Step 7: Set permissions for Folder: "no-access", Group: "Domain Admins", Permissions: "Read/Write"
</p>
<p>
no-access -> Properties -> Sharing -> Share... -> enter "domain admins" -> Add -> Permission Level: Read/Write -> Share -> Done
</p>

![image](https://github.com/jameswsm/sharing-resources/assets/170709350/9fb692b9-08e5-44f6-9753-5eaf32450619)
<p>
Step 8: On Client1(ex: bes.jom), navigate to the shared folder \\dc1
</p>
<br />


![image](https://github.com/jameswsm/sharing-resources/assets/170709350/fd5489e4-9801-45f2-a431-d4bd45f8ebf2)
![image](https://github.com/jameswsm/sharing-resources/assets/170709350/ac426f83-c2df-4fc8-b3c5-52d669ee982f)
![image](https://github.com/jameswsm/sharing-resources/assets/170709350/eb2e2a34-2b65-4b79-aa69-d72b58fd6ecc)
<p>
Attempting to access the no-access folder should show an error message because bes.jom is NOT an admin.
</p>
<p>
Attempting to create anything in the read-access folder should show a message of denied access. However you are allowed to open the file and read it(ex: hello).
</p>
<p>
Attempting to create anything in the write-acesss folder(ex:new file!) should work properly
</p>
<br />
















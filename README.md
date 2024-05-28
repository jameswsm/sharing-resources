
![image](https://github.com/jameswsm/sharing-resources/assets/170709350/ad40a500-1383-4130-88e8-f5bbd20feaf2)
</p>

<h1>Sharing Resources Over the Network</h1>
Tutorial for sharing resources over a network<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Microsoft Azure Active Subscription (Creation of Reasearch Group, VMs, Virtual Networks, Subnets)
- Active Directory running in Azure on a virtual machine (DC1)
- Client machine running in Azure on a VM (Client1) and joined to the domain

<h2>Steps: 1 - /////</h2>

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


<p>
Step 4: Set permissions for "Domain Users" group
</p>
<br />

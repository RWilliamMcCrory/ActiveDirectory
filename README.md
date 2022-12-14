<h1>How to Setup a Basic Home Lab Running Active Directory (Oracle VirtualBox) | Add Users w/PowerShell
</h1>


<h2>Description</h2>
In this project, I setup Windows Server, create and configure a DC, then I automate a process to create 1000 users utilizing a powershell script.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Active Directory</b>
- <b>Oracle VM VirtualBox Manager</b>

<h2>Environments Used </h2>

- <b>Windows 10</b>
- <b>Windows Server 2019</b>

<h2>Project walk-through:</h2>


<p align="center">
Installing Windows Server on my VM


 <br/>

![image](https://user-images.githubusercontent.com/120264673/207482496-fdbe1fe5-d618-478e-b32c-41893560864f.png)

<p align="center">
Setting up IP addresses on the DC using the following diagram:
<br/>


<p align="center">
  <img src="https://user-images.githubusercontent.com/120264673/207483014-54322000-5775-42f2-93d8-0ecbfeb5058b.png" />
</p>



<br />
<br />
<p align="center">
Implementation:

<br/>
</p>

<br/>
<p align="center">
  <img src="https://user-images.githubusercontent.com/120264673/207483040-b591a78d-0962-4317-930b-82c50f7974d7.png" />
</p>

<p align="center">
Installing Active Directory Domain Services

<br/>
<p align="center">
  <img src="https://user-images.githubusercontent.com/120264673/207483122-37c92005-8999-4d07-b151-2409cbb09bac.png" />
</p>




<p align="center">
Deployment:  Promoting computer to a Domain


<br/>
<p align="center">
  <img src="https://user-images.githubusercontent.com/120264673/207483237-bb70aaa5-6ab5-43bd-b758-65bd7af965ca.png" />
</p>






<p align= "center">
Creating an Organizational Unit for Admin accounts

<p align="center">
  <img src="https://user-images.githubusercontent.com/120264673/207483319-0ace0504-9b80-469f-850a-1eb29bbda2ee.png" />
</p>


  <p align="center">
  <img src="https://user-images.githubusercontent.com/120264673/207483347-32d43708-5097-4b27-bc90-70746890064e.png" />
</p>


  


<p align= "center">
Creating an Admin account:

 <p align="center">
  <img src="https://user-images.githubusercontent.com/120264673/207484304-0f49633a-a14b-4f24-bc60-49f4eb0b7e54.png" />
</p>



<p align= "center">
Provisioining the account with the needed admin security group

 <p align="center">
  <img src="https://user-images.githubusercontent.com/120264673/207484694-162dd37d-f689-4750-a10e-5a23c8b33ad3.png" />
</p>





<p align= "center">
Signing in with the newly created A-Account

 <p align="center">
  <img src="https://user-images.githubusercontent.com/120264673/207484879-e680aa3a-afbd-44ba-852e-73a51629c62a.png" />
</p>



<p align= "center">
Installing (RAS/NAT) on the DC to allow my Windows 10 client to access the internet through the DC

 <p align="center">
  <img src="https://user-images.githubusercontent.com/120264673/207485047-29951abe-eff6-4513-9e20-71ca70bf8462.png" />
</p>



<p align= "center">
Installing NAT


 <p align="center">
  <img src="https://user-images.githubusercontent.com/120264673/207485373-fc370f46-0072-44c9-8922-1c078f81aceb.png" />
</p>


<p align= "center">
Installing and setting DHCP scope


<p align="center">
  <img src="https://user-images.githubusercontent.com/120264673/207485459-44d78a37-4c64-48aa-9ca8-04ad2514acaa.png" />
</p>



<p align= "center">
Here's the file I'll be using to programmatically create 1000 users through Powershell:

<p align="center">
  <img src="https://user-images.githubusercontent.com/120264673/207485633-f4b1ee29-065d-44e3-92c9-a02c17824caa.png" />
</p>


<p align= "center">
Running the script after pointing Powershell to the needed file 

<p align= "center">
<img src="https://user-images.githubusercontent.com/120264673/207485808-e244c8b9-9d05-489a-aa5c-1276cc876b97.png"
</p>

<p align= "center">
Here's the users showing in AD after running the script 

<p align= "center">
<img src="https://user-images.githubusercontent.com/120264673/207486031-85a102d3-dc70-4252-8720-d42d93179d50.png"
</p>

<p align= "center">
Installing Windows 10 on a secondary VM to test access with one of the newly created accounts 

<p align= "center">
<img src="https://user-images.githubusercontent.com/120264673/207486240-2b11db84-4211-4e33-a143-8e83052ade69.png"
</p>

<p align= "center">
Testing Internet on the Client VM

<p align= "center">
<img src="https://user-images.githubusercontent.com/120264673/207487617-4242f599-b0e3-407d-b93b-f7b654b204c2.png"
</p>

<p align= "center">
Renaming the VM and joining the domain
<p align= "center">
<img src="https://user-images.githubusercontent.com/120264673/207488711-5019ed4e-2358-409d-be9b-f8927a1082a5.png"
</p>

<p align= "center">
Client VM showing in ADUC and the lease for the Client VM

<p align= "center">
<img src="https://user-images.githubusercontent.com/120264673/207489195-febcfff3-1017-452b-9c2a-4b7591bcd51d.png"
</p>


<p align= "center">
Thanks for viewing!


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Installation Steps</h2>

<p>
First, we need to install and enable IIS on Windows and <b>make sure that CGI and Common HTTP Features are enabled.</b><br>
In order to do this, we need to access "Windows Features" by following the next route:<br> <ins>Control Panel -> Programs -> Programs and Features - > Turn Windows features on or off. </ins>
</p>
<p>
  
![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/7bba0e68-aa3d-498a-b252-bee1d22487ae)

</p>
<br />
<p>
Inside "Windows Features", make sure to check "Internet Information Services".<br>
Then enable CGI by going the following route: <ins>Internet Information Services -> World Wide Web -> Application Development Features.</ins><br>
Finally, inside the "World Wide Web Services" folder, enter the "Common HTTP Features", make sure all the options are enabled, and click OK to begin the installation.
</p>
<p>
  
![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/02fd3e67-9a14-4836-af2d-ec05fe9fdd87)
![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/c1622e18-a4ed-49a8-84ec-a1f89fdfd58e)
![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/b48d5bc2-48fc-4046-9a59-691214cab01a)

</p>
<br />

<p>
To confirm that the installation of IIS was correct, go to a web browser and enter the localhost IP: 127.0.0.1 If your window looks like the example below, you are good to go.
</p>
<p>
  
![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/94606d1b-5fc5-4384-92b4-d1ab2067d715)

</p>
<br />
<p>
Next, we'll need to download and install some software in order to help OSticket correct installation. Search for the files on the WEB and install the current version of <b>PHP Manager for IIS</b>, <b>Rewrite Module</b> and <b>VC_redist</b>.
</p>
<p>
 Next, we'll need to install <b>PHP</b> current version.<br>
 Create the next directory -> C:\PHP
</p>
<p>

  ![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/4339bd41-3737-48d6-b5d2-c236a2f7e380)
  
</p>
<p>
  Download the .ZIP of the most stable version of <b>PHP</b> and extract the contents inside the recently created PHP directory.
</p>
<p>
  Then download and install the current version of <b>MySQL</b>. Follow the next steps in order to make a correct installation:<br>
  <ins>Typical Setup -> Launch Configuration Wizard (after install) -> Standard Configuration -> Install As Windows Service -> Choose and note down your new root password.</ins>
</p>
<br/>

<p>
  Now we'll make some configurations inside <b>Internet Informacion Services (IIS) Manager</b> to prepare for the installation of the OSticket software. 
</p>
<p>
  
  ![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/645a357c-d14b-4417-a6d8-3c382885497c) 
</p>
<p>
  Inside <b>IIS</b> we'll register the <b>PHP</b> directory we made before. First, go into the PHP Manager option.
</p>
<p>

  ![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/99b0ec93-d0cc-4c8a-809c-9b7f87cad8ec)
</p>
<p>
  Inside, click on the "Register new PHP Version option" and look for the "php-cgi.exe" inside our PHP directory to select as the file. Click ok and then restart the manager server.
</p>
<p>

  ![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/2e6f8eed-b811-4561-ab8c-ecefdb197318)
  ![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/5ef256ab-4d88-440c-9da6-fa98af2234ad)
  ![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/fdbcbb0e-dacd-4d39-ade7-c19063c6f3ee)
</p>

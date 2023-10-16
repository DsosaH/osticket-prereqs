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
First, we need to install and enable IIS on Windows and <b>make sure that CGI and Common HTTP Features are enabled.</b>
In order to do this, we need to access "Windows Features" by following the next route: <ins>Control Panel -> Programs -> Programs and Features - > Turn Windows features on or off. </ins>
</p>
<p>
  
![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/7bba0e68-aa3d-498a-b252-bee1d22487ae)

</p>
<br />
<p>
Inside "Windows Features", make sure to check "Internet Information Services".
Then enable CGI by going the following route: <ins>Internet Information Services -> World Wide Web -> Application Development Features.</ins>
Finally, inside the "World Wide Web Services" folder, enter the "Common HTTP Features", make sure all the options are enabled, and click OK to begin the installation.
</p>
<p>
  
![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/02fd3e67-9a14-4836-af2d-ec05fe9fdd87)
![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/c1622e18-a4ed-49a8-84ec-a1f89fdfd58e)
![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/b48d5bc2-48fc-4046-9a59-691214cab01a)

</p>
<br />

<p>
To confirm that the installation of IIS was correct, go to a web browser and enter the localhost IP: 127.0.0.1. If your window looks like the example below, you are good to go.
</p>
<p>
  
![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/94606d1b-5fc5-4384-92b4-d1ab2067d715)

</p>
<br />

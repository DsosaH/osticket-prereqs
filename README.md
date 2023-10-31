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
<br/>
<p>
  Download the most stable version of OSticket. Extract the "Upload" folder into "c:\inetpub\wwwroot" and rename the folder to "osTicket". Restart the manager server once again.
</p>
<p>

  ![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/d2b29a2b-01d9-414a-a666-8e12260adc30)

</p>
<br/>
<p>
  Inside ISS Manager follow <ins>sites -> Default -> osTicket</ins>. There click  “Browse *:80” to open an osTicket installer in the browser, but don't touch it yet, first we need to enable some extensions.
</p>
<p>

  ![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/bbc31f4d-6f81-4a0e-b652-0f1078ad54d7)
  ![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/9d879499-ab3d-43ba-b0cc-b809e3015af5)
  ![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/612f6c05-5203-456a-a408-b261bdb2857a)

</p>
<p>
  Enter PHP Manager inside the osTicket folder and click “Enable or disable an extension”. <br>Enable:
  <ul>
    <li>php_imap.dll</li>
    <li>php_intl.dll</li>
    <li>php_opcache.dll</li>
  </ul>
  
</p>
<p>

  ![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/8f875543-52f3-442e-a9e4-94d1e8e0fdcf)
  
</p>
<p>
  After you are done with the extensions, refresh your browser and the page should now look like this.
</p>
<p>

  ![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/31f55a2e-eb79-4eb4-9088-1e8c4ad12e3a)

</p>
<p>
  Rename "ost-sampleconfig.php" to "ost-config.php" in "C:\inetpub\wwwroot\osTicket\include".<br>
  Then inside the "Properties" of "ost-config.php", enter the Security tab and click on Advanced. There, disable inheritance and remove all inherited permissions for this object.
</p>
<p>

  ![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/22da3c42-6779-4b6e-95bc-f178ff91503c)
![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/4d5824a1-70a8-40ca-957e-e603ab494745)

</p>
<p>
  Now, we'll give this file new permissions.<br>
  Click "Add" -> "Select a Principal", type "Everyone" and check for names. Click ok.<br>
  Check "Full Control" then Ok. Apply and close.
</p>
<p>
  
  ![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/3830c6c1-0572-4c43-9ab1-9cf6ec1531e9)

</p>
<br/>
<p>
  Now we can go to the browser and click "Continue" to continue the setting up.<br>
  Choose a name for your desk and a default email. Fill the fields with the desired info.<br>
  Before we can install, we need to set up our Database. For this, we'll install "HeidiSQL".
</p><br/>
<p>
  Download the most stable version of "HeidiSQL" and install it then launch the software.<br>
  Inside "HeidiSQL" start a new session by clicking the new button, the insert the previously created password during the installation of "MySQL" and click open.<br>
  Right click "Unnamed", click "Create New" and select "Database". Choose a name for your data base create it.
</p>
<p>

  ![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/e1afc46f-f5b3-45a4-afe2-22c78b744978)

</p>
<p>
  Now that the database is up, go to the browser and fill the database setting fields with the fitting info. Finally click install and wait.<br>
  If everything went right, you should see this screen.
</p>
<p>

  ![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/37aba374-dc36-4e21-92c9-9522e55de2ec)

</p>
<p>
  Before finishing up, let's do some clean up and check that everything works just fine.<br>
  First, inside "C:\inetpub\wwwroot\osTicket" delete "setup". Then, go to  "C:\inetpub\wwwroot\osTicket\include" and set "ost-config.php" to "Read Only" in it's properties.
</p>
<p>

  ![image](https://github.com/DsosaH/osticket-prereqs/assets/148100125/36a761bc-ac25-4132-a223-ddb7ef5653cc)

</p>

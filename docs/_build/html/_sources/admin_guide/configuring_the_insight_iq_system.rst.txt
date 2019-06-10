Configuring the InsightIQ system
================================

Configure InsightIQ. 

InsightIQ configuration tasks include installation of SSL certificates, modifying port access, configuring LDAP authentication, and configuring email settings.

Specify the InsightIQ port 
--------------------------
Specify the port through which InsightIQ connects.

1. Open an SSH connection to the InsightIQ virtual machine and log in. 

2. In a text editor, open the ``/etc/isilon/insightiq.ini`` file, and specify the values for the following options.
  
   +-------------------+----------------------------------------+
   | Option            | Description                            |
   +===================+========================================+
   | port              | The port to connect to InsightIQ       |
   | redirect_to_port  | The port to connect to InsightIQ       |
   +-------------------+----------------------------------------+

   **Note** The value must be the same for both settings. You must have root permissions to modify the ``/etc/isilon/`` insightiq.ini file. If you are logged in the InsightIQ administrator account, you can gain root access by beginning a command with sudo. 

3. Save and close the ``/etc/isilon/insightiq.ini`` file. 

4. Restart InsightIQ by running the command iiq_restart. 

Specify an SSL certificate
--------------------------
Specify a custom SSL certificate. Although InsightIQ includes a default SSL certificate, you can specify a custom SSL certificate.

1. Open an SSH connection to the InsightIQ virtual machine, and log in. 

2. On the InsightIQ virtual machine, save a copy of the SSL certificate files that you want to specify. The certificate files must be of the .crt and.key file types. 

3. Open the /etc/isilon/uwsgi.ini file in a text editor and update the value of the https setting with the path of the SSL certificate files. For example, the following text specifies the SSL certificate files that are in the ``/etc/ssl/certs/`` directory:

   ``https = [::]:443,/etc/ssl/certs/server.crt,/etc/ssl/certs/ server.key,HIGH``

4. Restart InsightIQ by running the following command:

   ``iiq_restart``

Connect to InsightIQ over IPv6 
------------------------------
InsightIQ supports IPv6. You can connect to InsightIQ, monitor clusters, and connect to NFS data stores over IPv6. 

You can connect to an NFS data store over IPv6 only if IPv6 addresses are configured for both InsightIQ and the NFS server. You can monitor an Isilon cluster over IPv6 only if IPv6 addresses are configured for both the monitored cluster and InsightIQ, and the cluster is running OneFS 7.2.1 or later. 

If you connect to InsightIQ over IPv6 using an Apple Safari web browser, specify either a DNS hostname or an SSL URL. If you connect to InsightIQ over IPv6 using the Google Chrome web browser, specify a DNS hostname. You cannot connect to InsightIQ using an IP address while using Google Chrome, even if you specify an SSL connection type.

Table 1 Browser support with IPv6

+----------------+-----------------------------------+
| Web browser    | Supported connection type         |
+================+===================================+
| Apple Safari   | DNS hostname or an SSL connection |
| Google Chrome  | DNS hostname                      |
+----------------+-----------------------------------+

Configure outbound email support
--------------------------------
To send reports and InsightIQ status alerts by email, configure InsightIQ to use an email server. 

1. In the InsightIQ web application, click the Settings tab and then **Email** on the **Settings** ribbon. The **Configure Email Settings (SMTP)** view appears.

2. In the SMTP server field, type the hostname or IP address of an SMTP server that handles email for the organization.

3. In the SMTP port field, type the number of the port that is used to connect to the SMTP server that you specified.

4. If the SMTP server that you specified requires a username and password for authentication, in the **Username** and **Password** fields, specify a valid username and password. 

5. If the SMTP server you specified accepts email only from valid email addresses, type a valid email address in the **From Email** field. The address that you type appears in the **From** field of email messages.

6. If either the Transport Layer Security (TLS) or Secure Sockets Layer (SSL) protocol is required to connect to the SMTP server that you specified, select the **TLS Connection** checkbox. 

7. Click **Submit**.

Testing the email configuration
-------------------------------
Validate the InsightIQ email configuration by sending a test email. 

1. In the InsightIQ web application, click the **Settings** tab and then **Email** on the **Settings** ribbon. 

2. In the **Send a test email field**, type the name of an email address.

3. Click **Send**. 

4. Check the recipient email inbox. If you have configured InsightIQ correctly, a test email arrives.

# Android_app_VAPT
I did an Pentetration testing on a Android application

<h2>Vulnerability Analysis</h2>
<b>Overview:<br />
I did a Vulnerability Analysis and Penetration testing on android app Andro Goat and found some vulnerabilities and mentioned those vulnerabilities and its effects to the app in this report. </b>
<br />
<br/>
<h2>1.	Insecure Backup Storage:</h2>
•	Vulnerable Application – Andro Goat.<br /
•	Vulnerability Description:<br />
Insecure data storage vulnerabilities occur when development teams assume that users or malware will not have access to a mobile device's filesystem and subsequent sensitive information in data-stores on the device and let the backup to be open.<br />
•	Steps to Reproduce:<br />
  -	Step 1: Open Appie and extract the source code of the app.<br />
  -	Step 2: Open AndroidManifest.xml file and found that backup is allowed.<br />
-	Step 3: Now get the backup file through Appie using “adb backup -f test.ab AndroGoat” command.<br />
-	Step 4: Then use Kali to extract the complete application.<br />
•	Impact:<br />
-	Attackers can get the complete information about the application.<br />
-	Attackers can use it to exploit the app. <br />
•	Proof of Concept:<br />

![image](https://github.com/JOELFRANKO/Android_app_VAPT/assets/81144974/abf94528-a894-4744-9296-4c8f9ac35a39)

![image](https://github.com/JOELFRANKO/Android_app_VAPT/assets/81144974/d754f547-dbb1-43c3-aa0d-8e83c3a09f00)<br />

![image](https://github.com/JOELFRANKO/Android_app_VAPT/assets/81144974/cf2ba488-9dad-4d52-a5e9-7a79a1830ea4)<br />

![image](https://github.com/JOELFRANKO/Android_app_VAPT/assets/81144974/9485b196-8ca1-4ee8-b1f1-c3210b525de3)<br />

![image](https://github.com/JOELFRANKO/Android_app_VAPT/assets/81144974/e788481e-c02e-4126-9ea7-005f63b4c509)<br />

<h2>2.	Sensitive Data Hardcoding:</h2>
•	Vulnerable Application – Andro Goat.<br />
•	Vulnerability Description:<br />
Hard coding sensitive information, such as passwords, server IP addresses, and encryption keys can expose the information to attackers. Anyone who has access to the class files can decompile them and discover the sensitive information.<br />
•	Steps to Reproduce:<br />
-	Step 1: Open Appie and get the source code of the application using apktool.<br />
-	Step 2: Analyse the source code using Java Decompiler. <br />
-	Step 3: I got the promocode from the source code.<br />
-	Step 4: use the promocode to check.<br />
•	Impact:<br />
-	Attackers can get access to sensitive information.<br />
-	Attackers can use the information to exploit the app or can be used to gather more information of the app.<br />
•	Proof of Concept:<br />

![image](https://github.com/JOELFRANKO/Android_app_VAPT/assets/81144974/1a1e8fe6-6ede-4088-87bb-dedd56af9c0e)<br />

![image](https://github.com/JOELFRANKO/Android_app_VAPT/assets/81144974/b85b9a5f-575e-47d1-acfa-1d7286197880)<br />

![image](https://github.com/JOELFRANKO/Android_app_VAPT/assets/81144974/207e3929-0f02-4281-b5c5-3aea81799d15)<br />

![image](https://github.com/JOELFRANKO/Android_app_VAPT/assets/81144974/ccb9473d-620c-4de3-b0a7-f4dba291d9d8)<br />

<h2>3.	Denial of Service Attack:</h2><br />
•	Vulnerable Application – Andro Goat.<br />
•	Vulnerability Description:<br />
A denial-of-service (DoS) attack is a cyberattack on devices, information systems, or other network resources that prevents legitimate users from accessing expected services and resources. This is usually accomplished by flooding the targeted host or network with traffic until the target can't respond or crashes.<br />
•	Steps to Reproduce:<br />
-	Step 1: Open Appie and check the attack vector of the app and if the activity is 1 or more then check the activity.<br />
-	Step 2: Then use “run app.activity.start --component owasp.sat.agoat Activity” to do a dos attack.<br />
-	Step 3: DoS attack happened in “run app.activity.start --component owasp.sat.agoat owasp.sat.agoat.Splash Activity” this command.<br />
•	Impact:<br />
-	Attackers can stop the app execution.<br />
-	Attackers can crash the app and cause data, money and time loss.<br />
•	Proof of Concept:<br />

![image](https://github.com/JOELFRANKO/Android_app_VAPT/assets/81144974/b2f8675c-75df-4e38-9478-3919d5d9b36a)<br />

![image](https://github.com/JOELFRANKO/Android_app_VAPT/assets/81144974/763bfe76-5845-4822-9514-d726d09a95b9)<br />

![image](https://github.com/JOELFRANKO/Android_app_VAPT/assets/81144974/8d934278-3f6a-4948-9a6c-7b758aaf5c70)<br />

![image](https://github.com/JOELFRANKO/Android_app_VAPT/assets/81144974/486decd6-effb-45d4-89c1-6160e1c5a446)<br />

<p format:"Bold"><b> -> App crashed in the above image</b></p><br />

![image](https://github.com/JOELFRANKO/Android_app_VAPT/assets/81144974/9032b424-c334-4dda-b281-888007da2c84)<br />

<h2>4.	Insecure Data Storage:</h2><br />
•	Vulnerable Application – Andro Goat.<br />
•	Vulnerability Description:<br />
Insecure data storage vulnerabilities occur when development teams assume that users or malware will not have access to a mobile device's filesystem and subsequent sensitive information in data-stores on the device.<br />
•	Steps to Reproduce:<br />
-	Step 1: Open the application and store an information.<br />
-	Step 2: Open Appie and analyse the Android files for the information.<br />
-	Step 3: Got the information in  Database/aGoat.<br />
•	Impact:<br />
-	Attackers gain access to sensitive information.<br />
-	Attackers can use the information to exploit the application.<br />
•	Proof of Concept:<br />

![image](https://github.com/JOELFRANKO/Android_app_VAPT/assets/81144974/5d8e29d5-eaaa-4706-90c4-c996c471c95b)<br />

![image](https://github.com/JOELFRANKO/Android_app_VAPT/assets/81144974/759e5ee5-ae98-4fbe-8726-b38e2cd30ff9)<br />

![image](https://github.com/JOELFRANKO/Android_app_VAPT/assets/81144974/5888b980-6993-486f-bdda-92e85196beea)<br />

<h2>5.	Cross Site Scripting (XSS):</h2><br />
•	Vulnerable Application – Andro Goat.<br />
•	Vulnerability Description:<br />
Cross-site scripting (XSS) is an attack in which an attacker injects malicious executable scripts into the code of a trusted application or website. Attackers often initiate an XSS attack by sending a malicious link to a user and enticing the user to click it.<br />
•	Steps to Reproduce:<br />
-	Step 1: Open the application and try to run html scripts.<br />
-	Step 2: The html script inserted has been executed.<br />
•	Impact:<br />
-	Attackers gain access to sensitive information.<br />
-	Attackers can gain remote access to the system using RCE.<br />
•	Proof of Concept:<br />

![image](https://github.com/JOELFRANKO/Android_app_VAPT/assets/81144974/a333ac18-a007-478c-a0c6-a0f900636be7)<br />

![image](https://github.com/JOELFRANKO/Android_app_VAPT/assets/81144974/2d08800c-5c6a-4078-90ac-648208e06414)


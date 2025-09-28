# creating-a-backdoor-with-SET
creating a backdoor with SET - Ethical Hacking Techniques course

# AIM:
To Create a backdoor with Social Engineering Toolkit (SET)

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode


### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

### Architecture Diagram

```
+----------------+        +------------------------+        +----------------------+
| Attacker's PC  | -----> | SET (Credential        | -----> | Fake Login Page      |
| (Kali Linux)   |        | Harvester via Apache)  |        | (Hosted by SET)      |
+----------------+        +------------------------+        +----------------------+
       |                                                             |
       |                                                             v
       |   1. Configure SET with phishing site (e.g., Gmail clone)   |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Victim's Browser     |
       | <------------------------------------------------| Clicks Phishing Link|
       |                                                 +----------------------+
       |                                                             |
       |                                                             v
       |     2. Victim Enters Credentials → Sent to SET/Attacker    |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Credentials Captured |
       |                                                 | in Apache log/SET DB |
       |                                                 +----------------------+

```

## EXECUTION STEPS AND ITS OUTPUT:
Social Engineering attacks are the various cons used by the hackers to trick people into providing sensitive data to the attackers.

**Steps to Use SET for Phishing (Credential Harvester Attack Method)**

**1. Open terminal:**
```bash
sudo setoolkit
```
**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method  
```
**3. Enter your IP address as the attacker server.**
**4. Choose:**
```bash
2) Site Cloner
```
**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**

**6. Send the generated link to the victim.**

**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```

## OUTPUT:

<img width="1920" height="1200" alt="Screenshot (160)" src="https://github.com/user-attachments/assets/23856900-db3a-48ae-81ab-134bae688535" />

<img width="1920" height="1200" alt="Screenshot (161)" src="https://github.com/user-attachments/assets/a002db36-6d30-4321-8ee5-bfba071f608b" />

<img width="1920" height="1200" alt="Screenshot (162)" src="https://github.com/user-attachments/assets/0a661137-31f9-4b05-adeb-094d8cc21f5e" />

<img width="1920" height="1200" alt="Screenshot (163)" src="https://github.com/user-attachments/assets/61fcaffc-2947-46fe-9b42-47a8a28da4af" />

<img width="1920" height="1200" alt="Screenshot (164)" src="https://github.com/user-attachments/assets/666e43c5-0e79-4921-91ab-16659ebf2645" />

## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully

# **Protecting User Password Keys at Rest (on the Disk)**

![Intel Logo](https://logodownload.org/wp-content/uploads/2014/04/intel-logo-5-1.png)

## **Project Overview**


protecting user password keys at rest is paramount to ensuring the security and privacy of personal and sensitive information. "At rest" refers to data stored on a device or in a database, as opposed to data  actively being transferred across networks.
Several key factors drive the need for robust protection mechanisms for user password keys:
1.	Data Breaches: With the increasing frequency and sophistication of cyber-attacks, data breaches have become a significant threat. If user password keys are not properly protected, malicious actors can easily exploit them, leading to unauthorized access to accounts and services.
2.	Regulatory Compliance: Various regulations and standards, such as the General Data Protection Regulation (GDPR) and the Payment Card Industry Data Security Standard (PCI DSS), mandate stringent measures for protecting sensitive data, including password keys. Non-compliance can result in severe penalties and reputational damage.
3.	User Trust: Users expect their personal information to be handled with the highest level of security. Failure to protect user password keys can erode trust, leading to a loss of customers and a negative impact on the organization's brand.
To mitigate these risks, several best practices and technologies are employed to protect user password keys at rest:
1.	Encryption: Encrypting password keys using strong encryption algorithms ensures that even if the data is accessed by unauthorized individuals, it remains unreadable without the appropriate decryption key.
2.	Hashing: Password hashing involves converting the original password into a fixed-length string of characters, which is stored instead of the actual password. Hash functions are designed to be one-way, making it extremely difficult to reverse-engineer the original password from the hash.
3.	Salting: Adding a unique random value, known as a salt, to each password before hashing ensures that even identical passwords result in different hashes. This prevents attackers from using precomputed tables (rainbow tables) to crack passwords.
4.	Key Management: Proper management of encryption keys is crucial. This includes using secure key storage solutions, regularly rotating keys, and implementing access controls to restrict who can access the keys.
5.	Access Controls and Monitoring: Implementing strict access controls ensures that only authorized personnel have access to password keys. Additionally, continuous monitoring and logging of access to these keys can help detect and respond to any suspicious activity.
In conclusion, protecting user password keys at rest is an essential aspect of securing sensitive data and maintaining user trust. By employing a combination of encryption, hashing, salting, key management, and access controls, organizations can significantly reduce the risk of data breaches and comply with regulatory requirements.


## **Table of Contents**

- [Project Overview](#project-overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Directory Structure](#directory-structure)
- [Technical Details](#technical-details)

## **Features**

1. AES Encryption: Utilizes AES (Advanced Encryption Standard) with a 256-bit key size for robust data encryption, ensuring confidentiality of files and directories.
2. Passphrase-based Encryption: Allows users to securely encrypt files and directories using a passphrase, ensuring only authorized users can decrypt them.
3. File and Directory Handling:
•	Supports encryption and decryption of both individual files and entire directories.
•	Preserves directory structure during encryption and restores it during decryption, maintaining organizational integrity.
4. Key Management:
•	Generates random file encryption keys for each encrypted file, enhancing security.
•	Derives a secure key from the user-provided passphrase and a randomly generated salt using PBKDF2 for encryption key encryption.
5. Secure Storage of Encrypted Keys:
•	Encrypts file encryption keys using AES-CFB mode with a key derived from the passphrase and stores them alongside the encrypted data.
•	Ensures the integrity of encrypted file keys using HMAC-SHA256 for authentication.
6. Graphical User Interface (GUI):
•	Provides a user-friendly GUI using Tkinter, allowing easy file selection, passphrase input, and interaction with encryption and decryption functionalities.
•	Supports browsing for files and folders, simplifying user interaction with the application.


## **Installation**

### **Prerequisites**

- Python 3.6 or above
- Required Python libraries:
  - `Cryptography`


### **Steps**

1. **Clone the repository:**

    ```bash
    
[(https://github.com/jagadeeshreddy4881/Protecting-The-User-Passwords-At-Rest.git)](https://github.com/jagadeeshreddy4881/Protecting-The-User-Passwords-At-Rest.git) or
https://github.com/AnilKumar109109/intel]
    ```
    ![image](https://github.com/user-attachments/assets/def8dabe-907d-408e-b07f-b40b8c168de0)
    

2. •	Next we need to run ls to see what is in the directory
![image](https://github.com/user-attachments/assets/d70fc59a-eeba-4f7d-95cb-4ae226855964)
3.•	Next we need to run cd intel in order to enter the directory.
![image](https://github.com/user-attachments/assets/d9e426e3-af87-4f10-95a8-811efa30f8fe)

4.•	Next we need to run ls after getting into the intel directory.
![image](https://github.com/user-attachments/assets/d629bd71-b8d6-48e6-8140-97d5162b284c)

5.•	Next we need to run python metakey.py to display the dialog box
![image](https://github.com/user-attachments/assets/d3acb252-d673-4235-b056-14558457d793)


## **Usage**

1. **To Encrypt or Decrypt a File:**

    ```bash
    python encrypt.py
    ```

## **Directory Structure**

```plaintext
project-repo/
├── encrypt.py
├── hello.txt
├── hello.txt.enc
├── hello.txt.salt
├── README.md
```

## Technical Details

### Encryption Process

Step 1: Upon Successful implementation of the Python program in the VSCode, the File Encryptor/ Decryptor  dialog box will appear on the screen.
![image](https://github.com/user-attachments/assets/ab64cc1a-db84-444a-b811-fafa0fa400e9)
Step 2: click Browse File to browse the file that you need to encrypt.
Step 3: Select which file you need to encrypt.
![image](https://github.com/user-attachments/assets/07bb56a7-a8ee-489a-a269-b559b6c6b20b)
Step 4: Select which file you need to encrypt. click open.
![image](https://github.com/user-attachments/assets/a8bb0276-ee6d-48a2-9860-a00a86892b33)
Step 5: click encrypt.
![image](https://github.com/user-attachments/assets/655a9ce7-a472-46f2-a1c4-6ba6f10c428b)
Step 6: Enter the Passphrase for Encryption
![image](https://github.com/user-attachments/assets/2e44cf3a-51e3-48d2-87f2-81e579ad102a)
Step 7: After entering the passphrase, encryption is completed successfully.
![image](https://github.com/user-attachments/assets/0dfa2562-6a07-41ff-80dd-b90d875112a8)
Step 8: After encryption, an encrypted file and key file are generated.
![image](https://github.com/user-attachments/assets/37143507-ae67-4fba-8021-8115c254f9f1)



### Decryption Process

FILE DECRYPTION PROCESS:
Step 1: Click OK and then browse the file you need to decrypt.
![image](https://github.com/user-attachments/assets/1f2a61b9-2bd1-4b2d-ab54-2a5fc3997706)
Step 2: After selecting the encrypted file, click open.
![image](https://github.com/user-attachments/assets/f8c47752-3966-4ed8-b2dd-69fca199a9ac)
Step 3: click Decrypt to decrypt the encrypted file
![image](https://github.com/user-attachments/assets/201f2d72-2e5a-4ec0-81bc-dbe930215c56)
Step 4: After entering the passphrase for decryption, click ok.
Step 5: After clicking OK, the file was successfully decrypted.
![image](https://github.com/user-attachments/assets/2e3f3c99-4b51-4b9b-a5e5-16c328f5583c)

![image](https://github.com/user-attachments/assets/32eccfe3-fa8f-4502-b9de-612a76ba69e5)

**FOLDER ENCRYPTION PROCESS:**
Step 1: Click browse folder to encrypt the folder 
![image](https://github.com/user-attachments/assets/aca83fa4-5cf8-49dd-8948-7fe617b08b2d)
Step 2: Select the folder  and click select folder
![image](https://github.com/user-attachments/assets/e2a009c3-03ed-4980-9fec-0f78ce52bde1)
Step 3: Click encrypt to encrypt the folder
Step 4: After entering the passphrase for encryption click OK.
Step 5: After clicking "OK," the folder was successfully
encrypted.
![image](https://github.com/user-attachments/assets/3df83227-508a-40ba-8087-48d83ebabd49)
Step 6: The encrypted folder “folder.ept” was generated.
![image](https://github.com/user-attachments/assets/db85bd8d-a87a-465b-81dd-a55c0243fe7f)

 


**FOLDER DECRYPTION PROCESS:**
Step 1: Click Browse Folder to decrypt the folder.
![image](https://github.com/user-attachments/assets/b0c9abf8-1543-4301-917d-08462a652a68)
Step 2: After selecting an encrypted folder, click select folder.
![image](https://github.com/user-attachments/assets/747b6fe9-ad97-48b7-9dd6-5e1eaffb8656)
 Step 3: Click Decrypt to decrypt the folder.
 ![image](https://github.com/user-attachments/assets/91acb89a-b024-4ec4-ab0f-5fbfbdb952a2)
Step 4: After entering the passphrase for decryption click OK
![image](https://github.com/user-attachments/assets/697c424a-bee1-4511-9b0e-68195d0cbba4)
Step 5: The folder was successfully decrypted.
 ![image](https://github.com/user-attachments/assets/77f88c6a-fd8f-4eb8-a27a-ac8f9febbf68)
 
![image](https://github.com/user-attachments/assets/9fdd9e11-0e83-4646-beaf-1d97a92cb529)



 

      
    - Follow the prompts to enter your passphrase and decrypt the file.

## Requirements
- Python 3.x
- `cryptography` library

## Contact
For any questions or issues, please contact Shukoor at 
jbusired@gitam.in &  adomma@gitam.in.

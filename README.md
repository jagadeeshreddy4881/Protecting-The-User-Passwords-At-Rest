Protecting User Password Keys at Rest
Protecting user password keys at rest is paramount to ensuring the security and privacy of personal and sensitive information. "At rest" refers to data that is stored on a device or in a database as opposed to data that is actively being transferred across networks.

Importance of Protecting Password Keys
The need for robust protection mechanisms for user password keys is driven by several key factors:

Data Breaches: With the increasing frequency and sophistication of cyber-attacks, data breaches have become a significant threat. If user password keys are not properly protected, they can be easily exploited by malicious actors, leading to unauthorized access to accounts and services.
Regulatory Compliance: Various regulations and standards, such as the General Data Protection Regulation (GDPR) and the Payment Card Industry Data Security Standard (PCI DSS), mandate stringent measures for protecting sensitive data, including password keys. Non-compliance can result in severe penalties and reputational damage.
User Trust: Users expect their personal information to be handled with the highest level of security. Failure to protect user password keys can erode trust, leading to a loss of customers and a negative impact on the organization's brand.
Best Practices for Protecting Password Keys
To mitigate these risks, several best practices and technologies are employed to protect user password keys at rest:

Encryption: Encrypting password keys using strong encryption algorithms ensures that even if the data is accessed by unauthorized individuals, it remains unreadable without the appropriate decryption key.
Hashing: Password hashing involves converting the original password into a fixed-length string of characters, which is stored instead of the actual password. Hash functions are designed to be one-way, making it extremely difficult to reverse-engineer the original password from the hash.
Salting: Adding a unique random value known as a salt to each password before hashing ensures that even identical passwords result in different hashes. This prevents attackers from using precomputed tables (rainbow tables) to crack passwords.
Key Management: Proper management of encryption keys is crucial. This includes using secure key storage solutions, regularly rotating keys, and implementing access controls to restrict who can access the keys.
Access Controls and Monitoring: Implementing strict access controls ensures that only authorized personnel have access to password keys. Additionally, continuous monitoring and logging of access to these keys can help detect and respond to any suspicious activity.
Features
AES Encryption: Utilizes AES (Advanced Encryption Standard) with a 256-bit key size for robust data encryption, ensuring confidentiality of files and directories.
Passphrase-based Encryption: Allows users to securely encrypt files and directories using a passphrase, ensuring only authorized users can decrypt them.
File and Directory Handling:
Supports encryption and decryption of both individual files and entire directories.
Preserves directory structure during encryption and restores it during decryption, maintaining organizational integrity.
Key Management:
Generates random file encryption keys for each encrypted file, enhancing security.
Derives a secure key from the user-provided passphrase and a randomly generated salt using PBKDF2 for encryption key encryption.
Secure Storage of Encrypted Keys:
Encrypts file encryption keys using AES-CFB mode with a key derived from the passphrase and stores them alongside the encrypted data.
Ensures the integrity of encrypted file keys using HMAC-SHA256 for authentication.
Graphical User Interface (GUI):
Provides a user-friendly GUI using tkinter, allowing easy file selection, passphrase input, and interaction with encryption and decryption functionalities.
Supports browsing for files and folders, simplifying user interaction with the application.
Installation Process on Windows Using GitBash
Clone the repository from GitHub.
sh
Copy code
git clone <repository_link>
Navigate to the directory.
sh
Copy code
cd intel
Run the program.
sh
Copy code
python metakey.py
File and Folder Encryption and Decryption Process
File Encryption Process
Upon successful implementation of the Python program in VSCode, the File Encryptor/Decryptor dialog box will appear on the screen.
Click "Browse File" to select the file that you need to encrypt.
Select the file and click "Open".
Click "Encrypt".
Enter the passphrase for encryption.
After entering the passphrase, encryption is completed successfully.
An encrypted file and key file are generated.
File Decryption Process
Click "OK" and then browse the file you need to decrypt.
After selecting the encrypted file, click "Open".
Click "Decrypt".
Enter the passphrase for decryption and click "OK".
After clicking "OK", the file is successfully decrypted.
Folder Encryption Process
Click "Browse Folder" to encrypt the folder.
Select the folder and click "Select Folder".
Click "Encrypt".
Enter the passphrase for encryption and click "OK".
After clicking "OK", the folder is successfully encrypted.
An encrypted folder “folder.ept” is generated.
Folder Decryption Process
Click "Browse Folder" to decrypt the folder.
After selecting the encrypted folder, click "Select Folder".
Click "Decrypt".
Enter the passphrase for decryption and click "OK".
The folder is successfully decrypted.

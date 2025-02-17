# JohnTheRipper

## Objective

"To evaluate and strengthen password security by using John the Ripper to audit password strength across our systems. This tool will help identify weak, default, or compromised passwords (e.g., in user accounts, databases, or encrypted files) through controlled brute-force, dictionary, and rule-based attacks. Findings will guide actionable recommendations to enforce stronger password policies, reduce vulnerabilities, and align with cybersecurity best practices."

### Skills Learned

- Learned how to crack passwords using brute-force, dictionary, and smart rule-based attacks.  
- Got hands-on with different hash types (like MD5, SHA-256) and how to extract/convert them for testing.  
- Got comfortable with the command line for running security tools and automating tasks.  
- Discovered why strong password policies matter by spotting weak passwords (like "123456" or "password").  
- Figured out how to troubleshoot issues (like unsupported hashes) and speed up large password-cracking jobs.  
- Practiced reporting security risks and suggesting fixes, like enabling multi-factor authentication.  
- Stayed ethical by learning to test passwords responsibly, *only* with permission.  

### Tools Used
 
- **Wordlists** (like `rockyou.txt`) for dictionary attacks.  
- **`unshadow`** to merge password files (e.g., Linux `/etc/passwd` and `/etc/shadow`).  
- **`zip2john`** to extract hashes from password-protected ZIP/RAR files.  
- **Hashcat** (sometimes) to speed things up with GPU power.  
- **Bash/Python scripts** to automate repetitive tasks. 

## Steps
drag & drop screenshots here or use imgur and reference them using imgsrc

Every screenshot should have some text explaining what the screenshot is about.

Example below.

Image 1 demonstrates the use of the echo command to generate a password hash. As shown in the Image, plain text is converted into a hash using the SHA-1 algorithm, and the output is saved in a file named u1.txt.
![image1](https://github.com/user-attachments/assets/4791a922-5058-49aa-90f8-71fba57b189b)
Image 1 - Creating hash 

We have specified format like which algorithm of hash they're using eg: -MD5, -SHA1, -SHA256, etc. These values are fed into John the Ripper to crack in Image 2. We specified wordlist mode and instructed it to use rockyou.txt, one of the built-in wordlists that comes by default with most security-focused Linux distributions. and in the last we have to give the file that loaded with hash and then as you can see in Image 2 we have successfully cracked the password.  
![image](https://github.com/user-attachments/assets/49928181-8ba0-4f8d-9a1c-b7b4b1a951ac)
Image 2 - Cracking password

John has another utility called zip2john. zip2john helps us to get the hash from zip files. The below command will get the hash from the zip file and store it in the zip.txt file. and we will use John to crack the hash and we successfully cracked the zip password.
![image](https://github.com/user-attachments/assets/e26dae03-9ed9-49de-916a-2ca18d7e1865)
Image 3 - Cracking Zip password




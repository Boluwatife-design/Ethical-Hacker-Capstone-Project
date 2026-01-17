Discover user account information on a server and crack the password of Bob Smith's account. 
You will then locate the file that contains the Challenge 1 code and use Bob Smith's account credentials to open 
the file at 192.168.0.10 to view its contents.

# Step 1: Preliminary setup
- Open a browser and go to the website at 10.5.5.12.
<img width="744" height="426" alt="SET DVWA security to low" src="https://github.com/user-attachments/assets/30a4b628-47a4-4318-aa20-c62fc767155e" />


### Note: If you have problems reaching the website, remove the https:// prefix from the IP address in the browser address field.

- Login with the credentials admin / password.
- Set the DVWA security level to low and click Submit.

# Step 2: Retrieve the user credentials for the Bob Smith's account.
- Identify the table that contains usernames and passwords.

      1' OR 1=1
<img width="689" height="420" alt="display username" src="https://github.com/user-attachments/assets/213458b1-23c2-42e7-bfbf-fdf5b4920e7e" />
 
- Locate a vulnerable input form that will allow you to inject SQL commands.

      1' OR 1=1 UNION SELECT USER, Password FROM users#

- Retrieve the username and the password hash for Bob Smith's account.
<img width="725" height="384" alt="Injection to find Bob password hashes" src="https://github.com/user-attachments/assets/2f382fdb-03c5-4f91-9b39-5eb3e1015b9e" />

# Step 3: Crack Bob Smith's account password.
- Use any password hash cracking tool desired to crack Bob Smith’s password.
- Copied hash and pasted into "crackstation.net
<img width="837" height="410" alt="Crack station to crack hashes" src="https://github.com/user-attachments/assets/c0df2df3-0dcf-43ee-ab85-7e9f1bc2dd76" />
    
- What is the password of Bob Smith's account?

      Answer: password
# Step 4: Locate and open the file with Challenge 1 code.
- Log into 192.168.0.10 as Bob Smith.

      using ssh smithy@192.168.0.10
- Locate and open the flag file in the user's home directory.
- use "ls" to list file in the directory
- use "cat my_passwords.txt" to view file

      cat my_passwords.txt
  <img width="438" height="276" alt="Flag 1" src="https://github.com/user-attachments/assets/c47f4f01-37da-427b-a323-b1d3fc8a4e69" />

- What is the name of the file with the code?

      Answer: my_passwords.txt
- What is the message contained in the file? Enter the code that you find in the file.

      Congratulations!  
      You found the flag for Challenge 1!  
      The code for this challenge is 8748wf8J
  
# Step 5: Research and propose SQL attack remediation.
- Use Prepared Statements (Parameterized Queries) : Separates SQL code from user input (data) and The database never treats user input as executable SQL
- Input Validation: Ensures inputs match expected formats before reaching the database, Blocks unexpected characters that attackers rely on.
- Proper Error Handling & Logging: Prevents database errors from being shown to users. Stops attackers from learning table names, schemas, or DB type and Reduces attack feedback loop
- Use Least Privilege Database Accounts: Limits what the database user can do. Even if injection happens, damage is minimized.
- Avoid Dynamic SQL & String Concatenation: Prevents SQL queries from being built using raw strings, Eliminates the root cause of injection vulnerabilities.

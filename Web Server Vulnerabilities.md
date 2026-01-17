Find vulnerabilities on an HTTP server. 
Misconfiguration of a web server can allow for the listing of files contained in directories on the server.

# Step 1: Preliminary setup
- If not already, log into the server at 10.5.5.12 with the admin / password credentials.
- Set the application security level to low.
<img width="744" height="426" alt="SET DVWA security to low" src="https://github.com/user-attachments/assets/0d643652-59a1-4705-8010-458cfb903aad" />

# Step 2: From the results of your reconnaissance, determine which directories are viewable using a web browser and URL manipulation.
- Perform reconnaissance on the server to find directories where indexing was found using "Dirb".

      DIRB- command-line web content scanner used primarily for directory brute-forcing and
      reconnaissance during security audits or penetration testing.

      Dirb http://10.5.5.12
<img width="282" height="396" alt="directory" src="https://github.com/user-attachments/assets/d305d6e7-c925-4b8e-987a-39f096250361" />

- Which directories can be accessed through a web browser to list the files and subdirectories that they contain?

          The Config, docs and External
    
# Step 3: View the files contained in each directory to find the file containing the flag.
- Create a URL in the web browser to access the viewable subdirectories. 
- Find the file with the code for Challenge 2 located in one of the subdirectories.
<img width="260" height="217" alt="config index" src="https://github.com/user-attachments/assets/f8a900cb-fd93-4ac6-8149-1b21413cb3b1" />
<img width="290" height="232" alt="docx index" src="https://github.com/user-attachments/assets/c0e2be5b-7ea4-40cb-8dc8-0443d522d3b1" />
<img width="312" height="178" alt="External index" src="https://github.com/user-attachments/assets/a43e6b00-afb8-4d51-be7a-d50d691f5d27" />
<img width="296" height="148" alt="config flag 2" src="https://github.com/user-attachments/assets/74f2fc9d-6651-432f-9c8b-8843b9c788d7" />

- In which two subdirectories can you look for the file?

      http://10.5.5.12/config/
- What is the filename with the Challenge 2 code?

      db_form.html
- Which subdirectory held the file?

      config
- What is the message contained in the flag file? Enter the code that you find in the file.

      Great work!
      You found the flag file for Challenge 2!
      The code for this flag is:  aWe-4975
# Step 4: Research and propose directory listing exploit remediation.
- Disable Directory Listing on the Web Server: Prevents the web server from displaying the contents of directories when no index file is present, so Attackers can no longer browse files, backups, configs, or sensitive resources.
- Enforce Proper Access Controls & File Permissions: Ensures only authorized users can access directories and files, so even if directory listing is enabled accidentally, sensitive files remain inaccessible.

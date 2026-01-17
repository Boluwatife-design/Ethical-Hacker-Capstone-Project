# Step 1: Find and analyze the SA.pcap file.
- Analyze the content of the PCAP file to determine the IP address of the target computer and the URL location of the file with the Challenge 4 code.
<img width="246" height="262" alt="PCAP file" src="https://github.com/user-attachments/assets/abab88e9-31b3-427a-8ef6-4a915af1e5d0" />
<img width="940" height="343" alt="PCAP capture" src="https://github.com/user-attachments/assets/3f1ffe78-1fef-410c-8631-65132231359d" />

- What is the IP address of the target computer?

      10.5.5.11
- What directories on the target are revealed in the PCAP?

      /styles/, /javascripts/, /webservices/,/data/, /test/, /passwords/, /includes/, /icons.text/
<img width="618" height="352" alt="get password(4)" src="https://github.com/user-attachments/assets/424c445f-1d78-40d6-acde-33bae9066165" />

# Step 2: Use a web browser to display the contents of the directories on the target computer
- Use a web browser to investigate the URLs listed in the Wireshark output. Find the file with the code for Challenge 4.
<img width="365" height="210" alt="indes of pwd" src="https://github.com/user-attachments/assets/b301698f-f12b-4ed7-a215-038fba0349a6" />
<img width="618" height="352" alt="get password(4)" src="https://github.com/user-attachments/assets/b67c36f5-d865-4759-87cc-f7bf5929ada7" />
<img width="930" height="384" alt="url for flag 4" src="https://github.com/user-attachments/assets/25905f6b-ecf9-487a-9959-75b61bfa9134" />

- What is the URL of the file?

      http://10.5.5.11/data/user_accounts.xml
<img width="315" height="162" alt="flag 4 dir" src="https://github.com/user-attachments/assets/1f9d9416-bdb4-4e4b-a07b-835908f1d2e8" />

- What is the content of the file?

        <Employees>
      <Employee ID="0">
      <UserName>Flag</UserName>
      <Password>Here is the Code for Challenge 4!</Password>
      <Signature>21z-1478K</Signature>
      <Type>Flag</Type>
      </Employee>
      <Employee ID="1">
      <UserName>admin</UserName>
      <Password>adminpass</Password>
      <Signature>g0t r00t?</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="2">
      <UserName>adrian</UserName>
      <Password>somepassword</Password>
      <Signature>Zombie Films Rock!</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="3">
      <UserName>john</UserName>
      <Password>monkey</Password>
      <Signature>I like the smell of confunk</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="4">
      <UserName>jeremy</UserName>
      <Password>password</Password>
      <Signature>d1373 1337 speak</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="5">
      <UserName>bryce</UserName>
      <Password>password</Password>
      <Signature>I Love SANS</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="6">
      <UserName>samurai</UserName>
      <Password>samurai</Password>
      <Signature>Carving fools</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="7">
      <UserName>jim</UserName>
      <Password>password</Password>
      <Signature>Rome is burning</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="8">
      <UserName>bobby</UserName>
      <Password>password</Password>
      <Signature>Hank is my dad</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="9">
      <UserName>simba</UserName>
      <Password>password</Password>
      <Signature>I am a super-cat</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="10">
      <UserName>dreveil</UserName>
      <Password>password</Password>
      <Signature>Preparation H</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="11">
      <UserName>scotty</UserName>
      <Password>password</Password>
      <Signature>Scotty do</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="12">
      <UserName>cal</UserName>
      <Password>password</Password>
      <Signature>C-A-T-S Cats Cats Cats</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="13">
      <UserName>john</UserName>
      <Password>password</Password>
      <Signature>Do the Duggie!</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="14">
      <UserName>kevin</UserName>
      <Password>42</Password>
      <Signature>Doug Adams rocks</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="15">
      <UserName>dave</UserName>
      <Password>set</Password>
      <Signature>Bet on S.E.T. FTW</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="16">
      <UserName>patches</UserName>
      <Password>tortoise</Password>
      <Signature>meow</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="17">
      <UserName>rocky</UserName>
      <Password>stripes</Password>
      <Signature>treats?</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="18">
      <UserName>tim</UserName>
      <Password>lanmaster53</Password>
      <Signature>Because reconnaissance is hard to spell</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="19">
      <UserName>ABaker</UserName>
      <Password>SoSecret</Password>
      <Signature>Muffin tops only</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="20">
      <UserName>PPan</UserName>
      <Password>NotTelling</Password>
      <Signature>Where is Tinker?</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="21">
      <UserName>CHook</UserName>
      <Password>JollyRoger</Password>
      <Signature>Gator-hater</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="22">
      <UserName>james</UserName>
      <Password>i<3devs</Password>
      <Signature>Occupation: Researcher</Signature>
      <Type>Admin</Type>
      </Employee>
      <Employee ID="23">
      <UserName>ed</UserName>
      <Password>pentest</Password>
      <Signature>Commandline KungFu anyone?</Signature>
      <Type>Admin</Type>
      </Employee>
      </Employees>

  - What is the code for Challenge 4?

        21z-1478K
  <img width="453" height="370" alt="Flag 4" src="https://github.com/user-attachments/assets/9ca62918-d15b-4c97-bdea-15c035389a67" />

 # Step 3: Research and propose remediation that would prevent file content from being transmitted in clear text.
- Enforce Strong Access Controls & File Permissions: Restricts who can read files based on user identity and role, so even if someone can reach the system, they cannot read files without authorization.
- Encrypt Sensitive Files (At Rest): Ensures files are unreadable without proper decryption keys, so if files are accessed or stolen, their contents remain unintelligible.

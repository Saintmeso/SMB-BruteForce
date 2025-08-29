# Code for the bruteforce attack
The script tries many passwords automatically from the (passlist.txt) to see which one works under a specific IP and for a given username on a Windows computer via SMB protocol.

<img width="838" height="600" alt="Bruteforce Code" src="https://github.com/user-attachments/assets/1bbfe3e2-671f-473c-b690-7a77d86c1e02" />

Step-by-step:

1. Ask for input
   - Target IP address
   - Username
   - password list file
2. Set up a counter to track attempts.
3. Loop through the password list:
   - for each password in the text file, the script tries to log in using:

     (net use \\IP /user:username password)

4. Check if login succeeded:
  - If it works, it goes to (:success) and prints the password.
  - If not, it increments the counter and tries the next following password.

5. Stop after finding the password or after trying all passwords.





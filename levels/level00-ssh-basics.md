# Bandit Level 0 -> Level 1

### Mission Objective
Establish an SSH connection to the OverTheWire game server and retrieve the password for the next level.

### Technical Analysis
*   **Host:** `bandit.labs.overthewire.org`
*   **Port:** `2220` (Non-standard SSH port)
*   **User:** `bandit0`

###  Step-by-Step Execution
1. **Initial Connection:** I used the OpenSSH client to connect to the remote host. I initially faced an error by not specifying the username, which caused the server to reject my local machine's username.
2.  **Corrected Command:**
      ```bash
      ssh bandit0@bandit.labs.overthewire.org -p 2220
      ```
3.  **Authentication:** Logged in using the password `bandit0`.
4.  **Information Gathering:** Once inside, i performed an `ls` to list the directory contents and found a file named `readme`.
5.  **Password Extraction:** I used the `cat` command to read the file:
     ```bash
     cat readme
     ```
6.  **Results:** Obtained the alphanumeric string required for level 1.

###  Evidence
![Level 0 Screenshot](../assets/bandit_level0.png)


###  Key Learning
In Linux, the `cat` command is short for "concatenate." While it can merge files, its most common use in security is quickly outputting the content of a file to the terminal (STDOUT).

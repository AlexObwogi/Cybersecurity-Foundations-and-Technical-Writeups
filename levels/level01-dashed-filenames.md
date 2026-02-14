# Bandit Level 1 -> Level 2

###  **Objective**
The goal is to retrieve the password for the next level stored in a file called `-` located in the home directory.

###   **The Challenge**
In Linux, the `-` character is a "special" character. Many commands interprete a single dash as **stdin** (standard input) or the start of a command flag. If you try `cat -`, the terminal waits for you to type something rather than reading the file.

###  **Commands Used**
* `ls`: To list the files in the current directory.
* `cat`: To display the contents of the file.

###  **The Solution**
To force Linux to treat the dash as a filename, I used the **relative Path**:

```bash
cat ./-

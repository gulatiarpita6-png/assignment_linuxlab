


 # LINUX SCRIPTS REPOSITORY

This repository contains Linux shell scripts demonstrating basic scripting concepts like **loops**, **arrays**, and **user input**.

---

## 📜 Scripts Included
| **Script Name**      | **Purpose**                                      |
|----------------------|--------------------------------------------------|
| `print_numbers.sh`   | Prints numbers between a given range            |
| `array_loop.sh`      | Demonstrates array usage and loops through items |

---

# **1. Script: `print_numbers.sh`**
**Purpose:**  
To print numbers from a given **start** to **end** using a **for loop**.

---

### **Code** 

```bash
#!/bin/bash
# print_numbers.sh - Script to print numbers from start to end

# Take input from user
read -p "Enter the starting number: " start
read -p "Enter the ending number: " end

# Display range info
echo "Printing numbers from $start to $end..."

# Loop to print numbers
for (( i=$start; i<=$end; i++ ))
do
    echo $i
done

# Completion message
echo "Done!"

````
``

<img width="588" height="251" alt="image" src="https://github.com/user-attachments/assets/0b9ca94e-9e42-4196-b703-4d1ca9235931" />


# **2. Script: array_loop.sh**

**Purpose:**
To demonstrate how to store multiple values in an array and display them using a for loop.

Code
```bash
#!/bin/bash

# Declare an array
numbers=(10 20 30 40 50)

# Loop through the array
echo "Printing numbers from the array:"
for num in "${numbers[@]}"
do
    echo "Number: $num"
done

# Show total elements
echo "Total numbers: ${#numbers[@]}"

```
<img width="578" height="327" alt="image" src="https://github.com/user-attachments/assets/bdb5e6ea-6b34-4bd5-b7ac-7ad2c41662c9" />

# Linux Script questions 

1. Purpose of `#!/bin/bash` at the top of a script?
2. How to make a script executable?

---

## **1. Purpose of `#!/bin/bash`**
The line:
```bash
#!/bin/bash
```
 1. It tells the system which interpreter should execute the script.
 2. /bin/bash is the path to the Bash shell on Linux systems.
 3. Without this line, the script might fail or use the wrong shell.

 ## **2. to make script excecutable we use:** 
 
 `
step 1. chmod +x file.sh //	Make a script executable.

step 2. ./file.sh	//Run the script.

step 3. ls -l	//Check file permissions


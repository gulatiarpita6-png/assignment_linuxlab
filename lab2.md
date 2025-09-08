


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


 ```
![alt text](image-2.png)

### 2. 2. Script: array_loop.sh

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
![alt text](image-4.png)


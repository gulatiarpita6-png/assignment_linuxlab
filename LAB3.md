
# Lab 3 – Modify an Existing Script


---


### Example of Original Code:
```bash
#!/bin/bash
for i in {1..10}
do
  echo $i
done
```

**Output:**
```
1
2
3
4
5
6
7
8
9
10
```

---

## New Behavior – `enhanced_numbers.sh`
- Asks the user for **start**, **end**, and **step** values.
- Validates that:
  - Start and end must be integers.
  - Step must be a **positive integer**.
- Prints numbers from **start** to **end** using the given step.

### Example Code:
```bash
#!/bin/bash

read -p "Enter start number: " start
read -p "Enter end number: " end
read -p "Enter step value: " step



## Example Runs

### **Case 1: Valid Input**
```
$ ./enhanced_numbers.sh
Enter start number: 1
Enter end number: 10
Enter step value: 2
Printing numbers from 1 to 10 with step 2:
1
3
5
7
9
Done!
```

### **Case 2: Invalid Step**
```
$ ./enhanced_numbers.sh
Enter start number: 1
Enter end number: 5
Enter step value: -2
Error: Step cannot be zero or negative.
```

---
```
## Extra Questions

### **Q1. Difference between `$1`, `$@`, and `$#`**
| Symbol | Meaning | Example |
|--------|--------------------|----------------|
| `$1`   | First argument passed to the script | `./script.sh hello world` → `$1 = hello` |
| `$@`   | All arguments as separate strings | `"$@"` → `hello world` |
| `$#`   | Number of arguments | `./script.sh hello world` → `$# = 2` |

---

### **Q2. What does `exit 1` mean in a script?**
- `exit 0` → Script completed successfully.
- `exit 1` → Script failed due to an **error**.
- In our script, we used `exit 1` when:
  - Invalid inputs are provided.
  - Step value is zero or negative.

---

# 🐚 Shell Scripting Tutorial!!

Shell scripting allows you to **automate tasks** in Linux/Unix by writing commands inside a file that the shell executes line by line.

---

## 1. 🔹 What is a Shell Script?

* A **shell** is a command-line interpreter (e.g., `bash`, `zsh`, `sh`).
* A **shell script** is a text file with a series of commands.
* File usually has **`.sh`** extension, though not mandatory.

**Example: `hello.sh`**

```bash
#!/bin/bash
echo "Hello, World!"
```
![alt text](image6/shfirst.png)

Run it:

```bash
chmod +x hello.sh   # make it executable
./hello.sh
```
![alt text](image6/first.png)


Output:

```
Hello, World!
```

---

## 2. 🔹 Variables

Variables store data (text, numbers, paths, etc.).

### Defining variables

```bash
name="Parth"
age=18
```


⚠️ No spaces around `=`.

### Accessing variables

```bash
echo "My name is $name and I am $age years old."
```


![alt text](image6/shsecond.png)


Output:

```
My name is Parth   and I am 18 years old.
```

![alt text](image6/secondsh.png)



## 3. 🔹 User Input

Read input from user with `read`.

```bash
#!/bin/bash
echo "Enter your favorite language:"
read lang
echo "You chose $lang"
```
![alt text](image6/shthird.png)

---

Output:

![alt text](image6/third.png)

## 4. 🔹 Conditional Statements (if-else)

```bash
#!/bin/bash
num=10

if [ $num -gt 5 ]; then
    echo "Number is greater than 5"
else
    echo "Number is less than or equal to 5"
fi
```

![alt text](image6/shfourth.png)

Operators:

* `-eq` (equal)
* `-ne` (not equal)
* `-gt` (greater than)
* `-lt` (less than)
* `-ge` (greater or equal)
* `-le` (less or equal)

---

Output-

![alt text](image6/fourth.png)


### For loop

```bash
for i in 1 2 3 4 5
do
    echo "Number: $i"
done
```

![alt text](image6/fourthsh.png)


Output-
![alt text](image6/fourth2.png)


Or use a range:

```bash
for i in {1..5}
do
    echo "Iteration $i"
done
```


![alt text](image6/fourth3sh.png)


Output-

![alt text](image6/fourth3sh.png)


### While loop

```bash
count=1
while [ $count -le 5 ]
do
    echo "Count: $count"
    ((count++))   # increment
done
```
![alt text](image6/fourth4.png)


Output-

![alt text](image6/fourth4.png)


### Until loop

Runs until condition becomes true.

```bash
x=1
until [ $x -gt 5 ]
do
    echo "Value: $x"
    ((x++))
done
```
![alt text](image6/fourth5sh.png)

Output-

![alt text](image6/fourth5.png)

---

## 6. 🔹 Functions

Encapsulate reusable code.

```bash
greet() {
    echo "Hello, $1"
}

greet Parth
greet World
```

![alt text](image6/sixthsh.png)


Output:

```
Hello, Parth
Hello, World
```
![alt text](image6/sixth.png)


---


## 7. 🔹 Command Line Arguments

Access arguments passed to script:

```bash
#!/bin/bash
echo "Script name: $0"
echo "First argument: $1"
echo "Second argument: $2"
echo "All arguments: $@"
echo "Number of arguments: $#"
```

![alt text](image6/seventhsh.png)

Run:

```bash
./script.sh apple banana
```

Output:

```
Script name: ./script.sh
First argument: apple
Second argument: banana
All arguments: apple banana
Number of arguments: 2
```

![alt text](image6/seventh.png)

---


## 8. 🔹 Arrays

```bash
fruits=("apple" "banana" "cherry")

echo "First fruit: ${fruits[0]}"

for fruit in "${fruits[@]}"; do
    echo "Fruit: $fruit"
done
```

![alt text](image6/eightsh.png)

Output-

![alt text](image6/eight.png)

---

## 9. 🔹 Useful Commands in Scripts

* `date` → show current date/time
* `whoami` → show current user
* `ls` → list files
* `pwd` → print working directory
* `cat` → read file contents

---


## 10. 🔹 A Practical Example

**Backup script (`backup.sh`):**

```bash
#!/bin/bash
# Backup home directory to /tmp

backup_file="/tmp/home_backup_$(date +%Y%m%d%H%M%S).tar.gz"

tar -czf $backup_file $HOME

echo "Backup saved to $backup_file"
```

Run:

```bash
./backup.sh
```

---


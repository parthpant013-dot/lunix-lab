# Shell Scripting
# 🔹 1. **Print variables using while loop**

### Example :

```bash
#!/bin/bash

variable=("A" "B" "C")

echo "Variable[0]: ${variable[0]}"
length=${#variable[@]}
count=0

while [ $count -lt $length ]
do
    echo "count: $count"
    echo "Variable: ${variable[$count]}"
    ((count++))
done

```

![alt text](shell_script_image/while_loop.png)

Output-

![alt text](shell_script_image/whilesh.png)



---
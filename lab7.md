# Armstrong Number Checker (Bash Script)

This script checks whether a given number is an **Armstrong number**.

---


## 📜 Script

```bash
#!/bin/bash
# armstrong.sh
# Usage: ./armstrong.sh 153

if [ $# -ne 1 ]; then
  echo "Usage: $0 <non-negative-integer>"
  exit 1
fi

n="$1"
if ! [[ $n =~ ^[0-9]+$ ]]; then
  echo "Input must be a non-negative integer."
  exit 1
fi

# count digits
temp="$n"; digits=0
while [ "$temp" -gt 0 ]; do
  temp=$(( temp / 10 ))
  ((digits++))
done
# handle zero
[ $digits -eq 0 ] && digits=1

sum=0
temp="$n"
while [ "$temp" -gt 0 ]; do
  d=$(( temp % 10 ))
  # compute d^digits
  pow=1
  for ((i=0;i<digits;i++)); do pow=$(( pow * d )); done
  sum=$(( sum + pow ))
  temp=$(( temp / 10 ))
done

if [ "$sum" -eq "$n" ]; then
  echo "$n is an Armstrong number."
else
  echo "$n is NOT an Armstrong number (sum=$sum)."
fi

```
![alt text](shell_script_image/armstrong.png)

![alt text](shell_script_image/arms2.png)

---

✅ **Explanation**:  
An Armstrong number (also known as a narcissistic number) is a number that is equal to the sum of its own digits each raised to the power of the number of digits.  
For example, `153 = 1^3 + 5^3 + 3^3`.

## 📌 Usage

```bash
./armstrong.sh <number>
```

Example:

```bash
./armstrong.sh 153
```

Output:

```
153 is an Armstrong number.
```

![alt text](image7/armout.png)

---


# Prime Number Checker (Bash Script)

This script checks whether a given number is **prime**.

---

✅ **Explanation**:  
A prime number is a number greater than 1 that has no divisors other than 1 and itself.  
For example: `17` is prime, but `18` is not because it is divisible by `2`, `3`, `6`, and `9`.

## 📜 Script

```bash
#!/bin/bash
# prime_check.sh
# Usage: ./prime_check.sh 17

if [ $# -ne 1 ]; then
  echo "Usage: $0 <positive-integer>"
  exit 1
fi

n=$1
if ! [[ $n =~ ^[0-9]+$ ]] || [ "$n" -le 1 ]; then
  echo "$n is not a prime (need integer > 1)."
  exit 1
fi

is_prime=1
i=2
while [ $((i * i)) -le "$n" ]; do
  if [ $((n % i)) -eq 0 ]; then
    is_prime=0
    break
  fi
  ((i++))
done

if [ $is_prime -eq 1 ]; then
  echo "$n is prime."
else
  echo "$n is NOT prime (divisible by $i)."
fi

```

![alt text](image7/prinw.png)

---


## 📌 Usage

```bash
./prime_check.sh <number>
```

Example:

```bash
./prime_check.sh 17
```

Output:

```
17 is prime.
```

![alt text](image7/primenoout.png)


---


# Sum of Digits (Bash Script)

This script calculates the **sum of digits** of a given non-negative integer.

---


## 📜 Script

```bash
#!/bin/bash
# sum_digits.sh
# Usage: ./sum_digits.sh 1234

if [ $# -ne 1 ]; then
  echo "Usage: $0 <non-negative-integer>"
  exit 1
fi

num="$1"
if ! [[ $num =~ ^[0-9]+$ ]]; then
  echo "Input must be a non-negative integer."
  exit 1
fi

sum=0
while [ "$num" -gt 0 ]; do
  digit=$(( num % 10 ))
  sum=$(( sum + digit ))
  num=$(( num / 10 ))
done

echo "Sum of digits: $sum"

```
![alt text](image7/sumdig.png)

---

## 📌 Usage

```bash
./sum_digits.sh <number>
```

Example:

```bash
./sum_digits.sh 1234
```

Output:

```
Sum of digits: 10
```

![alt text](image7/sumdigout.png)

---
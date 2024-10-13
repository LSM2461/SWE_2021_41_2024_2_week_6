# SWE_2021_41_2024_2_week_6
## Week 4 Assignment
###
>  Link of week 4 repository
>> https://github.com/LSM2461/SWE_2021_41_2024_2_week_4
### 
```python
def isHappy(n):
  # Initialize an empty list for tracking numbers in the loop
  loop = []
  sum = 0
  s1 = str(n)

  # Calculate the sum of squares of digits
  for i in range(len(s1)):
    sum += int(s1[i]) ** 2

  # Start an infinite loop to determine if it's a happy number
  while(True):
    # **If the sum value is 1, return True (Happy Number)**
    if(sum == 1):
      return True
    else:
      s2 = str(sum)

      # *Check if the sum is already in the loop*
      # **If it's a sycle, return False (not Happy Number)**
      if(s2 in loop):
        return False
      else:
        # Add the current sum value to the loop and reset the sum value to 0
        loop.append(s2)
        sum = 0

        # Recalculate the sum of squares of digits for the new number
        for i in range(len(s2)):
          sum += int(s2[i]) ** 2
```
### 


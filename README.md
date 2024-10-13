# SWE_2021_41_2024_2_week_6
## Week 4 Assignment
###
>  Link of week 4 repository
>> https://github.com/LSM2461/SWE_2021_41_2024_2_week_4
### 
```python
def isHappy(n):
  loop = []
  sum = 0
  s1 = str(n)
  
  for i in range(len(s1)):
    sum += int(s1[i]) ** 2
  while(True):
    if(sum == 1):
      return True
    else:
      s2 = str(sum)
      if(s2 in loop):
        return False
      else:
        loop.append(s2)
        sum = 0
        
        for i in range(len(s2)):
          sum += int(s2[i]) ** 2
```
### 


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
    # If the sum value is 1, return True (Happy Number)
    if(sum == 1):
      return True
    else:
      s2 = str(sum)

      # Check if the sum is already in the loop
      # If it's a sycle, return False (not Happy Number)
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
> Goal of the code
>> To determine whether the given number is a **"Happy Number"**
###
> Variables used in the code
>> 1. **loop**: a list for tracking the numbers generated during the process
>> 2. **sum**: cumulative value added by the sqaures of the next digit of the numbers
>> 3. **s1**: string value of the given number *n*
>> 4. **s2**: string value of the generated new nubmers during the process
###
> Core idea of the code
>> + If the sum value is already in the loop, *n* is **not a happy number**
>> + If the sum value reaches *1*, *n* is **a happy number**

## Week 5 Assignment
###
<pre>
  <code>
    docker exec ossp-container cat /etc/os-release
  </code>
</pre>

The result will show the **information about the operating system running inside the container**. \
\
**My output: \
PRETTY_NAME="Ubuntu 24.04.1 LTS" \
NAME="Ubuntu" \
VERSION_ID="24.04" \
VERSION="24.04.1 LTS (Noble Numbat)" \
VERSION_CODENAME=noble \
ID=ubuntu \
ID_LIKE=debian \
HOME_URL="https://www.ubuntu.com/" \
SUPPORT_URL="https://help.ubuntu.com/" \
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/" \
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy" \
UBUNTU_CODENAME=noble \
LOGO=ubuntu-logo**

###
<pre>
  <code>
    docker exec ossp-container git --version
  </code>
</pre>

The result will show the **Git version** installed in the container. \
\
**My output: git version 2.43.0**

###
<pre>
  <code>
    docker exec ossp-container python3 --version
  </code>
</pre>

The result will show the **Python version** installed in the container. \
\
**My output: Python 3.12.3**

###
<pre>
  <code>
    docker inspect --format="{{ .HostConfig.Binds }}" ossp-container
  </code>
</pre>

The result will show the **directory path from the host that is mounted inside the container** \
\
**My output: [/Users/임수민/Desktop/ossp_host_dir:/mnt/ossp_container_dir]**

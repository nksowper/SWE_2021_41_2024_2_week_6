# SWE_2021_41_2024_2_week_6

---

## Week 4 Assignment

* [Repository Link](https://github.com/nksowper/SWE_2021_41_2024_2_week_4)
```python
def isHappy(n):
    checklist = [0 for _ in range(1000)]
    sum = 0
    while(True):
        while(n):
            sum = sum +(n%10)**2
            n = n//10
        if(sum == 1):
            return True
        if(checklist[sum]==1):
            return False
        checklist[sum] = 1
        n = sum
        sum = 0

num = int(input())

if(isHappy(num)):
    print("True")
else:
    print("False")
```
* During calculation, if a value that has already appeared comes up again, it will repeat infinitely. So, I created checklist to check whether the value has already appeared. If value of checklist[sum] is equals to 1 it returns False, otherwise it returns True.

---
## Week 5 Assignment
> ```bash
>  docker exec ossp-container cat /etc/os-realease
> ```
> * This command displays details about the operating system of the ossp-container. The operating system of my container is **Ubuntu 24.04.1 LTS**.

> ```bash
>  docker exec ossp-container git --version
> ```
>  * This command displays the version of Git that is installed in the ossp-container. The version of Git  is **git version 2.43.0**.

> ```bash
>  docker exec ossp-container python3 --version
> ```
>  * This command displays the version of Python that is installed in the ossp-container. The version of Python is **Python 3.12.3**.

> ```bash
>  docker inspect --format="{{ .HostConfig.Binds }}" ossp-container
> ```
>  * This command displays the path of mounted directory of the ossp-container. In my case, the result is **[./ossp_host_dir:/mnt/ossp_container_dir]**.

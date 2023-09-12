# QUIZ 072

<img width="1353" alt="Screenshot 2023-09-13 at 12 59 46 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/03f5f10d-74c6-4d71-aabb-488e5574a702">

## Written code

![image](https://github.com/Madaniarias/Year-2/assets/111761417/92294aa0-3f60-4b9f-aad8-47b8d03df3aa)

## Code

```.py

import random

def hex_num(digit: int):
    return '0123456789abcdef'[digit]

def get_mac_number():
    return hex_num(random.randint(0, 15))

def get_group_mac_numbers():
    numbers = [get_mac_number() for _ in range(2)]
    return ''.join(numbers)

def get_mac_address():
    address = [get_group_mac_numbers() for _ in range(6)]
    return ':'.join(address)

def macgenerator(N: int):
    out = []
    for _ in range(N):
        out.append(get_mac_address())
    return out

print(macgenerator(N=10))

```

## Test

<img width="1777" alt="Screenshot 2023-09-13 at 1 14 51 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/f39d2b29-79eb-42db-ba51-8ff86c591125">


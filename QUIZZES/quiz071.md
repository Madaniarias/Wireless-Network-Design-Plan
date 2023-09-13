# QUIZ 071

<img width="1407" alt="Screenshot 2023-09-13 at 12 07 37 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/cb4f03e0-83f7-40b0-97e7-5dcea57e4416">

## Written code

![image](https://github.com/Madaniarias/Year-2/assets/111761417/cf5778a9-2692-439b-8175-ca16fe24a2c1)

## Code

```.py
import random

#create class
class IPv6machine:
    def __init__(self, N):
        self.N = N

    # Generate a random IPv6
    def generate_ipv6_address(self):
        ipv6_parts = ["".join(random.choices("0123456789abcdef", k=4)) for _ in range(8)]
        ipv6_address = ":".join(ipv6_parts)
        return ipv6_address

    # Generate N random IPv6 addresses
    def generate_ipv6_addresses(self):
        ipv6_addresses = [self.generate_ipv6_address() for _ in range(self.N)]
        return ipv6_addresses

#Test
ipv6_machine = IPv6machine(N=10)
random_ipv6_addresses = ipv6_machine.generate_ipv6_addresses()
print(random_ipv6_addresses)
```

## Test
<img width="1774" alt="Screenshot 2023-09-13 at 12 57 37 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/a0067842-5c61-4233-a7dd-d647b708896b">

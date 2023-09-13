# QUIZ 070

<img width="1365" alt="Screenshot 2023-09-13 at 12 02 26 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/d9ead158-2e37-4e9d-b5f2-9ed1b99bfaf0">

# Written code

![image](https://github.com/Madaniarias/Year-2/assets/111761417/63e72b3f-393e-4b6b-a766-26a5054e5944)

# Code

```.py
#create IPv4machine class
class IPv4machine:
    def generate_addresses(self):
        return (f"{a}.{b}.{c}.{d}" for a in range(0,256) for b in range(0,256) for c in range(0,256) for d in range(0,256))

# Instance of the IPv4Generator class
ip_generator = IPv4machine()

# call ip_generator to iterate and print IPv4 addresses
for ip_address in ip_generator.generate_addresses():
    print(ip_address)
```

# Test

<img width="274" alt="Screenshot 2023-09-13 at 12 03 53 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/b34285b2-66f3-4d3e-a762-8c98fd34c8f9">


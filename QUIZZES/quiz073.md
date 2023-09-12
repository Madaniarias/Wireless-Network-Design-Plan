# QUIZ 073

<img width="1396" alt="Screenshot 2023-09-13 at 1 17 43 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/7bb54511-58f5-4e31-9527-a8ad7f491990">

## Written code

![image](https://github.com/Madaniarias/Year-2/assets/111761417/ceae6fdc-6db5-4241-b57e-487b2b244ee9)

## Code

```.py
import random
def check_mac(MAC):
    return len(MAC) == 17 and MAC.count(":") == 5

def generate_ipv4():
    ipv4 = ".".join(str(random.randint(0, 255)) for a in range(4))
    return ipv4

def update(table, MAC):
    if check_mac(MAC):
        if MAC in table:
            return table[MAC]
        else:
            while True:
                ip = generate_ipv4()
                if ip not in table.values():
                    table[MAC] = ip
                    return ip

def display_addresses(table):
    print("Routing Table:")
    for MAC, IP in table.items():
        print(f"MAC address: {MAC}, IP address: {IP}")


table = {}
while True:
    mac_address = input("Enter MAC address (xx:xx:xx:xx:xx:xx): ")
    if check_mac(mac_address):
        ip_address = update(table, mac_address)
        print(f"Assigned IP address: {ip_address}")
    else:
        print("Invalid MAC address format. Please use xx:xx:xx:xx:xx:xx format.")
    display_addresses(table)

```

## Test

<img width="1396" alt="Screenshot 2023-09-13 at 2 18 18 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/837191d6-110b-429b-a473-05ffbfb2f0d8">

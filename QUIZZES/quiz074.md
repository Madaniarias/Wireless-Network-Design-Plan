# QUIZ 074

<img width="1396" alt="Screenshot 2023-09-13 at 2 28 21 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/72da9ce2-2e05-4560-8b4c-e3b9289a86c6">

## Written code

## Code

```.py
def build_data_packages(mac_sender, ip_sender, mac_receiver, ip_receiver, data):
    package_size = 4  # pack size

    packages = [] #list to store packs

    # number of packages required
    num_packages = (len(data) + package_size - 1) // package_size

    for sequence_number in range(num_packages):
        #  Separate current package content
        start_idx = sequence_number * package_size
        end_idx = start_idx + package_size
        package_data = data[start_idx:end_idx]

        # Format for the display
        header = f"{mac_sender}|{ip_sender}|{mac_receiver}|{ip_receiver}|{sequence_number}|"

        # header + package data (format + info)
        package = header + package_data
        packages.append(package)

    return packages

# Test
input_mac_sender = "80:90:AA:F0:22:11"
input_ip_sender = "192.168.1.2"
input_mac_receiver = "30:AA:1A:F1:00:AE"
input_ip_receiver = "192.168.1.3"
input_data = "Hello world"

result = build_data_packages(input_mac_sender, input_ip_sender, input_mac_receiver, input_ip_receiver, input_data)
print(result)
```

## Test

Case 1: word: Hello World
<img width="1770" alt="Screenshot 2023-09-13 at 9 58 01 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/48b2496c-afb0-47e2-94f5-d9f5ec230f9d">

Case 2: word: Hello
<img width="1396" alt="Screenshot 2023-09-13 at 9 57 42 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/9329e8e5-bbe2-462c-82ba-b7fa0dd4154c">


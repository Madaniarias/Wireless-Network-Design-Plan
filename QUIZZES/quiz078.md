# QUIZ 078

<img width="553" alt="Screenshot 2023-09-16 at 5 57 26 PM" src="https://github.com/Madaniarias/Year-2/assets/111761417/f961c468-de8f-4fcc-a2b3-c897bd12e2ab">

## Written code

![IMG-5754](https://github.com/Madaniarias/Year-2/assets/111761417/1e158244-5eeb-4114-a669-121f99251552)

## Code

```.py

class MariasFirewall:
    def __init__(self, data: str):
        #Initialize data
        self.data = data

    #create function find port
    def find_port(self):
        # This part converts to decimal
        # 1. self.data [:16] Takes the first 16 numbers from the string
        # 2. The ",2" says that the number is in base 2 (says that number is in binary)
        # 3. int() transforms number to decimal with the past info given
        port = int(self.data[:16], 2)
        return port

    #create function to errormsg
    def errormsg(self):
        port = self.find_port()
        #in this line i create a set with "{}" o 2 unique integers.
        #this line checks if the port is allowed or not, filters if needed
        if port in {80, 22123}:
            #if any of the ports allowed print
            return "Allowed", self.data[16:]
        # If it is not allowed always return "filtered , not allowed"
        return "Filtered", "not allowed"

test1 = MariasFirewall("100111001011001110010110011100101")
result, data = test1.errormsg()
print(f"Port: {test1.find_port()}, Result: {result}, Data: {data}")

test2 = MariasFirewall("010101100110101111110111001111")
result, data = test2.errormsg()
print(f"Port: {test2.find_port()}, Result: {result}, Data: {data}")

```

## Test

<img width="1340" alt="Screenshot 2023-09-16 at 9 50 26 PM" src="https://github.com/Madaniarias/Year-2/assets/111761417/a354a7c1-8b0c-4f35-a14f-689c24cfa4c0">


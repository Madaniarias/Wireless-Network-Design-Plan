# QUIZ 077

<img width="1396" alt="Screenshot 2023-09-13 at 2 33 09 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/ce9e8ac7-ec34-4872-a9dc-139e72d670a3">

## Written code


## Code

```.py
def parity_check(data):
    ones_count = 0

    # Iterate for every bit in the data (start at bit 2)
    for bit in data[1:]:
        # bit to integer -> add to count
        ones_count += int(bit)

    # Check if the parity bit matches the count of '1' bits
    if ones_count % 2 == int(data[0]):
        return True  # Parity check passed
    else:
        return False  # Parity check failed

# Example usage:
test1 = "100111001011001110010110011100101"
test2 = "011101111101110111110111001111"

result1 = parity_check(test1)
result2 = parity_check(test2)

print("Parity Check Case 1:", result1)
print("Parity Check Case 2:", result2)
```

## Test
<img width="1396" alt="Screenshot 2023-09-13 at 9 35 29 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/38f130c7-a0ff-4d22-955f-c8dae723b5f7">

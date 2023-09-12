# QUIZ 075

<img width="1396" alt="Screenshot 2023-09-13 at 2 31 53 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/ff8843bb-f76e-4468-a185-fca9df4d70df">

## Written code

![image](https://github.com/Madaniarias/Year-2/assets/111761417/46723851-f90a-4139-bea3-5f3eaee39b35)

## Code

```.py
def send_bits(word: str) -> str:
    binary_result = ""  # Initialize an empty string

    # Loop through each character in the input word
    for char in word:
        letter = ord(char)  # Get the ASCII value
        binary_letter = bin(letter)[2:]  # Convert the ASCII to binary
        binary_letter = "0" * (8 - len(binary_letter)) + binary_letter
        binary_result += binary_letter  # Append the binary

    return binary_result

word = "Hello World!"
binary_word = send_bits(word)
print(binary_word)
```

## Test

<img width="1396" alt="Screenshot 2023-09-13 at 2 42 46 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/a60b4ae0-4d7f-4728-941a-b4e3fcad7fbf">

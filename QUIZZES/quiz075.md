# QUIZ 075

<img width="1396" alt="Screenshot 2023-09-13 at 2 31 53 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/ff8843bb-f76e-4468-a185-fca9df4d70df">

## Written code

![image](https://github.com/Madaniarias/Year-2/assets/111761417/b6fffeb5-3216-4bc8-a384-a2e6d1a62a49)

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

# QUIZ 076

<img width="1396" alt="Screenshot 2023-09-13 at 2 32 36 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/4b98e496-a3e5-40bb-812f-b73db1a9ac89">

## Written code

![image](https://github.com/Madaniarias/Year-2/assets/111761417/7295f4d7-25c9-41db-8f3c-48a49ab4d8c9)
![image](https://github.com/Madaniarias/Year-2/assets/111761417/ece249c4-2098-4610-be6b-43204c332239)

## Code

```.py
# Create ErrorDetection class
class ErrorDetection:
    def __init__(self):
        self.error = False  # Initialize error 
        self.error_list = []  # Initialize list to store error positions

    # Check for errors in the data
    def check_errors(self, data):
        data_count = len(data) // 3
        for i in range(data_count):
            # Check if any of the three copies of the data differ
            if (
                    data[i] != data[i + data_count]
                    or data[i + data_count] != data[i + 2 * data_count]
                    or data[i] != data[i + 2 * data_count]
            ):
                self.error = True  # Set error flag if an error is found
                self.error_list.append(i)  # Record the position of the error

    # Correct errors in the data
    def correct_errors(self, data):
        if self.error:
            data_count = len(data) // 3
            for i in self.error_list:
                # Correct errors by choosing the majority value among three copies (more 0 or more 1)
                corrected_bit = max(
                    data[i], data[i + data_count], data[i + 2 * data_count]
                )
                data[i] = corrected_bit
                data[i + data_count] = corrected_bit
                data[i + 2 * data_count] = corrected_bit

        return data


# Input data
input_data = "100111001011001110010110011100101"

# Convert input data into list of integers
data = [int(bit) for bit in input_data]

# instance of the ErrorDetection class
error_detector = ErrorDetection()

# Error checking in data
error_detector.check_errors(data)

# If errors are detected, attempt to correct them (display confirmation)
if error_detector.error:
    print("Errors detected. Attempting to correct...")

    # Corrected data
    corrected_data = error_detector.correct_errors(data)

    # Convert corrected data to a string
    corrected_data_str = "".join(str(bit) for bit in corrected_data)

    # Print correct data
    print("Corrected data:", corrected_data_str)
else:
    print("No errors detected. Data is valid.")

```

## Test
Case #1 (No error): input: 100111001011001110010110011100101
<img width="1396" alt="Screenshot 2023-09-13 at 8 26 21 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/82a601b8-59db-4f7e-bbe5-c84b5804c78c">

Case #1 (Error): input: 100111001011001110010110011100100 (change last digit to 0 instead of 1)
<img width="1396" alt="Screenshot 2023-09-13 at 8 27 42 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/dd299468-6cb2-4469-a098-e63d495b2242">

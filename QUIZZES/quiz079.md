# QUIZ 079
<img width="1421" alt="Screenshot 2023-10-10 at 7 54 43 PM" src="https://github.com/Madaniarias/Year-2/assets/111761417/c5cd83a5-2b61-4a69-97fa-20a8d3f427fd">

## Written code

## Code

```.py
# Class for checking if a number is palindromic
class PalindromeChecker:
    def is_palindromic(number):
        # Convert number to a string to check if palindromic 
        number_str = str(number)
        return number_str == number_str[::-1]

# Class for finding palindromic numbers in a certain range
class PalindromicNumberFinder:
    def find_palindromic_numbers(self, start, end):
        # empty list 
        palindromic_numbers = []

        # Iterate through the range of numbers from the start to the end. (+ 1 to get last) 
        for number in range(start, end + 1):
            # Check if the number is palindromic using the PalindromeChecker class
            if PalindromeChecker.is_palindromic(number):
                # If palindromic, add it to the list 
                palindromic_numbers.append(number)

        # Return the list of palindromic numbers 
        return palindromic_numbers

# Create instance 
finder = PalindromicNumberFinder()

# test 1
start_range = 1
end_range = 9
result1 = finder.find_palindromic_numbers(start_range, end_range)
print(result1) 

# Test 2
start_range = 10
end_range = 199
result2 = finder.find_palindromic_numbers(start_range, end_range)
print(resu

```

## Test
<img width="1289" alt="Screenshot 2023-10-30 at 10 19 05 AM" src="https://github.com/Madaniarias/Year-2/assets/111761417/496e1aec-3fe7-4efa-bc41-97d228c7eadb">

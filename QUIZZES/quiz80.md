# QUIZ 080
<img width="1421" alt="Screenshot 2023-10-10 at 7 55 36 PM" src="https://github.com/Madaniarias/Year-2/assets/111761417/d47e38e8-fe11-492c-9772-6b757d041741">

## Written code

## Code

```.py
class EmployeeNameSorter:
    def __init__(self, names):
        self.names = names

    def sort_names_alphabetically(self):
        # Sort the names in alphabetical order
        self.names.sort()

    def get_sorted_names(self):
        return self.names


# Initialize the collection of names
names_collection = ["Smith, Jane", "Doe, Bob"]

# Create instance of the EmployeeNameSorter class
name_sorter = EmployeeNameSorter(names_collection)
# Sort alphabetically
name_sorter.sort_names_alphabetically()
# sorted names
sorted_names = name_sorter.get_sorted_names()
print("Sorted:", sorted_names)

```

## Test
<img width="1289" alt="Screenshot 2023-10-30 at 3 51 46 PM" src="https://github.com/Madaniarias/Year-2/assets/111761417/5e5de00f-9f19-4010-8f05-244b1951e453">


from statistics import median, multimode

# Function 1: Calculate the sum
def sum_numbers(numbers):
    return sum(numbers)


# Function 2: Calculate the average (mean)
def average(numbers):
    if len(numbers) == 0:
        return 0
    return sum(numbers) / len(numbers)


# Function 3: Calculate the median and mode
def median_mode(numbers):
    if len(numbers) == 0:
        return None, []

    med = median(numbers)
    mod = multimode(numbers)

    return med, mod


# Example usage
my_list = [2, 4, 4, 6, 8]

print("Sum:", sum_numbers(my_list))
print("Average:", average(my_list))

med, mod = median_mode(my_list)
print("Median:", med)
print("Mode:", mod)

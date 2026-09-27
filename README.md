# wk11d02ex01_compute_average.py



"""
PROGCON Week 11 - Test Results and Reflection Summary

1. Four Test Arrays and Averages:
   - [22, 9, 0, 17] -> Sum: 48, Count: 4, Average: 12.0
   - [22, 0, 49, 8]  -> Sum: 79, Count: 4, Average: 19.75
   - [35, 13, 22, 0] -> Sum: 70, Count: 4, Average: 17.5
   - [10, 5, -4, 27] -> Sum: 38, Count: 4, Average: 9.5

2. Correctness Judgments and Reflections:
   - All calculated averages matched the expected manual outputs accurately.
   - The debugged program successfully computes the true mathematical mean of the entire list, avoiding the early-return and division-by-zero flaws found in the original pseudocode.
"""

# Main Program: Compute Average Workflow
print("Hey there! This program displays the final average of the numbers you input.")
print("How many numbers do you need the program to average?")

# Get the count of numbers from the user
count_input = int(input())

# Initialize the array and variables
numbers = [0] * count_input
total = 0

# Loop to gather inputs from the user
for i in range(0, len(numbers), 1):
    print("Input the value of the " + str(i + 1) + " number:")
    numbers[i] = int(input())

# Loop to process the inputs and accumulate the total sum
for i in range(0, len(numbers), 1):
    num = numbers[i]
    total = total + num

# Calculate and display the final average cleanly at the end
if len(numbers) > 0:
    average = total / len(numbers)
    print("The final average is: " + str(average))
else:
    print("No numbers were provided.")

# **Python Assignment 03**

## **Overview**

In this assignment, you’ll practice the following Python fundamentals:

1. **Variables and basic data types (strings, integers, floats).**
2. **Getting user input and type casting.**
3. **String methods** (e.g., `upper()`, `lower()`, `strip()`, `replace()`, etc.).
4. **Basic arithmetic with numbers.**
5. **List creation, indexing, and methods** (`append()`, `remove()`, slicing, etc.).

## **The assignment is broken into several parts. Complete the core tasks first (Parts 1–3), and then try the extra challenges (Part 4) if you want to go deeper.**

## **Part 1: Working with Variables, Input, and Strings**

1. **Prompt for user input**

   - Ask the user to enter their full name and store it in a variable named `full_name`.
   - Print a greeting message, for example:

   ```python
   Hello, <full_name>! Welcome to the Python assignment.
   ```

2. **String methods**

   - Print the user’s name in **all uppercase** letters.
   - Print the user’s name in **all lowercase** letters.
   - Print the **length** of the user’s name (number of characters).
   - Replace all the **spaces** in the user’s name with **hyphens** (`-`), and print the result.
   - **Bonus**: Trim any leading or trailing spaces (if any) from the user’s name using `strip()`.

3. **Type casting and numeric operations**

   - Ask the user to enter their **birth year** (as input). Convert that input to an integer.
   - Calculate the user’s approximate age by subtracting the birth year from the **current year**. Print the result in a sentence.
   - Example output:

   ```python
   You are approximately 25 years old.
   ```

---

## **Example Output (Walkthrough)**

```text
Enter your full name:  John Doe
Hello, John Doe! Welcome to the Python assignment.
Your name in uppercase: JOHN DOE
Your name in lowercase: john doe
Length of your name: 8
Name with hyphens: John-Doe
Current year is 2024, so you are approximately 24 years old.

```

## **Part 2: Lists and Indexing**

1. **Create a list from user input**

   - Prompt the user to enter three of their favorite fruits (e.g., `"apple,banana,orange"`) in one line, separated by **commas**.
   - Split the string by commas to create a list called `fruit_list`.
   - Print the list to verify that it’s correct.

2. **List indexing and slicing**

   - Print the **first** fruit in the list.
   - Print the **last** fruit in the list.
   - Print the **second** fruit in the list using indexing (i.e., `fruit_list[1]`).
   - Print the **slice** of the list containing the first two fruits.

3. **List methods**
   - **Append** a new fruit to the list using `append()`. Print the updated list.
   - **Remove** one fruit from the list using `remove()` (or `pop()`). Print the updated list again.
   - Print the **length** of the list using `len()`.

---

## **Example Output (Walkthrough)**

```text
Enter three of your favorite fruits (comma-separated): apple, banana, mango
Your list of fruits: ['apple', ' banana', ' mango']
First fruit: apple
Last fruit:  mango
Second fruit:  banana
First two fruits: ['apple', ' banana']
Adding a new fruit...
Updated list: ['apple', ' banana', ' mango', 'strawberry']
Removing one fruit...
Updated list: ['apple', ' banana', 'strawberry']
Length of the list is now 3
```

## **Part 3 (Optional Challenge): Combining Concepts**

1. **String & List Interaction**

   - Create a new list from the letters of your `full_name` (excluding spaces).

     **Hint**:

     ```python
     letters_list = list(full_name.replace(" ", ""))
     ```

   - Print the **first 3 letters** and the **last 3 letters** of `letters_list`.

2. **Manipulate and Reconstruct**

   - Convert the **first 3 letters** of `letters_list` to uppercase, and the **rest** to lowercase.
   - Reconstruct the name from `letters_list` back into a string using `"".join(...)` and print it out.

3. **Simple Arithmetic on a List of Numbers**
   - Prompt the user to enter **5 numbers** (e.g., `"10 20 30 40 50"`) in one line, separated by spaces.
   - Convert each input into an integer and store all in a list called `numbers_list`.
   - Print the **sum** of the numbers, and the **average** (sum / length of the list).

---

## **Example Output (Walkthrough)**

```text
Creating a letters list from your full name...
First 3 letters: ['J', 'o', 'h']
Last 3 letters: ['D', 'o', 'e']
Reconstructing name with some modifications...
Modified name: JOHdoe
Enter 5 numbers (space-separated): 10 20 30 40 50
Sum of your numbers: 150
Average of your numbers: 30.0
```

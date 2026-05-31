
# Arrays and Strings in C# - Complete Beginner to Developer Guide

## Why Learn Arrays and Strings?

Arrays and Strings are two of the most fundamental concepts in programming.

Almost every application you build will use them:

- User names
- Product lists
- Student records
- Search systems
- APIs
- Databases
- Games

Mastering Arrays and Strings early makes learning Data Structures and Algorithms much easier.

---

# What is an Array?

An Array is a collection of elements of the same data type stored together.

Think of an array as a row of lockers.

```text
Index:   0   1   2   3   4
Value:  80  75  90  88  95
```

Each value has a position called an index.

Arrays use zero-based indexing.

---

# Why Arrays Start From 0

Arrays start at index 0 because memory addresses are calculated efficiently.

```text
Address of element =
BaseAddress + (Index × SizeOfDataType)
```

This makes accessing elements extremely fast.

---

# Creating Arrays

## Method 1

```csharp
int[] numbers = { 10, 20, 30, 40, 50 };
```

## Method 2

```csharp
int[] numbers = new int[5];
```

This creates space for 5 integers.

---

# Accessing Elements

```csharp
int[] numbers = { 10, 20, 30 };

Console.WriteLine(numbers[0]);
```

Output:

```text
10
```

---

# Updating Elements

```csharp
numbers[1] = 99;
```

Before:

```text
10 20 30
```

After:

```text
10 99 30
```

---

# Array Length

```csharp
Console.WriteLine(numbers.Length);
```

Output:

```text
3
```

---

# Traversing Arrays

## Using for loop

```csharp
for (int i = 0; i < numbers.Length; i++)
{
    Console.WriteLine(numbers[i]);
}
```

## Using foreach loop

```csharp
foreach (int number in numbers)
{
    Console.WriteLine(number);
}
```

Many C# developers prefer foreach when modification is not required.

---

# Common Array Operations

## Find Maximum

```csharp
int max = numbers[0];

foreach (int number in numbers)
{
    if (number > max)
    {
        max = number;
    }
}
```

---

## Find Minimum

```csharp
int min = numbers[0];

foreach (int number in numbers)
{
    if (number < min)
    {
        min = number;
    }
}
```

---

## Calculate Sum

```csharp
int sum = 0;

foreach (int number in numbers)
{
    sum += number;
}
```

---

# Important Array Facts

- Arrays store homogeneous data.
- Size is fixed after creation.
- Accessing by index is O(1).
- Searching is usually O(n).
- Memory is allocated contiguously.

---

# Common Beginner Mistake

```csharp
int[] numbers = { 10, 20, 30 };

Console.WriteLine(numbers[3]);
```

Error:

```text
IndexOutOfRangeException
```

Valid indexes:

```text
0 1 2
```

---

# What is a String?

A String is a sequence of characters.

```csharp
string name = "John";
```

Visualized:

```text
J o h n
0 1 2 3
```

---

# Strings Are Immutable

This is one of the most important C# concepts.

```csharp
string name = "John";
name = "Jack";
```

The original string is not modified.

A completely new string is created.

This behavior helps make strings safer and easier to manage.

---

# Accessing Characters

```csharp
string word = "Hello";

Console.WriteLine(word[0]);
```

Output:

```text
H
```

---

# String Length

```csharp
Console.WriteLine(word.Length);
```

Output:

```text
5
```

---

# Loop Through a String

```csharp
for (int i = 0; i < word.Length; i++)
{
    Console.WriteLine(word[i]);
}
```

---

# String Concatenation

## Traditional

```csharp
string firstName = "John";
string lastName = "Doe";

string fullName = firstName + " " + lastName;
```

---

## String Interpolation (Recommended)

```csharp
string fullName = $"{firstName} {lastName}";
```

Modern C# projects use interpolation extensively.

---

# String Comparison

```csharp
string name1 = "John";
string name2 = "John";

Console.WriteLine(name1 == name2);
```

Output:

```text
True
```

---

# Useful String Methods

## Contains

```csharp
string text = "Hello World";

Console.WriteLine(text.Contains("World"));
```

Output:

```text
True
```

---

## StartsWith

```csharp
text.StartsWith("Hello");
```

---

## EndsWith

```csharp
text.EndsWith("World");
```

---

## ToUpper

```csharp
text.ToUpper();
```

Output:

```text
HELLO WORLD
```

---

## ToLower

```csharp
text.ToLower();
```

Output:

```text
hello world
```

---

## Replace

```csharp
text.Replace("World", "C#");
```

Output:

```text
Hello C#
```

---

## Split

```csharp
string data = "Apple,Banana,Mango";

string[] fruits = data.Split(',');
```

Result:

```text
Apple
Banana
Mango
```

---

# Array vs String

| Feature | Array | String |
|----------|--------|---------|
| Stores | Multiple values | Characters |
| Mutable | Yes | No (Immutable) |
| Indexing | Yes | Yes |
| Length | .Length | .Length |
| Type | Data Structure | Reference Type |

---

# Time Complexity Every Developer Should Know

| Operation | Complexity |
|------------|------------|
| Access Array Element | O(1) |
| Update Array Element | O(1) |
| Search Array | O(n) |
| Traverse Array | O(n) |
| String Length | O(1) |
| String Comparison | O(n) |

---

# Interview Questions

1. Why do arrays start from index 0?
2. What is the difference between Array and List?
3. What does .Length return?
4. Why are strings immutable in C#?
5. Difference between == and Equals()?
6. How does string interpolation work?

---

# Best Practices

✅ Use meaningful names.

```csharp
int[] studentMarks;
```

Instead of:

```csharp
int[] a;
```

✅ Use foreach for reading.

✅ Validate indexes before access.

✅ Prefer string interpolation.

```csharp
$"Hello {name}"
```

✅ Understand immutability before working with strings.

---

# Practice Exercises

## Exercise 1

Create an array of 5 numbers and print them.

## Exercise 2

Find the largest number in an array.

## Exercise 3

Find the sum of all elements.

## Exercise 4

Print each character of a string.

## Exercise 5

Count vowels in a string.

## Exercise 6

Reverse a string.

---

# What to Learn Next

After mastering Arrays and Strings:

1. Loops (for, while, foreach)
2. Methods
3. Lists
4. Dictionaries
5. Classes and Objects
6. Exception Handling
7. File Handling
8. LINQ
9. Data Structures
10. Algorithms

Arrays + Strings + Loops form the foundation of nearly every programming problem.

Happy Coding!

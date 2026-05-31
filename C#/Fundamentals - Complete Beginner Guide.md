# C# Fundamentals - Complete Beginner Guide

## Topics Covered

1. If, Else If, Else
2. Switch Case
3. Arrays
4. Strings
5. For Loops
6. While Loops
7. Functions
8. Pass By Value vs Pass By Reference

---

# 1. If, Else If, Else

## What is a Conditional Statement?

A conditional statement allows a program to make decisions.

Real-life example:

```text
If it is raining:
    Take an umbrella
Else:
    Go outside normally
```

### Syntax

```csharp
if (condition)
{
    // code
}
else if (condition)
{
    // code
}
else
{
    // code
}
```

### Example

```csharp
int age = 20;

if (age >= 18)
{
    Console.WriteLine("Adult");
}
else
{
    Console.WriteLine("Minor");
}
```

### Multiple Conditions

```csharp
int marks = 85;

if (marks >= 90)
{
    Console.WriteLine("Grade A");
}
else if (marks >= 75)
{
    Console.WriteLine("Grade B");
}
else if (marks >= 50)
{
    Console.WriteLine("Grade C");
}
else
{
    Console.WriteLine("Fail");
}
```

---

# 2. Switch Case

Used when checking many fixed values.

### Syntax

```csharp
switch(value)
{
    case value1:
        break;

    case value2:
        break;

    default:
        break;
}
```

### Example

```csharp
int day = 3;

switch(day)
{
    case 1:
        Console.WriteLine("Monday");
        break;

    case 2:
        Console.WriteLine("Tuesday");
        break;

    case 3:
        Console.WriteLine("Wednesday");
        break;

    default:
        Console.WriteLine("Invalid Day");
        break;
}
```

## When to Use Switch?

Use switch when:

- Comparing one variable
- Multiple fixed values
- Cleaner than many else-if statements

---

# 3. Arrays

## What is an Array?

An array stores multiple values of the same type.

Without arrays:

```csharp
int mark1 = 80;
int mark2 = 90;
int mark3 = 70;
```

With arrays:

```csharp
int[] marks = {80,90,70};
```

### Array Visualization

```text
Index:  0   1   2
Value: 80  90  70
```

### Access Elements

```csharp
Console.WriteLine(marks[0]);
```

Output:

```text
80
```

### Length

```csharp
Console.WriteLine(marks.Length);
```

### Important Concepts

- Fixed size
- Same datatype
- Zero-based indexing
- Fast access O(1)

---

# 4. Strings

## What is a String?

A string is a sequence of characters.

```csharp
string name = "John";
```

Visualization:

```text
J o h n
0 1 2 3
```

### Access Characters

```csharp
Console.WriteLine(name[0]);
```

Output:

```text
J
```

### Length

```csharp
Console.WriteLine(name.Length);
```

### String Concatenation

```csharp
string first = "John";
string last = "Doe";

string full = first + " " + last;
```

### String Interpolation

```csharp
string full = $"{first} {last}";
```

### Useful Methods

```csharp
name.ToUpper();
name.ToLower();
name.Contains("oh");
name.Replace("John", "Jack");
```

### Important

Strings are immutable.

When modified, a new string is created.

---

# 5. For Loops

## What is a Loop?

Loops repeat code.

Without loop:

```csharp
Console.WriteLine(1);
Console.WriteLine(2);
Console.WriteLine(3);
```

With loop:

```csharp
for(int i = 1; i <= 3; i++)
{
    Console.WriteLine(i);
}
```

### Structure

```csharp
for(initialization; condition; update)
{
    // code
}
```

### Example

```csharp
for(int i = 1; i <= 10; i++)
{
    Console.WriteLine(i);
}
```

### Traversing Arrays

```csharp
int[] numbers = {10,20,30};

for(int i = 0; i < numbers.Length; i++)
{
    Console.WriteLine(numbers[i]);
}
```

---

# 6. While Loops

A while loop runs as long as a condition is true.

### Syntax

```csharp
while(condition)
{
    // code
}
```

### Example

```csharp
int i = 1;

while(i <= 5)
{
    Console.WriteLine(i);
    i++;
}
```

### Difference

For Loop:
- Known number of iterations

While Loop:
- Unknown number of iterations

Example:

```csharp
while(password != "admin")
{
    // keep asking
}
```

---

# 7. Functions

## What is a Function?

A function is a reusable block of code.

### Without Functions

```csharp
Console.WriteLine("Hello");
Console.WriteLine("Hello");
Console.WriteLine("Hello");
```

### With Functions

```csharp
static void SayHello()
{
    Console.WriteLine("Hello");
}
```

Usage:

```csharp
SayHello();
```

### Function with Parameters

```csharp
static void Greet(string name)
{
    Console.WriteLine($"Hello {name}");
}
```

Call:

```csharp
Greet("John");
```

### Function Returning Value

```csharp
static int Add(int a, int b)
{
    return a + b;
}
```

Call:

```csharp
int result = Add(10,20);
```

---

# 8. Pass By Value vs Pass By Reference

One of the most important C# concepts.

## Pass By Value

A copy is sent.

Original variable remains unchanged.

### Example

```csharp
static void ChangeValue(int number)
{
    number = 100;
}

int x = 10;

ChangeValue(x);

Console.WriteLine(x);
```

Output:

```text
10
```

Why?

Because only a copy was modified.

---

## Pass By Reference

Original variable is modified.

### Example

```csharp
static void ChangeValue(ref int number)
{
    number = 100;
}

int x = 10;

ChangeValue(ref x);

Console.WriteLine(x);
```

Output:

```text
100
```

Because the actual variable was passed.

---

# Comparison

| Feature | Pass By Value | Pass By Reference |
|----------|--------------|-------------------|
| Copy Sent | Yes | No |
| Original Changes | No | Yes |
| Memory Usage | More | Less |
| Uses ref Keyword | No | Yes |

---

# Common Interview Questions

## If Else

1. Difference between if and switch?
2. What happens if multiple conditions are true?

## Arrays

1. Why arrays start at index 0?
2. Difference between Array and List?

## Strings

1. Why are strings immutable?
2. Difference between == and Equals()?

## Loops

1. Difference between for and while?
2. Infinite loop examples?

## Functions

1. Why use functions?
2. What is recursion?

## Pass By Reference

1. Difference between value and reference?
2. What does ref keyword do?

---

# Best Practices

✅ Use meaningful variable names

```csharp
int studentCount;
```

❌ Avoid

```csharp
int x;
```

✅ Use functions for reusable code

✅ Validate user input

✅ Prefer string interpolation

```csharp
$"Hello {name}"
```

✅ Keep functions small

✅ Avoid duplicate code

---

# Learning Path After This

1. Collections (List, Dictionary)
2. Object-Oriented Programming
3. Exception Handling
4. File Handling
5. LINQ
6. Generics
7. Async/Await
8. Data Structures
9. Algorithms
10. ASP.NET Core

Master these fundamentals before moving to advanced topics.

They form the foundation of professional C# development.

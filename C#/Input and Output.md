# C# Input and Output for Complete Beginners

## Introduction

A program is like a conversation:

- **Input** = Information the user gives to the program.
- **Output** = Information the program shows to the user.

In C#, the most common way to do this is:

- `Console.WriteLine()` → Output
- `Console.ReadLine()` → Input

---

# 1. Output in C#

```csharp
Console.WriteLine("Hello, World!");
```

### Explanation

- `Console` is a built-in class that works with the console.
- `WriteLine()` displays text and then moves to the next line.
- `"Hello, World!"` is the text to display.

### Output

```text
Hello, World!
```

---

# 2. Taking Input in C#

```csharp
Console.Write("Enter your name: ");
string name = Console.ReadLine();

Console.WriteLine("Hello " + name);
```

### Explanation

```csharp
Console.Write("Enter your name: ");
```

Displays text without moving to the next line.

```csharp
string name = Console.ReadLine();
```

- Waits for the user to type something.
- Stores the value in the variable `name`.
- `string` means text data.

```csharp
Console.WriteLine("Hello " + name);
```

Combines `"Hello "` with the user's name.

### Example Run

```text
Enter your name: John
Hello John
```

---

# 3. Taking Number Input

`ReadLine()` always returns text, so numbers must be converted.

```csharp
Console.Write("Enter your age: ");
int age = int.Parse(Console.ReadLine());

Console.WriteLine("Your age is " + age);
```

### Explanation

```csharp
int age;
```

- `int` means integer (whole number).

```csharp
int.Parse(...)
```

- Converts text into an integer.

### Example Run

```text
Enter your age: 20
Your age is 20
```

---

# 4. Taking Two Numbers and Adding Them

```csharp
Console.Write("Enter first number: ");
int num1 = int.Parse(Console.ReadLine());

Console.Write("Enter second number: ");
int num2 = int.Parse(Console.ReadLine());

int sum = num1 + num2;

Console.WriteLine("Sum = " + sum);
```

### Example Run

```text
Enter first number: 5
Enter second number: 7
Sum = 12
```

---

# 5. String Interpolation (Recommended)

Instead of:

```csharp
Console.WriteLine("Hello " + name);
```

Use:

```csharp
Console.WriteLine($"Hello {name}");
```

The `$` symbol allows variables to be inserted directly into a string.

Example:

```csharp
int age = 20;
Console.WriteLine($"I am {age} years old.");
```

### Output

```text
I am 20 years old.
```

---

# 6. Complete Beginner Program

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.Write("Enter your name: ");
        string name = Console.ReadLine();

        Console.Write("Enter your age: ");
        int age = int.Parse(Console.ReadLine());

        Console.WriteLine($"Hello {name}");
        Console.WriteLine($"You are {age} years old.");
    }
}
```

### Example Run

```text
Enter your name: Alice
Enter your age: 18
Hello Alice
You are 18 years old.
```

---

# Quick Summary

| Task | Code |
|------|------|
| Print text | `Console.WriteLine("Hello");` |
| Print without new line | `Console.Write("Hello");` |
| Read text | `string name = Console.ReadLine();` |
| Read integer | `int age = int.Parse(Console.ReadLine());` |
| Print variable | `Console.WriteLine(age);` |
| Print with text | `Console.WriteLine($"Age = {age}");` |

---

# Practice Exercise

Write a program that asks for:

1. User's name
2. Favorite color

Then display:

```text
Hello John!
Your favorite color is Blue.
```

Happy Coding!

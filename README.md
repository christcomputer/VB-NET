# VB-NET

### 1.  In VB.NET , Printing "HELLO WORLD!" through a console app

```vb
Module Module1
    Sub Main()
        Console.WriteLine("HELLO WORLD!")
        Console.ReadLine() ' This keeps the console window open until you press Enter
    End Sub
End Module
```

### 2. Calculate the factorial of a number using VB.NET

```vb
Module Module1
    Sub Main()
        Dim number As Integer
        Dim factorial As Long = 1

        Console.Write("Enter a number: ")
        number = Convert.ToInt32(Console.ReadLine())

        For i As Integer = 1 To number
            factorial *= i
        Next

        Console.WriteLine("The factorial of " & number & " is " & factorial)
        Console.ReadLine()
    End Sub
End Module
```

### 3. Find the greatest of three numbers using VB.NET

```vb
Module Module1
    Sub Main()
        Dim num1 As Integer
        Dim num2 As Integer
        Dim num3 As Integer

        Console.Write("Enter the first number: ")
        num1 = Convert.ToInt32(Console.ReadLine())

        Console.Write("Enter the second number: ")
        num2 = Convert.ToInt32(Console.ReadLine())

        Console.Write("Enter the third number: ")
        num3 = Convert.ToInt32(Console.ReadLine())

        If num1 >= num2 AndAlso num1 >= num3 Then
            Console.WriteLine("The greatest number is " & num1)
        ElseIf num2 >= num1 AndAlso num2 >= num3 Then
            Console.WriteLine("The greatest number is " & num2)
        Else
            Console.WriteLine("The greatest number is " & num3)
        End If

        Console.ReadLine()
    End Sub
End Module
```

### 4. Swap two numbers in VB.NET

```vb
Module Module1
    Sub Main()
        Dim num1 As Integer
        Dim num2 As Integer
        Dim temp As Integer

        Console.Write("Enter the first number: ")
        num1 = Convert.ToInt32(Console.ReadLine())

        Console.Write("Enter the second number: ")
        num2 = Convert.ToInt32(Console.ReadLine())

        ' Swapping the numbers using a temporary variable
        temp = num1
        num1 = num2
        num2 = temp

        Console.WriteLine("After swapping:")
        Console.WriteLine("First number: " & num1)
        Console.WriteLine("Second number: " & num2)

        Console.ReadLine() ' This keeps the console window open until you press Enter
    End Sub
End Module
```

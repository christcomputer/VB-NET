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
### 5. calculate the grade using a form app

```vb
Public Class Form1
    Private Sub Button1_Click(sender As Object, e As EventArgs) Handles Button1.Click
        Dim marks As Integer
        Dim grade As String

        ' Get the marks from the TextBox1
        Integer.TryParse(TextBox1.Text, marks)

        ' Calculate grade based on the marks
        If marks >= 90 Then
            grade = "A"
        ElseIf marks >= 80 Then
            grade = "B"
        ElseIf marks >= 70 Then
            grade = "C"
        ElseIf marks >= 60 Then
            grade = "D"
        Else
            grade = "F"
        End If

        ' Display the grade in TextBox2
        TextBox2.Text = grade
    End Sub
End Class

```

```
[Enter Marks:] [TextBox1]
[Calculate Grade] [Button1]
[Grade:] [TextBox2]
```
### 6. Basic calculator using a Windows Forms application in VB.NET

```vb
Public Class Form1
    Dim firstNumber As Double
    Dim secondNumber As Double
    Dim operation As String

    Private Sub ButtonNumber_Click(sender As Object, e As EventArgs) Handles Button0.Click, Button1.Click, Button2.Click, Button3.Click, Button4.Click, Button5.Click, Button6.Click, Button7.Click, Button8.Click, Button9.Click
        TextBox1.Text = TextBox1.Text & CType(sender, Button).Text
    End Sub

    Private Sub ButtonAdd_Click(sender As Object, e As EventArgs) Handles ButtonAdd.Click
        firstNumber = Convert.ToDouble(TextBox1.Text)
        TextBox1.Text = ""
        operation = "+"
    End Sub

    Private Sub ButtonSubtract_Click(sender As Object, e As EventArgs) Handles ButtonSubtract.Click
        firstNumber = Convert.ToDouble(TextBox1.Text)
        TextBox1.Text = ""
        operation = "-"
    End Sub

    Private Sub ButtonMultiply_Click(sender As Object, e As EventArgs) Handles ButtonMultiply.Click
        firstNumber = Convert.ToDouble(TextBox1.Text)
        TextBox1.Text = ""
        operation = "*"
    End Sub

    Private Sub ButtonDivide_Click(sender As Object, e As EventArgs) Handles ButtonDivide.Click
        firstNumber = Convert.ToDouble(TextBox1.Text)
        TextBox1.Text = ""
        operation = "/"
    End Sub

    Private Sub ButtonEqual_Click(sender As Object, e As EventArgs) Handles ButtonEqual.Click
        secondNumber = Convert.ToDouble(TextBox1.Text)
        Select Case operation
            Case "+"
                TextBox1.Text = (firstNumber + secondNumber).ToString()
            Case "-"
                TextBox1.Text = (firstNumber - secondNumber).ToString()
            Case "*"
                TextBox1.Text = (firstNumber * secondNumber).ToString()
            Case "/"
                TextBox1.Text = (firstNumber / secondNumber).ToString()
        End Select
    End Sub

    Private Sub ButtonClear_Click(sender As Object, e As EventArgs) Handles ButtonClear.Click
        TextBox1.Text = ""
        firstNumber = 0
        secondNumber = 0
    End Sub
End Class
```
```
[TextBox]
[Button1][Button2][Button3][ButtonAdd]
[Button4][Button5][Button6][ButtonSubtract]
[Button7][Button8][Button9][ButtonMultiply]
[ButtonClear][Button0][ButtonEqual][ButtonDivide]
```
### 7. Write a C# program that checks if a given string is a palindrome
```C#
using System;

namespace PalindromeChecker
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Enter a string:");
            string input = Console.ReadLine();

            string reversed = ReverseString(input);
            if (input.Replace(" ", "").ToLower() == reversed.Replace(" ", "").ToLower())
            {
                Console.WriteLine("The string is a palindrome.");
            }
            else
            {
                Console.WriteLine("The string is not a palindrome.");
            }
        }

        static string ReverseString(string s)
        {
            char[] charArray = s.ToCharArray();
            Array.Reverse(charArray);
            return new string(charArray);
        }
    }
}
```

### 8. Write a C# program that calculates the average of a list of numbers input by the user.

```C#
using System;
using System.Linq;

namespace AverageCalculator
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Enter numbers separated by spaces:");
            string input = Console.ReadLine();
            double[] numbers = input.Split(' ').Select(Double.Parse).ToArray();
            double average = numbers.Average();
            Console.WriteLine("Average: " + average);
        }
    }
}
```

### 9. Write a C# program that counts the number of vowels in a string input by the user.

```C#
using System;

namespace VowelCounter
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Enter a string:");
            string input = Console.ReadLine().ToLower();
            int vowelCount = 0;

            foreach (char c in input)
            {
                if ("aeiou".Contains(c))
                {
                    vowelCount++;
                }
            }

            Console.WriteLine("Number of vowels: " + vowelCount);
        }
    }
}
```

### 10. Print Hello world using button Click using C# Form app

```C#
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace WindowsFormsApp1
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void btnClickThis_Click(object sender, EventArgs e)
        {
            lblHelloWorld.Text = "Hello World!";
        }
        
    }
}

```

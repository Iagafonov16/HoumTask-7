﻿# HoumTask-7
// Задача 1: Задайте значения M и N. Напишите программу, которая выведет все натуральные числа в промежутке от M до N. Использовать рекурсию, не использовать циклы.
Console.Write("Введите значение M: "); 
int M = int.Parse(Console.ReadLine()); 
 
Console.Write("Введите значение N: "); 
int N = int.Parse(Console.ReadLine()); 

void PrintNaturalNumbers(int current, int N) 
{ 
  if (current <= N) 
    { 
      Console.Write(current + " "); 
      PrintNaturalNumbers(current + 1, N); 
    } 
} 
PrintNaturalNumbers(M, N); 


//Задача 2: Напишите программу вычисления функции Аккермана с помощью рекурсии. Даны два неотрицательных числа m и n.
Console.Write("Введите неотрицательное число m: "); 
int m = int.Parse(Console.ReadLine()); 
 
Console.Write("Введите неотрицательное число n: "); 
int n = int.Parse(Console.ReadLine()); 
 
int result = AckermannFunction(m, n); 
Console.WriteLine($"Значение функции Аккермана для ({m}, {n}) равно: {result}"); 
 
 
int AckermannFunction(int m, int n) 
{ 
  if (m == 0) 
  return n + 1; 
  else if (n == 0) 
    return AckermannFunction(m - 1, 1); 
  else 
    return AckermannFunction(m - 1, AckermannFunction(m, n - 1)); 
} 

// Задача 3: Задайте произвольный массив. Выведете его элементы, начиная с конца. Использовать рекурсию, не использовать циклы.
int[] myArray = { 3, 9, 18, 32, 64 }; 
 
Console.WriteLine("Элементы массива, начиная с конца:"); 
PrintArrayReverse(myArray, myArray.Length - 1); 
 
 
static void PrintArrayReverse(int[] arr, int index) 
{ 
  if (index >= 0) 
    { 
      Console.Write(arr[index] + " "); 
      PrintArrayReverse(arr, index - 1); 
    } 
} 

# dz5
// dotnet new console 
//dotnet run
// Zadanie 1:  Задайте массив заполненный случайными положительными трёхзначными числами (длина массива 5 элементов). Напишите программу, которая покажет количество чётных чисел в массиве.
// Code 
using System;

class Program {
    static void Main(string[] args) {
        Random random = new Random();
        int[] array = new int[5];
        // Заполняем массив случайными трехзначными числами
        for (int i = 0; i < array.Length; i++) {
            array[i] = random.Next(100, 1000);
        }
        // Считаем количество четных чисел в массиве
        int count = 0;
        for (int i = 0; i < array.Length; i++) {
            if (array[i] % 2 == 0) {
                count++;
            }
        }
        Console.WriteLine("Массив: " + string.Join(", ", array));
        Console.WriteLine("Количество четных чисел: " + count);
        Console.ReadKey();
    }
}
//END
// Zadanie 3:Задайте массив вещественных чисел от -100 до 100 (длина массива 5 элементов). Найдите разницу между максимальным и минимальным элементов массива.
//Code
internal class Program
{
    private static void Main(string[] args)
    {
        double[] numbers = { -50.2, 10.4, -30.8, 40.5, 20.7 };
        double min = numbers[0];
        double max = numbers[0];
        foreach (double number in numbers)
        {
            if (number < min)
            {
                min = number;
            }
                 else if (number > max)
            {
                max = number;
            }
        }
       Console.WriteLine("-50.2, 10.4, -30.8, 40.5, 20.7");
        Console.WriteLine("Минимальный элемент: "+min);
        Console.WriteLine("Максимальный элемент: "+max);
        double difference = Math.Abs(max - min);
        Console.WriteLine("Ответ: " + difference);
    }
}
//END
//DOP. ZADACHI
//Zadanie 4: Задайте массив из 8 случайных чисел из промежутка [-9, 9]. Напишите программу получает на вход число и определяет, присутствует ли заданное число в массиве.
//Code
int[] array = new int[8];
Random rand = new Random();

for (int i = 0; i < array.Length; i++)
{
    array[i] = rand.Next(-9, 10); // генерируем число от -9 до 9
}
Console.WriteLine(string.Join(", ", array));
Console.WriteLine("Введите число:");
int number = int.Parse(Console.ReadLine()); // считываем число с консоли

bool isPresent = false; // флаг, показывающий, найдено ли число в массиве

foreach (int element in array)
{
    if (element == number)
    {
        isPresent = true;
        break;
    }
}

if (isPresent)
{
    Console.WriteLine($"Число {number} присутствует в массиве.");
}
else
{
    Console.WriteLine($"Число {number} отсутствует в массиве.");
}
//END
//Zadanie 5: Задайте массив из 10 случайных чисел из промежутка [-100, 100]. Найдите количество элементов массива, значения которых лежат в отрезке [10,99].
//Code
int[] array = new int[10];
Random rand = new Random();
int count = 0; // счетчик количества элементов, значения которых лежат в отрезке [10, 99]

for (int i = 0; i < array.Length; i++)
{
    array[i] = rand.Next(-100, 101); // генерируем число от -100 до 100
    
    if (array[i] >= 10 && array[i] <= 99) // проверяем, что число находится в отрезке [10, 99]
    {
        count++; // увеличиваем счетчик на 1
    }
}
Console.WriteLine(string.Join(", ", array));
Console.WriteLine($"Количество элементов, значения которых лежат в отрезке [10, 99]: {count}");
//END

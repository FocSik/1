# Первая задача
---
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    namespace CSHARP.TEST
    {
    class square
    {
    private
    double side;
    public square(double n)
    {
    if (n <= 0)
    {
    error();
    }
    this.side = n;
    }
    public double calcSquare()
    {
    return Math.Pow(side,2);
    }
    public double calcPreim()
    {
    return side * 4;
    }
    public double calcLenth()
    {
    return Math.PI * side;
    }
    public double calcSqCircle()
    {
    return Math.PI * Math.Pow(side / 2, 2);
    }
    public void message()
    {
    Console.WriteLine(" площадь квадрата: " + calcSquare() +
    "\n периметр квадрата: " + calcPreim() +
    "\n длина вписаной окружности: " + calcLenth()+
    "\n Площадь вписаной окружности: " + calcSqCircle());
    }
    private void error()
    {
    Console.WriteLine("Ошибка, введено некорректное значение");
    Environment.Exit(0);
    }
    static void Main(string[] args)
    {
    Console.WriteLine("Введите длинну стороны квадрата:  ");
    double k = double.Parse(Console.ReadLine());
    square sq = new square(k);
    sq.message();
    }
    }
    }

1Lab 

   1.Написать программу, которая выводит текущее время и дату.  
   2.Создать переменные различных типов (int, float64, string, bool) и вывести их на экран.  
   3.Использовать краткую форму объявления переменных для создания и вывода переменных.  
   4.Написать программу для выполнения арифметических операций с двумя целыми числами и выводом результатов.  
   5.Реализовать функцию для вычисления суммы и разности двух чисел с плавающей запятой.  
   6.Написать программу, которая вычисляет среднее значение трех чисел.  



```
package main

import (
	"fmt"
	"time"
)

// Функция для вычисления суммы и разности двух чисел с плавающей запятой
func sumAndDifference(a, b float64) (float64, float64) {
	return a + b, a - b
}

func main() {
// 1. Вывод текущего времени и даты
	currentTime := time.Now()
	fmt.Println("1. Текущее время и дата:", currentTime.Format("2006-01-02 15:04:05"))

// 2. Создание переменных различных типов
	var integerVar int = 42
	var floatVar float64 = 3.1415
	var stringVar string = "Hello, Go!"
	var boolVar bool = true
	fmt.Printf("2. Переменные: int = %d, float64 = %.4f, string = %s, bool = %t\n", integerVar, floatVar, stringVar, boolVar)

// 3. Краткая форма объявления переменных
	shortInt := 100
	shortString := "Short Declaration"
	fmt.Println("3. Краткая форма:", shortInt, ",", shortString)

// 4. Арифметические операции с двумя целыми числами
	num1, num2 := 20, 5
	fmt.Printf("4. Арифметика (%d и %d): Сумма = %d, Разность = %d, Произведение = %d, Частное = %d\n",
		num1, num2, num1+num2, num1-num2, num1*num2, num1/num2)

// 5. Функция суммы и разности
	f1, f2 := 10.5, 4.2
	sum, diff := sumAndDifference(f1, f2)
	fmt.Printf("5. float64 (%v и %v): Сумма = %.2f, Разность = %.2f\n", f1, f2, sum, diff)

// 6. Вычисление среднего значения трех чисел
	val1, val2, val3 := 15.0, 25.0, 35.0
	average := (val1 + val2 + val3) / 3
	fmt.Printf("6. Среднее значение (15, 25, 35) = %.2f\n", average)
}
```
Запусить код в любом удобном текстовом редакторе, ide или в браузере.  

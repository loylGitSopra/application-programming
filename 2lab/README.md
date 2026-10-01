2Lab

1.Написать программу, которая определяет, является ли введенное пользователем число четным или нечетным.  
2.Реализовать функцию, которая принимает число и возвращает "Positive", "Negative" или "Zero".  
3.Написать программу, которая выводит все числа от 1 до 10 с помощью цикла for.  
4.Написать функцию, которая принимает строку и возвращает ее длину.  
5.Создать структуру Rectangle и реализовать метод для вычисления площади прямоугольника.  
6.Написать функцию, которая принимает два целых числа и возвращает их среднее значение.  


```
package main

import (
	"fmt"
	"unicode/utf8"
)

// Функция для определения знака числа
func checkSign(number int) string {
	if number > 0 {
		return "Positive"
	} else if number < 0 {
		return "Negative"
	}
	return "Zero"
}

// Функция для возврата длины строки
func getStringLength(text string) int {
	// Используем RuneCountInString для корректного подсчета символов (включая кириллицу)
	return utf8.RuneCountInString(text)
}

// Структура Rectangle
type Rectangle struct {
	width  float64
	height float64
}

// Метод для вычисления площади прямоугольника
func (r Rectangle) Area() float64 {
	return r.width * r.height
}

// Функция для вычисления среднего значения двух целых чисел
func averageOfTwo(a, b int) float64 {
	return float64(a+b) / 2.0
}

func main() {
	// 1. Определение четности числа
	var inputNumber int
	fmt.Print("1. Введите целое число: ")
	// Ввод с клавиатуры. Для тестирования без остановки программы можно закомментировать Scan.
	fmt.Scan(&inputNumber)
	if inputNumber%2 == 0 {
		fmt.Printf("Число %d является четным.\n", inputNumber)
	} else {
		fmt.Printf("Число %d является нечетным.\n", inputNumber)
	}

	// 2. Функция "Positive", "Negative" или "Zero"
	testValue := -8
	fmt.Printf("2. Знак числа %d: %s\n", testValue, checkSign(testValue))

	// 3. Вывод чисел от 1 до 10 с помощью цикла for
	fmt.Print("3. Числа от 1 до 10: ")
	for i := 1; i <= 10; i++ {
		fmt.Printf("%d ", i)
	}
	fmt.Println()

	// 4. Функция возврата длины строки
	sampleString := "Golang Development"
	fmt.Printf("4. Длина строки '%s': %d символов\n", sampleString, getStringLength(sampleString))

	// 5. Структура Rectangle и площадь
	rect := Rectangle{width: 7.5, height: 4.0}
	fmt.Printf("5. Площадь прямоугольника (%.1fx%.1f): %.2f\n", rect.width, rect.height, rect.Area())

	// 6. Среднее значение двух целых чисел
	numA, numB := 10, 21
	fmt.Printf("6. Среднее значение чисел %d и %d: %.2f\n", numA, numB, averageOfTwo(numA, numB))
}
```

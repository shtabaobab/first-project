# Отработка навыков использования markdown
---

Текст в маркдауне можно **выделять жирным** или *курсивом*


Конечно, самое интересное, отработать печать кода

##Java

```java

import java.util.Scanner;

public class Shopping {

    public static void main(String[] args) {

        System.out.println("Вас приветствует список покупок!");

        String[] shoppingList = new String[8];  // Объявляем массив shoppingList через длину
        int productCount = 0; // переменная для подсчёта добавленных товаров

        Scanner scanner = new Scanner(System.in);


        while (true) { // консольный интерфейс
            System.out.println("Выберите одну из команд:");
            System.out.println("1. Добавить товар в список");
            System.out.println("2. Показать список");
            System.out.println("3. Очистить список");
            System.out.println("4. Завершить работу");

            int actionNumber = scanner.nextInt(); // пользователь выбирает команду

            if (actionNumber == 1) { // команда № 1
                System.out.println("Введите название товара:");


                scanner.nextLine(); // Спасибо! Ты лучший, хорошая подсказка
                String product = scanner.nextLine();

                if (productCount < shoppingList.length) { // проверяем, есть ли еще место в массиве
                    shoppingList[productCount] = product; // добавляем очередной товар в список товаров
                    productCount++;
                    System.out.println("Товар " + product + " добавлен в список под номером " + productCount + ".");

                } else if () {
                    
                } else {
                    System.out.println("Извините, список покупок уже полон.");}

                } else if (actionNumber == 2) { // команда № 2
                    System.out.println("Список покупок:"); // выводим список покупок
                    for (int i = 0; i < productCount; i++) {
                        System.out.println((i + 1)+ ". " + shoppingList[i]);
                    }

                } else if (actionNumber == 3) { // команда № 3
                    productCount = 0; // Очищаем список покупок
                    System.out.println("Список покупок очищен.");

                } else if (actionNumber == 4) { // команда № 4
                    System.out.println("Спасибо за использование программы!");
                    break;

                } else { // любая другая команда
                    System.out.println("Неизвестная команда!");
                }
            }
        }
```

А вот так оформляеются [ссылки](https://www.yandex.ru "Я Yandex!")
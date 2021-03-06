# Отчёт о тестировании приложения "Money Transfer"

## Краткое описание

После совершения операции пополнения счета VIP-клиента произошло некорректное отображение остатка, приложение вывело отрицательный результат. 
Проверка кода показала, что переменной total_balance присвоен неверный тип данных. 
Итоговое числовое значение переменной total_balance превысило допустимое значение для типа данных int.

## Описание тестов

Проведено позитивное функциональное тестирование. Протестировано приложение вывода баланса счета VIP-клиента после совершения операции перевода средств (пополнение счета). Тестирование проводилось методом белого ящика с запуском кода на исполнение.

## Результаты

1. При присвоении переменной total_balance значения, соответствующего типу данных int, приложение возвращает корректный результат. При присвоении переменной total_balance значения, не соответствующего типу данных int - возвращается отрицательный баланс после сложения.
![Отрицательный баланс после сложения](https://user-images.githubusercontent.com/71065934/104580574-7f799d80-566e-11eb-96a1-70f54d7f37df.png)

2. [Баг-репорт](https://github.com/asatoroff/jdz1/issues/1)

## Общие рекомендации
*Задать переменным vip_cont, transfer, total_balance тип данных long*

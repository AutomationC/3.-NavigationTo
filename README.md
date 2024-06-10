# 2.-NavigationTo
Задания по навигации Selenium

## Задача 1 Определить уникальный элемент на каждой из трех страниц:
    https://ib.psbank.ru/
    https://ib.psbank.ru/store/products/consumer-loan
    https://ib.psbank.ru/store/products/investmentsbrokerage
  
  Формат ответа
  
  Страница Х, тип локатора Х, значение локатора Х
  
## Задача 2 Реализовать метод для ожидание загрузки страниц из предыдущей задачи
 
  Формат ответа 
  
  Тест реализовывающий указанные шаги
  
  |Шаги                                                                     | Результат                                              |
  |-------------------------------------------------------------------------|--------------------------------------------------------|
  | Открыть страницу https://ib.psbank.ru/ и проверить отображение текста   | Присутствует заголовок с текстом 'Финансовые продукты' |
    
## Задача 3 Проверить переход по ссылке внутри элемента

  Формат ответа 
  
  Тест реализовывающий указанные шаги
  
   |Шаги                                        | Результат|
   |---------------------------------------------|--------------------------------------------------------|
   |Jткрыть страницу https://ib.psbank.ru/      | Страница загрузилась|
   |В меню нажать на элемент 'инвестиции'       | Раскрылся выпадающий список который содержит элемент 'Брокерский договор' со ссылкой '/store/products/investmentsbrokerage'|
   |Нажать на элемент 'Брокерский договор'      | Произошел переход по указанной ссылке, на страницу Инвестиции |
   
## Задача 4 Работа с различными вкладками браузера. Реализовать механизм переключение между активными вкладками |

  Формат ответа 
  
  Тест реализовывающий указанные шаги
  
   |Шаги                                        | Результат|
   |---------------------------------------------|--------------------------------------------------------|
   |Открыть страницу https://ib.psbank.ru/store/products/consumer-loan                             | Страница кредита загрузилась|
   |Открыть страницу в новой вкладке https://ib.psbank.ru/store/products/investmentsbrokerage   | Страница инвестиций загрузилась|
   |Проверить отображение информации о номере лицензии и дате на странице инвестиций            | Данные отображаются корректно и соответствуют маске 'Генеральная лицензия на осуществление банковских операций № {номер} от {dd MMM yyyy}' или 'Генеральная лицензия на осуществление банковских операций № \d\d\d\d от \d\d .* \d\d\d\d'|
   |Закрыть страницу инвестиций                                                                 | Активной вкладкой стала страница кредита|
   |Проверить отображение информации о номере лицензии и дате на странице инвестиций            | Данные соответствуют результату шага 3|
   
## Задача 5 Работа с различными вкладками на странице. Реализовать возможность работы при различном состоянии страниц

  Формат ответа 
  
  Тест реализовывающий указанные шаги
  
   |Шаги                                        | Результат|
   |---------------------------------------------|--------------------------------------------------------|
   |Открыть страницу получения ипотеки                                                                               | Страница ипотеки загрузилась|
   |Переключиться на вкладку 'Приобретение'                                                                          | Загрузилась информация о программах элемент 'Приобретение' окрасился в черный цвет (dark)|
   |Переключиться на программу 'Семейная ипотека'                                                                    | В блоке расчета ежемесячного платежа загрузились данные по программе 'Семейная ипотека'|
   |В блоке расчета ежемесячного платежа проверить значение ставки по программе 'Семейная ипотека'                   | Значение ставки составляет отобразилось корректно и соответствуют маске '\d*%'|
   |Переключиться на вкладку рефинансирование                                                                        | Загрузилась информация о программах элемент 'Рефинансирование' окрасился в черный цвет (dark)|
   |Переключиться на программу 'Рефинансирование. Семейная ипотека'                                                  | В блоке расчета ежемесячного платежа загрузились данные по программе 'Рефинансирование. Семейная ипотека' |
   |В блоке расчета ежемесячного платежа проверить значение ставки по программе 'Рефинансирование. Семейная ипотека' | Значение ставки идентично результату шага 4|

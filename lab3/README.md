# Лабораторная работа №3 «Регулярные выражения»
Для определения варианта используйте свой табельный номер, которые можно найти в ИСУ. (_Пример номера:_ 125598)
## Задание на 60 баллов (Смайлики)
___Вариант №310___
1) Реализуйте программный продукт на языке Python, используя регулярные выражения по варианту, представленному в таблице.
2) Для своей программы придумайте минимум 5 тестов. Каждый тест является отдельной сущностью, передаваемой регулярному выражению для обработки. Для каждого теста необходимо самостоятельно (без использования регулярных выражений) найти правильный ответ. После чего сравнить ответ, выданный программой, и полученный самостоятельно.
3) Программа должна считать количество смайликов определённого вида (вид смайлика описан в таблице вариантов) в предложенном тексте. Все смайлики имеют такую структуру:
   
    [_глаза_][_нос_][_рот_].

    Вариантом является различные наборы глаз, носов и ртов.

| Номер в ИСУ % 5  | Глаза  | Номер в ИСУ % 4  | Нос  | Номер в ИСУ % 7  | Рот    |
|------------------|--------|------------------|------|------------------|--------|
| 0                | :      | 0                | -    | 0                | (      |
| 1                | ;      | 1                | <    | 1                | )      |
| 2                | X      | 2                | -{   | 2                | O      |
| 3                | 8      | 3                | <{   | 3                | &#124; |
| 4                | =      |                  |      | 4                | \      |
|                  |        |                  |      | 5                | /      |
|                  |        |                  |      | 6                | P      |

_Пример смайлика:_ 8<{P

4) \* нарисовав смайлик по вашему варианту при помощи средств языка программирования Python, можно заработать дополнительные баллы.
## Доп. задание №1 (+18 баллов)
___Вариант №5___
1) Реализуйте программный продукт на языке Python, используя регулярные выражения по варианту, представленному в таблице.
2) Для своей программы придумайте минимум 5 тестов. Каждый тест является отдельной сущностью, передаваемой регулярному выражению для обработки. Для каждого теста необходимо самостоятельно (без использования регулярных выражений) найти правильный ответ. После чего сравнить ответ, выданный программой, и полученный самостоятельно.
   
    Пример тестов приведён в таблице.

| Номер в ИСУ % 6 | Задание |
|---|---|
| 0 | Хайку – жанр традиционной японской лирической поэзии века, известный с XIV века. <br><br> Оригинальное японское хайку состоит из 17 слогов, составляющих один столбец иероглифов. Особыми разделительными словами – кирэдзи – текст хайку делится на части из 5, 7 и снова 5 слогов. При переводе хайку на западные языки традиционно вместо разделительного слова использую разрыв строки и, таким образом, хайку записываются как трёхстишия. <br><br> Перед вами трёхстишия, которые претендуют на то, чтобы быть хайку. В качестве разделителя строк используются символы «/». Если разделители делят текст на строки, в которых 5/7/5 слогов, то выведите «Хайку!». Если число строк не равно 3, то выведите строку «Не хайку. Должно быть 3 строки.». Иначе выведите строку вида «Не хайку.» <br><br> Для простоты будем считать, что слогов ровно столько же, сколько гласных, не задумываясь о тонкостях. <br><br> Пример: <br><table><tr><td>Ввод</td><td>Вывод</td></tr><tr><td>Вечер за окном. / Еще один день прожит. / Жизнь скоротечна...</td><td>Хайку!</td></tr><tr><td>Просто текст</td><td>Не хайку. Должно быть 3 строки.</td></tr><tr><td>Как вишня расцвела! / Она с коня согнала / И князя-гордеца.</td><td>Не хайку.</td></tr></table> |
| 1 | Довольно распространённая ошибка ошибка – это повтор слова. Вот в предыдущем предложении такая допущена. Необходимо исправить каждый такой повтор. <br><br> Повтор это – слово, один или несколько пробельных символов, и снова то же слово. <br><br> Пример: <br><table><tr><td>Ввод</td><td>Вывод</td></tr><tr><td>Довольно распространённая ошибка ошибка – это лишний повтор повтор слова слова. Смешно, не не правда ли? Не нужно портить хор хоровод.</td><td>Довольно распространённая ошибка – это лишний повтор слова. Смешно, не правда ли? Не нужно портить хор хоровод.</td></tr></table> |
| 2 | Дан текст. Необходимо найти в нём любой фрагмент, где сначала идёт слово «ВТ», затем не более 4 слов, и после этого идёт слово «ИТМО».<br><br>Для простоты будем считать словом любую последовательность букв, цифр и знаков «_» (то есть символов \w).<br><br>Пример:<br><table><tr><td>Ввод</td><td>Вывод</td></tr><tr><td>А ты знал, что ВТ – лучшая кафедра в ИТМО?</td><td>ВТ лучшая кафедра в ИТМО</td></tr></table> |
| 3 | Дан текст. Требуется найти в тексте все фамилии, отсортировав их по алфавиту.<br><br> Фамилией для простоты будем считать слово с заглавной буквой, после которого идут инициалы.<br><br>Пример:<br><table><tr><td>Ввод</td><td>Вывод</td></tr><tr><td>Студент Вася вспомнил, что на своей лекции Балакшин П.В. упоминал про старшекурсников, которые будут ему помогать: Анищенко А.А. и Машина Е.А.</td><td>Анищенко<br>Балакшин<br>Машина</td></tr></table>
| 4 | Анатолий выложил пост с расписанием доп. занятий по информатике, но везде перепутал время. Поэтому нужно заменить все вхождения времени на строку (TBD).<br><br> Время – это строка вида HH:MM:SS или HH:MM, в которой HH – число от 00 до 23, а MM и SS – число от 00 до 59.<br><br> Пример:<br><table><tr><td>Ввод</td><td>Вывод</td></tr><tr><td>Уважаемые студенты! В эту субботу в 15:00 планируется доп. занятие на 2 часа. То есть в 17:00:01 оно уже точно кончится.</td><td>Уважаемые студенты! В эту субботу в (TBD) планируется доп. занятие на 2 часа. То есть в (TBD) оно уже точно кончится.</td></tr></table>
| 5 | С помощью регулярного выражения найти в тексте все слова, в которых две гласные стоят подряд, а после этого слова идёт слово, в котором не больше 3 согласных.<br><br>Пример: <br><table><tr><td>Ввод</td><td>Вывод</td></tr><tr><td>Кривошеее существо гуляет по парку</td><td>гуляет</td></tr></table>
## Доп. задание №2 (+22 баллов)
___Вариант №1___
1. Реализуйте программный продукт на языке Python, используя регулярные выражения по варианту, представленному в таблице.
2. Для своей программы придумайте минимум 5 тестов.
3. Протестируйте свою программу на этих тестах.

| Номер в ИСУ % 4 | Задание |
|---|---|
| 0 | Написать регулярное выражение, которое проверяет корректность email и в качестве ответа выдаёт почтовый сервер (почтовый сервер – часть email идущая после «@»).<br><br>Для простоты будем считать, что почтовый адрес может содержать в себе буквы, цифры, «.» и «_», а почтовый сервер только буквы и «.». При этом почтовый сервер, обязательно должен содержать верхний уровень домена («.ru», «.com», etc.)<br><br>Пример:<br><table><tr><td>Ввод</td><td>Вывод</td></tr><tr><td>students.spam@yandex.ru</td><td>yandex.ru</td></tr><tr><td>example@example</td><td>Fail!</td></tr><tr><td>example@example.com</td><td>example.com</td></tr></table>
| 1 | С помощью регулярного выражения найти в тексте слова, в которых встречается строго одна гласная буква (встречаться она может несколько раз). Пример таких слов: окно, трава, молоко, etc.<br><br>После чего данные слова требуется отсортировать по увеличению длины слова.<br><br>Пример:<br><table><tr><td>Ввод</td><td>Вывод</td></tr><tr><td>Классное слово – обороноспособность, которое должно идти после слов: трава и молоко.</td><td>и<br>слов<br>идти<br>слово<br>трава<br>должно<br>молоко<br>обороноспособность</td></tr></table>
| 2 | Студент Вася очень любит курс «Компьютерная безопасность». Однажды Васе задали домашнее задание зашифровать данные, переданные в сообщение. Недолго думая, Вася решил заменить все целые числа на функцию от этого числа. Функцию он придумал не сложную 3𝑥<sup>2</sup>+5, где 𝑥−исходное число. Помогите Васе с его домашним заданием.<br><br>Пример:<br><table><tr><td>Ввод</td><td>Вывод</td></tr><tr><td>20 + 22 = 42</td><td>1205 + 1457 = 5297</td></tr></table>
| 3 | Вывесили списки стипендиатов текущего семестра, которые представляют из себя список людей ФИО и номер группы этого человека. Вы решили подшутить над некоторыми из своих одногруппников и удалить их из списка. <br><br>С помощью регулярного выражения найдите всех студентов своей группы, у которых инициалы начинаются на одну и туже букву и исключите их из списка.<br><br>Пример (группа P000):<br><table><tr><td>Ввод<td>Вывод</td></tr><tr><td>Петров П.П. P000<br>Анищенко А.А. P33113<br>Примеров Е.В. P000<br>Иванов И.И. P000</td><td>Анищенко А.А. P33113<br>Примеров Е.В. P000</td></tr></table>
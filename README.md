
# Лабораторная работа №8 PSQL.
# Цель:
Определить наиболее эффективный метод загрузки данных (малых и больших объемов) из CSV-файлов в СУБД PostgreSQL, сравнивая время выполнения для методов: pandas.to_sql(), psycopg2.copy_expert() (с файлом и с io.StringIO), и пакетная вставка (psycopg2.extras.execute_values).
# Выполнение заданий:
## 1. Подключение к библиотекам.
![image](https://github.com/user-attachments/assets/7ba89229-6cc4-427c-9ea3-e720d5b5816a)
![image](https://github.com/user-attachments/assets/6a963107-33e5-4bf2-8df1-095a72d30099)
## 2. Пути к файлам, Установка и импорт необходимых библиотек.
![image](https://github.com/user-attachments/assets/e2bbf382-f704-47fa-9c0a-a4bb853f512c)
![image](https://github.com/user-attachments/assets/4506914d-e790-444f-9a3d-e8bc1798f0e4)
## 3. Теперь можно приступать к загрузке csv файлов различными методами.
![image](https://github.com/user-attachments/assets/ca0727f2-190c-4323-972e-d1fdb785148a)
## 4. Проведем визуализацию результатов.
![image](https://github.com/user-attachments/assets/75160eb9-5f32-4561-ab8d-c4c76a9970e2)
В итоге видно что на небольших файлах copy_export(StringIO) и copy_export(file) показывают примерно одинаковых результат, на болшем объеме данных copy_export(file) оказывается уже в 2 раза быстрее. Pandas.to_sql же при работе с любым размером файла показывает неудоволетвориельный результат.
# Индивидуальные задания. Вариант 7.
## Определим вспомогательные функции, воспользовавших примером.
![image](https://github.com/user-attachments/assets/cf889a83-72bd-4950-b58c-95f705112461)
![image](https://github.com/user-attachments/assets/dd797aa3-4983-4fa4-9298-85bf0aaa0643)
![image](https://github.com/user-attachments/assets/2ece1a20-d521-42c7-a24e-486fc2b29f54)
![image](https://github.com/user-attachments/assets/b5fc20d5-14c6-4838-8c4a-33482f2dc8f1)
## Задание №1. Создать таблицы sales_small, sales_big.	
![image](https://github.com/user-attachments/assets/71631842-77a8-44a2-8788-a72ac5785fb6)
![image](https://github.com/user-attachments/assets/51714d92-400f-4621-8d1e-8b22e996d37d)
![image](https://github.com/user-attachments/assets/839ff2d1-afd2-4b18-a64f-971e59d309b7)
## Задание №2. Метод: pandas.to_sql().
![image](https://github.com/user-attachments/assets/17bb7d1f-ab36-4391-952b-0a724111bac6)
![image](https://github.com/user-attachments/assets/a45275f1-d10c-48be-9bb4-c1bccd766e4f)
## Задание №3. Метод: copy_expert (file).
![image](https://github.com/user-attachments/assets/3089985a-ce27-4335-9723-146bf22679e0)
![image](https://github.com/user-attachments/assets/527b5538-bb40-405a-b10e-5f1fd11e9446)
![image](https://github.com/user-attachments/assets/eae49a29-a2fb-4fc0-84d0-b1fc51420bef)
## Задание №4. Метод: SQL: Выбрать id, total_revenue для 10 записей с макс. выручкой из sales_big.
![image](https://github.com/user-attachments/assets/086f7ac9-f1da-40b9-a480-8522001a0f1c)
![image](https://github.com/user-attachments/assets/f60ceafc-4f39-4c05-905c-d4f612a7ce8f)
![image](https://github.com/user-attachments/assets/a57070f8-af38-47c1-8d59-b42a8e2841c9)
## Задание №5. Python: Извлечь результаты SQL (задание 4) в DataFrame и вывести его.
![image](https://github.com/user-attachments/assets/917222b0-2387-44a0-a5e9-e977fcc2a12c)
![image](https://github.com/user-attachments/assets/08c95ba6-c9ea-4531-9b49-a78e7fa8a125)
![image](https://github.com/user-attachments/assets/dfee592c-442e-4075-be7c-2c627b962350)
# Вывод:
В хоже работы были изучены методы загрузки данных разных объемов из CSV-файлов в СУБД PostgreSQL, также была проведена визуализация полученных результатов.

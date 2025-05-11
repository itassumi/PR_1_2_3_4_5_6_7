# Практична робота №4

## Тема
**Реалізація нової сутності, створення CRUD-операцій та відповідного RESTful API**

## Мета
Закріпити навички створення повноцінної серверної логіки для роботи з новою сутністю за допомогою **TypeORM**, **Express** та **TypeDI**. Ознайомитися з процедурою створення міграцій, перевірки змін у структурі бази даних та тестування REST API через **Postman**.

---

## Завдання

### 1. Створення нової сутності `Post`  
![1](https://github.com/itassumi/PR_1_2_3_4_5_6_7/blob/ddba548478d88eab9a19ebbf20cd5e4cb427d162/PR_1_2_4_5_6_7/PR_4/screen/1.png)

---

### 2. Створення та виконання міграції
- Створити міграцію для сутності `Post`
- Виконати міграцію:

![2_4](https://github.com/itassumi/PR_1_2_3_4_5_6_7/blob/ddba548478d88eab9a19ebbf20cd5e4cb427d162/PR_1_2_4_5_6_7/PR_4/screen/2_4.png)

- Перевірити результат виконання через IDE:

![3](https://github.com/itassumi/PR_1_2_3_4_5_6_7/blob/ddba548478d88eab9a19ebbf20cd5e4cb427d162/PR_1_2_4_5_6_7/PR_4/screen/3.png)

---

### 3. Реалізація REST API (CRUD для `Post`)
- Створити контролер та сервіси  
- Налаштувати маршрути відповідно до REST принципів  

![4_4](https://github.com/itassumi/PR_1_2_3_4_5_6_7/blob/ddba548478d88eab9a19ebbf20cd5e4cb427d162/PR_1_2_4_5_6_7/PR_4/screen/4_4.png)  
![5_4](https://github.com/itassumi/PR_1_2_3_4_5_6_7/blob/ddba548478d88eab9a19ebbf20cd5e4cb427d162/PR_1_2_4_5_6_7/PR_4/screen/5_4.png)

---

### 4. Тестування через Postman
- Додати нові ендпоінти до колекції Postman  
- Протестувати всі CRUD-операції  

![6](https://github.com/itassumi/PR_1_2_3_4_5_6_7/blob/ddba548478d88eab9a19ebbf20cd5e4cb427d162/PR_1_2_4_5_6_7/PR_4/screen/6.png)

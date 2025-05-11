# Практична робота №4

## Тема
**Реалізація нової сутності, створення CRUD-операцій та відповідного RESTful API**

## Мета
Закріпити навички створення повноцінної серверної логіки для роботи з новою сутністю за допомогою **TypeORM**, **Express** та **TypeDI**. Ознайомитися з процедурою створення міграцій, перевірки змін у структурі бази даних та тестування REST API через **Postman**.

---

## Завдання

### 1. Створення нової сутності `Post`  
![Скріншот 1](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/16dda30b773177884d7af147b8d25606a055aeaf/PR_4/screen/1.png?raw=true)

---

### 2. Створення та виконання міграції
- Створити міграцію для сутності `Post`
- Виконати міграцію:

![Скріншот 2](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/16dda30b773177884d7af147b8d25606a055aeaf/PR_4/screen/2.png?raw=true)

- Перевірити результат виконання через IDE:

![Скріншот 3](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/16dda30b773177884d7af147b8d25606a055aeaf/PR_4/screen/3.png?raw=true)

---

### 3. Реалізація REST API (CRUD для `Post`)
- Створити контролер та сервіси  
- Налаштувати маршрути відповідно до REST принципів  

![Скріншот 4](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/16dda30b773177884d7af147b8d25606a055aeaf/PR_4/screen/4.png?raw=true)  
![Скріншот 5](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/16dda30b773177884d7af147b8d25606a055aeaf/PR_4/screen/5.png?raw=true)

---

### 4. Тестування через Postman
- Додати нові ендпоінти до колекції Postman  
- Протестувати всі CRUD-операції  

![Скріншот 6](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/16dda30b773177884d7af147b8d25606a055aeaf/PR_4/screen/6.png?raw=true)

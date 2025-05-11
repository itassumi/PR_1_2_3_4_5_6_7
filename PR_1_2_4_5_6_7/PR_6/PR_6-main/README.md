# Практична робота №6

## Тема
**Розробка UI для реалізації CRUD-операцій**

## Мета
Створити користувацький інтерфейс для взаємодії з реалізованим RESTful API, що надає можливість **перегляду, створення, редагування та видалення** екземплярів певної сутності.  
Розробка ведеться на базі **React** з використанням **TanStack Router** для реалізації маршрутизації.

---

## Завдання

На основі boilerplate-проєкту [`vite-react-boilerplate`](https://github.com) реалізувати UI для роботи з сутністю `Post`, яка була створена у попередньому занятті.

---

### 1. Сторінка колекції екземплярів сутності (`/posts`)

- Відображення списку всіх доступних `Post`
- Показ основної інформації для кожного елемента
- Перехід до перегляду конкретного поста: `/posts/:id`
- Кнопка **"Створити новий екземпляр"** → `/posts/new`
- Реалізація **видалення** елементів (із підтвердженням дії)

![1](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/bb122f1f9ece06f30aea75d311eb2a5a26705862/PR_6/screen/1.png?raw=true)
![2](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/bb122f1f9ece06f30aea75d311eb2a5a26705862/PR_6/screen/2.png?raw=true)
![3](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/bb122f1f9ece06f30aea75d311eb2a5a26705862/PR_6/screen/3.png?raw=true)
![4](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/bb122f1f9ece06f30aea75d311eb2a5a26705862/PR_6/screen/4.png?raw=true)
![5](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/bb122f1f9ece06f30aea75d311eb2a5a26705862/PR_6/screen/5.png?raw=true)

---

### 2. Сторінка одного поста (`/posts/:id`) або створення нового (`/posts/new`)

#### `/posts/:id` (перегляд та редагування)

- Повне відображення інформації
- Форма редагування
- Кнопка **Update** для збереження змін

#### `/posts/new` (створення)

- Форма з порожніми полями
- Кнопка **Create** для збереження нового поста

![6](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/bb122f1f9ece06f30aea75d311eb2a5a26705862/PR_6/screen/6.png?raw=true)
![7](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/bb122f1f9ece06f30aea75d311eb2a5a26705862/PR_6/screen/7.png?raw=true)

---

### Результат

![8](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/bb122f1f9ece06f30aea75d311eb2a5a26705862/PR_6/screen/8.png?raw=true)
![9](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/bb122f1f9ece06f30aea75d311eb2a5a26705862/PR_6/screen/9.png?raw=true)
![10](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/bb122f1f9ece06f30aea75d311eb2a5a26705862/PR_6/screen/10.png?raw=true)
![11](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/bb122f1f9ece06f30aea75d311eb2a5a26705862/PR_6/screen/11.png?raw=true)
![12](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/bb122f1f9ece06f30aea75d311eb2a5a26705862/PR_6/screen/12.png?raw=true)
![13](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/bb122f1f9ece06f30aea75d311eb2a5a26705862/PR_6/screen/13.png?raw=true)

 

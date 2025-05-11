# Практично-лабораторне заняття №7

## Тема
**Інтеграція клієнтської частини з RESTful API**

## Мета
Підключити користувацький інтерфейс до реального серверного API.  
Ознайомитися з підходами до організації HTTP-запитів через Axios, зберігання токенів доступу, обробки помилок, роботи з `.env`-змінними.  
Забезпечити повноцінну взаємодію клієнтської частини з бекендом.

---

## Завдання

Використовуючи реалізовану у попередньому завданні клієнтську частину (інтерфейс для роботи з сутністю `Post`), внести такі зміни:

---

### 1. Налаштування змінних оточення

- У корені проєкту створити файл `.env`
- Додати такі змінні:

```env
VITE_API_BASE_URL=http://localhost:4000/v1
VITE_API_AUTH_TOKEN=your_jwt_token_here
```

![.env приклад](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/6be2aa28e7644418a8a7c6597f59644160dfabea/PR_7/screen/1.png?raw=true)

---

### 2. Створення конфігурації Axios

- Створити файл `src/api/axios.ts`
- Налаштувати:
  - `baseURL`
  - заголовки: `Content-Type: application/json`
  - авторизацію через токен (`Authorization: Bearer ...`)
- Реалізувати обробку помилок через інтерцептор (лог або повідомлення)

![Axios приклад](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/6be2aa28e7644418a8a7c6597f59644160dfabea/PR_7/screen/2.png?raw=true)
![Інтерцептор](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/6be2aa28e7644418a8a7c6597f59644160dfabea/PR_7/screen/3.png?raw=true)

---

### 3. Реальні запити замість моків

У файлі `src/api/posts.ts` реалізувати функції з використанням Axios:

- `getAllEntities()` → `GET /posts`
- `getEntityById(id)` → `GET /posts/:id`
- `createEntity(data)` → `POST /posts`
- `updateEntity(id, data)` → `PUT /posts/:id`
- `deleteEntity(id)` → `DELETE /posts/:id`

**Порада:** Використовуйте типізовані відповіді (Generics у Axios) для кращої розробки.

![Запити](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/6be2aa28e7644418a8a7c6597f59644160dfabea/PR_7/screen/4.png?raw=true)
![Код приклад](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/6be2aa28e7644418a8a7c6597f59644160dfabea/PR_7/screen/5.png?raw=true)
![Виклик API](https://github.com/itassumi/PR_1_2_4_5_6_7_8/blob/6be2aa28e7644418a8a7c6597f59644160dfabea/PR_7/screen/6.png?raw=true)

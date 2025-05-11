# Лабораторна робота: Ознайомлення з TypeScript

**Виконала**: Коляда Анастасія, ІПЗ - 3.02

---

## Завдання 1: Типізація змінних

### Опис завдання:
Оголосіть змінні наступних типів: `string`, `number`, `boolean`, `array`, `object`.
Створіть функцію, яка приймає як аргумент об'єкт із полями `name` (тип `string`) та `age` (тип `number`) і повертає рядок виду:
**"Name: John, Age: 30"**.

### Результат:
![Результат](https://github.com/user-attachments/assets/112106d3-d1a8-45b1-b6c3-8e9ece801032)

### Перевірка:
#### JS:
![JS](https://github.com/user-attachments/assets/b48a9d7d-97b3-40e7-83bc-9cfe1d46fa5a)

#### .D.TS:
![DTS](https://github.com/user-attachments/assets/22746e00-4f25-434a-acf3-47024a7a4b2d)

#### Errors:
![Errors](https://github.com/user-attachments/assets/19224ded-1fbf-4a5f-984f-d9747918770d)

#### Logs:
![Logs](https://github.com/user-attachments/assets/9dc435dd-5f88-4a8a-af75-3cc5b667edb1)

---

## Завдання 2: Інтерфейси

### Опис завдання:
Оголосіть інтерфейс `Person`, який містить поля:

```ts
interface Person {
  name: string;
  age: number;
  address?: string; // Опціональне поле
}
```

Реалізуйте функцію `printPerson`, яка приймає об'єкт типу `Person` та виводить його дані у консоль.

### Результат:
![Результат](https://github.com/user-attachments/assets/9a84d5f1-1ff6-4421-9338-213ab4d3c93a)

### Перевірка:
#### JS:
![JS](https://github.com/user-attachments/assets/864df4df-cf6e-4279-a424-683e3bd1a0fd)

#### .D.TS:
![DTS](https://github.com/user-attachments/assets/b7a15c9f-fd81-47d1-af19-f3d162e24d06)

#### Errors:
![Errors](https://github.com/user-attachments/assets/a6a369ca-d229-4f7e-b646-d8be75165572)

#### Logs:
![Logs](https://github.com/user-attachments/assets/b5a7c85c-5ab6-4cbf-9bef-add1b59dd834)

---

## Завдання 3: Композитні типи

### Опис завдання:
Оголосіть об'єднаний тип (`union type`), наприклад:

```ts
type Status = 'success' | 'error' | 'loading';
```

Реалізуйте конструкцію (наприклад, функцію або умову), яка виводить повідомлення відповідно до значення `Status`.

### Результат:
![Результат](https://github.com/user-attachments/assets/fce54aba-14f5-464a-bf88-13ac86b73bb3)

### Перевірка:
#### JS:
![JS](https://github.com/user-attachments/assets/97dcc4dd-3d03-4913-bff7-2a9ddd870f07)

#### .D.TS:
![DTS](https://github.com/user-attachments/assets/a8c63768-c90c-41aa-aaf8-9419d9e0b10a)

#### Errors:
![Errors](https://github.com/user-attachments/assets/8ddb653f-fef3-44f6-ba31-839386753530)

#### Logs:
![Logs](https://github.com/user-attachments/assets/2fe4e83e-d348-49cc-8f70-2980c7771493)

---

## Завдання 4: Дженерики

### Опис завдання:
Реалізуйте функцію:

```ts
function identity<T>(value: T): T {
  return value;
}
```

Використайте її для типів `number`, `string` та `boolean`.

### Результат:
![Результат](https://github.com/user-attachments/assets/6ab99d2d-d752-4f76-b4dc-ebfe2e342f6d)

### Перевірка:
#### JS:
![JS](https://github.com/user-attachments/assets/bedf05d8-5346-4196-91ed-07863922031a)

#### .D.TS:
![DTS](https://github.com/user-attachments/assets/d5bfdabf-8274-400f-b89f-29bddc04146c)

#### Errors:
![Errors](https://github.com/user-attachments/assets/e5ddff1d-ba32-4331-9c85-831b6b2a0700)

#### Logs:
![Logs](https://github.com/user-attachments/assets/30ef9e85-cd47-44a2-a7bd-58aa8d89427a)

---

## Завдання 5: Класи

### Опис завдання:
Реалізуйте клас:

```ts
class Car {
  constructor(public model: string, public year: number) {}

  getCarInfo(): string {
    return `Model: ${this.model}, Year: ${this.year}`;
  }
}
```

### Результат:
![Результат](https://github.com/user-attachments/assets/c4aff26a-e085-4c12-87b4-5ac6726d03e4)

### Перевірка:
#### JS:
![JS](https://github.com/user-attachments/assets/804dc4dc-22d2-4be2-9264-8a04bafca572)

#### .D.TS:
![DTS](https://github.com/user-attachments/assets/2b04da9a-832b-4d10-8c69-af68367af638)

#### Errors:
![Errors](https://github.com/user-attachments/assets/146be931-0fc2-414d-b7e5-093918f314a2)

#### Logs:
![Logs](https://github.com/user-attachments/assets/a852b13a-fb30-487a-a9f5-20a645df1235)




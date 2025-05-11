# Практично-лабораторне заняття №8
## Тема
**Неперервна інтеграція (CI)**

## Мета
Ознайомитись з принципами і практиками неперервної інтеграції, сформувати навички автоматизації CI/CD процесів у GitHub Actions.

## Визначення

Неперервна інтеграція (CI) — це практика розробки програмного забезпечення, коли розробники регулярно об'єднують свої зміни коду в центральному репозиторії, після чого автоматично виконуються збірка та тести.

## Завдання

### 1. Завершити наступні практичні роботи на GitHub Skills та надати посилання на репозиторії з виконаним завданням у звіті:
- ✅ Hello GitHub Actions  
- ✅ Publish Packages  

### Результат роботи:
![1](https://github.com/user-attachments/assets/c8d29386-cf70-492c-9e83-322271b4110e)
![2](https://github.com/user-attachments/assets/1b8f169a-ceee-4a52-8740-36f639fbb39a)
![3](https://github.com/user-attachments/assets/f6961ecf-2c2c-48e1-9dca-14d730e4e31d)
![4](https://github.com/user-attachments/assets/b4b5367e-526a-4aec-90cd-ba283ef69c72)
![5](https://github.com/user-attachments/assets/74559202-ee71-413a-8052-5fc35b480028)
![6](https://github.com/user-attachments/assets/20574031-b039-4eab-b860-6b53f0ff5b29)
![7](https://github.com/user-attachments/assets/3688ba04-3dad-4524-a4ad-b51fbac2f3d0)
![8](https://github.com/user-attachments/assets/ec99ec61-81c7-4f35-ade5-d0a37805b36b)
![9](https://github.com/user-attachments/assets/599c8548-901d-4fce-8825-7ee9f9dc4a55)
![10](https://github.com/user-attachments/assets/02505588-4204-44d8-a29e-a234a122707b)
![11](https://github.com/user-attachments/assets/2226db3a-a09e-4650-a43a-269c73425176)
![12](https://github.com/user-attachments/assets/86b1f685-c483-4dc1-b217-4a39722b97c8)
![13](https://github.com/user-attachments/assets/ec7d7488-cfdc-437a-960c-4d5a382b382e)
![14](https://github.com/user-attachments/assets/5edf8ee7-c3e9-4361-bd76-dd706898b2ae)
![15](https://github.com/user-attachments/assets/7d05eea2-1fba-4d88-9927-09fd765ed261)
![1](https://github.com/user-attachments/assets/a49baafb-080f-4d9e-bbe9-9a0ad19e2004)
![2](https://github.com/user-attachments/assets/22b61e2b-79d3-4a5f-aa56-18491a21e1de)
![3](https://github.com/user-attachments/assets/4d7f27f3-d4db-46a0-a604-f96c40d4cb8b)
![4](https://github.com/user-attachments/assets/974d2167-e5bd-45b6-98a4-47a4964d0820)
![5](https://github.com/user-attachments/assets/8d3913d3-8ff0-4162-8271-ca8575ab647e)
![6](https://github.com/user-attachments/assets/c80236b5-ac0c-4806-a5ed-0b4ecd981096)
![7](https://github.com/user-attachments/assets/0772584e-b5ff-4483-bcfc-d92dbcdcbd5d)
![8](https://github.com/user-attachments/assets/24bfc888-2b9b-4527-8184-0f1c5ff92641)
![9](https://github.com/user-attachments/assets/9e3a66a1-c21f-48a4-810d-a2965b609cf1)
![10](https://github.com/user-attachments/assets/e21a2a4e-160e-4ed6-a350-c309ab11537f)
![11](https://github.com/user-attachments/assets/6dd0266f-16ff-4baf-b846-59daea13be16)

### 2. Створити власний GitHub Workflow для збірки Docker-образу Front-End репозиторію та завантаження його у GitHub Container Registry
#### 2.1. Створити воркфлоу з двома тригерами:
- ручний запуск (workflow_dispatch)
- push до гілок: main, feature/*
#### 2.2. Workflow має містити 1 job з наступними кроками:
- клонування репозиторію за допомогою actions/checkout
- встановлення pnpm, встановлення залежностей (pnpm install) і збірка проекту (pnpm run build) в одному кроці
- авторизація в GitHub Container Registry:
  - registry: ghcr.io
  - username: ${{ github.actor }}
  - password: ${{ secrets.GITHUB_TOKEN }}
- збірка та пуш Docker-образу:
  - context: .
  - push: true
  - tags: ghcr.io/${{ github.repository_owner }}/${{ github.event.repository.name }}
#### 2.3. Перевірити результат на вкладці Packages в GitHub, має з’явитися завантажений Docker-образ

![1](https://github.com/user-attachments/assets/91be0776-e06f-4d5d-a734-e1b9613a6213)
![2](https://github.com/user-attachments/assets/c82b044f-bf4e-4414-a734-70dbc18bee2a)
![3](https://github.com/user-attachments/assets/40446032-ffbc-4f0f-8a0b-b6f31a289a63)
![4](https://github.com/user-attachments/assets/218c5e0a-4805-4173-a825-11316d646b73)



# Практично-лабораторне заняття №9  
**Тема:** Неперервна доставка  
**Мета:** ознайомитися з принципами і практиками неперервної доставки, сформувати навички роботи з хмарними сервісами Azure

---

## Завдання

1. **Створити Azure App Service у власній підписці Azure:**
   - Створити ресурсну групу (resource group)
   - Створити всередині ресурсної групи App Service. При створенні вибрати деплой контейнеру замість коду

2. **Створити у Azure Service principal, який буде використовуватись для доступу GitHub до вашої підписки Azure:**
   - В порталі Azure натисніть значок з командним рядком → виберіть **Bash**
   - При створенні App Service Plan оберіть план **Free**
   - Виконайте команду:
     ```bash
     az ad sp create-for-rbac --name "myApp" --role contributor --scopes /subscriptions/<subscription_id>/resourceGroups/<resource_group_name> --json-auth
     ```
   - `subscription_id` знайдіть у розділі **Subscriptions** на порталі Azure
   - Після виконання команди скопіюйте вивід у форматі:
     ```json
     {
       "clientId": "<GUID>",
       "clientSecret": "<GUID>",
       "subscriptionId": "<GUID>",
       "tenantId": "<GUID>"
     }
     ```

3. **У GitHub-репозиторії:**
   - Перейдіть в **Settings → Secrets and variables → Actions → New Repository Secret**
   - Назва: `AZURE_CREDENTIALS`
   - Значення: вивід команди з попереднього кроку (без пробілів або переносу рядків в кінці)

4. **Додати нову job у GitHub Actions workflow:**

   #### Логін в Azure:
   ```yaml
   - uses: azure/login@v2
     with:
       creds: ${{ secrets.AZURE_CREDENTIALS }}
   ```

   #### Деплой у App Service:
   ```yaml
   - name: Deploy to Azure Web App
     uses: azure/webapps-deploy@v2
     with:
       app-name: <app_service_name>
       images: ghcr.io/${{ github.repository_owner }}/${{ github.event.repository.name }}:latest
   ```

5. **Запустіть workflow** і перевірте, що він завершився успішно

6. **У логах `Deploy to Azure Web App` знайдіть посилання, що починається з `App Service Application Url`** — воно веде до вашого розгорнутого сайту

---

## Виконання роботи та результати:

![1](https://github.com/user-attachments/assets/80e0529a-37fe-4be7-bb12-7dfa84f03f88)  
![2](https://github.com/user-attachments/assets/af27e88c-63ac-4b44-b4c0-c200c93f64de)  
![3](https://github.com/user-attachments/assets/8c95d414-341f-4f28-b66c-13cb19fc05a6)  
![4](https://github.com/user-attachments/assets/86b05b1d-c140-4941-85a1-ed1c06d20da2)  
![5](https://github.com/user-attachments/assets/959c82d9-8b14-4057-a95d-35420130e34a)  
![6](https://github.com/user-attachments/assets/d414d665-04f6-4735-b1d7-cd844d1a40d5)



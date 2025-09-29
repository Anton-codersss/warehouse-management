# Инструкции по развертыванию

## 🚀 Пошаговое развертывание

### 1. Railway (Backend + Database)

1. **Зарегистрируйтесь на Railway**:
   - Перейдите на https://railway.app
   - Создайте аккаунт через GitHub

2. **Создайте новый проект**:
   - Нажмите "New Project"
   - Выберите "Deploy from GitHub repo"
   - Загрузите папку `warehouse-backend`

3. **Настройте переменные окружения**:
   ```
   NODE_ENV=production
   JWT_SECRET=warehouse_management_secret_key_2024_production
   FRONTEND_URL=https://ваш-frontend.vercel.app
   ```

4. **Добавьте PostgreSQL**:
   - В проекте нажмите "Add Service"
   - Выберите "PostgreSQL"
   - Railway автоматически создаст DATABASE_URL

5. **Получите URL backend**:
   - После развертывания получите URL типа: `https://ваш-проект.railway.app`

### 2. Vercel (Frontend)

1. **Зарегистрируйтесь на Vercel**:
   - Перейдите на https://vercel.com
   - Создайте аккаунт через GitHub

2. **Создайте новый проект**:
   - Нажмите "Add New"
   - Выберите "Project"
   - Загрузите папку `warehouse-frontend`

3. **Настройте переменные окружения**:
   ```
   VITE_API_URL=https://ваш-backend.railway.app/api
   ```

4. **Получите URL frontend**:
   - После развертывания получите URL типа: `https://ваш-проект.vercel.app`

### 3. Обновите CORS в backend

В Railway проекте обновите переменную:
```
FRONTEND_URL=https://ваш-frontend.vercel.app
```

## ✅ Результат

После завершения у вас будет:
- **Frontend**: https://ваш-проект.vercel.app
- **Backend**: https://ваш-проект.railway.app
- **3 аккаунта**: admin/admin123, operator1/pass123, operator2/pass123

## 🔧 Альтернативный способ

Если нужна помощь с развертыванием:
1. Создайте аккаунты на Railway и Vercel
2. Предоставьте доступ к проектам
3. Я помогу настроить развертывание удаленно

## 📞 Поддержка

При возникновении проблем:
- Проверьте переменные окружения
- Убедитесь, что CORS настроен правильно
- Проверьте логи в Railway и Vercel
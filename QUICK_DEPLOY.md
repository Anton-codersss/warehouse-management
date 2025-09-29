# 🚀 Быстрое развертывание - 5 минут

## Способ 1: Автоматическое развертывание через GitHub

### Шаг 1: Создайте GitHub репозиторий
1. Идите на https://github.com
2. Создайте новый публичный репозиторий `warehouse-management`
3. Загрузите все файлы из папки `c:\Progrs\Ver03`

### Шаг 2: Развертывание Backend на Railway
1. Идите на https://railway.app
2. Войдите через GitHub
3. Нажмите "New Project" → "Deploy from GitHub repo"
4. Выберите ваш репозиторий `warehouse-management`
5. Выберите папку `/warehouse-backend`
6. Добавьте переменные окружения:
   ```
   NODE_ENV=production
   JWT_SECRET=warehouse_secret_2024_prod
   ```
7. Добавьте PostgreSQL: "Add Service" → "PostgreSQL"
8. Скопируйте URL backend (типа `https://xyz.railway.app`)

### Шаг 3: Развертывание Frontend на Vercel
1. Идите на https://vercel.com
2. Войдите через GitHub
3. Нажмите "Add New" → "Project"
4. Выберите ваш репозиторий `warehouse-management`
5. Выберите папку `/warehouse-frontend`
6. Добавьте переменную окружения:
   ```
   VITE_API_URL=https://ваш-backend.railway.app/api
   ```
7. Нажмите "Deploy"
8. Скопируйте URL frontend (типа `https://xyz.vercel.app`)

### Шаг 4: Обновите CORS
1. В Railway проекте добавьте переменную:
   ```
   FRONTEND_URL=https://ваш-frontend.vercel.app
   ```

## ✅ Готово!

Ваша система доступна по адресу: `https://ваш-frontend.vercel.app`

**Аккаунты для входа:**
- admin / admin123 (Администратор)
- operator1 / pass123 (Оператор)
- operator2 / pass123 (Оператор)

---

## Способ 2: Загрузка архивов (если нет GitHub)

1. **Файлы готовы для загрузки:**
   - `backend-deploy.zip` - для Railway
   - `frontend-deploy.zip` - для Vercel

2. **Следуйте инструкциям выше**, но вместо GitHub выберите "Upload folder"

---

## 🆘 Нужна помощь?

Если что-то не получается:
1. Создайте аккаунты на Railway и Vercel
2. Сообщите мне - помогу настроить удаленно

**Время развертывания: 5-10 минут**
**Стоимость: Бесплатно навсегда**
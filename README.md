# 🚀 Star Rocket - Telegram Mini App

**Star Rocket** — це захопливий Telegram Mini App, де гравці роблять ставки у Telegram Stars і намагаються зупинити ракету до її вибуху, щоб отримати виграш!

## 🎮 Механіка гри

- **Ставка**: від 100 до 2000 Telegram Stars
- **Множник**: рівень зростає від x1.05 до x10.00+
- **Вибір**: гравець може "забрати виграш" або ризикнути
- **Вибух**: якщо ракета вибухає — ставка програється

## 📋 Функції

✅ **Гра**
- Плавна анімація ракети
- Онлайн гравці (100-200)
- Бот-гравці з різними ніками
- Стрічка найбільших виграшів

✅ **Профіль**
- Баланс Telegram Stars
- Рівень та досвід
- Реферальна система
- Промокоди
- Вибір мови (УК/РУ/EN)

✅ **Адмін-панель**
- Створення промокодів
- Установка нагород
- Статистика гри

## 🛠 Технічний стек

- **Frontend**: React 18 + TypeScript + Vite
- **Backend**: Node.js + Express
- **БД**: PostgreSQL
- **Хостинг**: Render

## 📦 Встановлення

### 1. Клонування репозиторію
```bash
git clone https://github.com/lioscript/star-up.git
cd star-up
```

### 2. Встановлення залежностей

**Backend:**
```bash
npm install
```

**Frontend:**
```bash
cd client
npm install
cd ..
```

### 3. Налаштування .env

Скопіюйте `.env.example` у `.env`:
```bash
cp .env.example .env
```

Заповніть значення:
```
TELEGRAM_BOT_TOKEN=ваш_токен
DATABASE_URL=postgresql://user:password@localhost:5432/star_rocket
MINI_APP_URL=http://localhost:3000
PORT=3000
ADMIN_ID=5929338019
```

### 4. Ініціалізація БД

```bash
npm run init-db
```

### 5. Запуск локально

**Backend:**
```bash
npm run dev
```

**Frontend (новий термінал):**
```bash
cd client
npm run dev
```

## 🚀 Деплой на Render

### 1. Підготовка

- Створіть аккаунт на [Render](https://render.com)
- Підключіть GitHub репозиторій

### 2. Створення PostgreSQL БД

- На Render створіть PostgreSQL сервіс
- Скопіюйте `DATABASE_URL`

### 3. Створення веб-сервісу

- **Repository**: lioscript/star-up
- **Branch**: main
- **Build Command**: `npm install && cd client && npm install && cd .. && npm run build`
- **Start Command**: `node server/index.js`
- **Environment**:
  - `TELEGRAM_BOT_TOKEN`
  - `DATABASE_URL`
  - `MINI_APP_URL`
  - `ADMIN_ID`
  - `PORT=3000`

### 4. Deploy

Render автоматично буде деплоїти після кожного push на main!

## 📱 Додавання у Telegram

1. Відкрийте BotFather: https://t.me/BotFather
2. Оберіть вашого бота
3. Командуйте `/setmenubutton`
4. Введіть URL вашого Render сервісу

## 🎯 API Endpoints

### Game
- `GET /api/game/balance/:telegramId` - Баланс гравця
- `POST /api/game/result` - Записати результат

### User
- `GET /api/user/profile/:telegramId` - Профіль
- `POST /api/user/create` - Новий користувач
- `POST /api/user/promo` - Використати промокод

### Admin
- `POST /api/admin/promo/create` - Створити промокод
- `GET /api/admin/stats/:telegramId` - Статистика

## 📝 Ліцензія

MIT

## 👤 Автор

**lioscript** — GitHub

---

**Розроблено для гравців Telegram! 🎮💫**
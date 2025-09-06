# 🎓 TIUE Mobile App

<div align="center">

![TIUE Logo](https://img.shields.io/badge/TIUE-Mobile%20App-blue?style=for-the-badge&logo=react)
[![React Native](https://img.shields.io/badge/React%20Native-0.76.4-61DAFB?style=flat&logo=react)](https://reactnative.dev/)
[![Expo](https://img.shields.io/badge/Expo-~53.0.22-000020?style=flat&logo=expo)](https://expo.dev/)
[![Django](https://img.shields.io/badge/Django-5.0+-092E20?style=flat&logo=django)](https://djangoproject.com/)
[![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=flat&logo=python)](https://python.org/)

**Мобильное приложение для студентов и администрации ТИУЭ**

</div>

## 📱 О проекте

TIUE Mobile App - это комплексное мобильное приложение для студентов и администрации Таджикского исламского университета имени Хожи Умара (ТИУЭ). Приложение предоставляет удобный доступ к академической информации, новостям, расписанию и другим университетским услугам.

### ✨ Основные возможности

- 🔐 **Система аутентификации** - безопасный вход для студентов и администраторов
- 📰 **Новости университета** - актуальные новости с изображениями и событиями
- 📅 **Расписание занятий** - персональное расписание для каждого студента
- 👥 **Управление пользователями** - административная панель для управления студентами
- 🌙 **Темная тема** - поддержка светлой и темной тем с переключением
- 📱 **Адаптивный дизайн** - оптимизация для различных размеров экранов
- 🔄 **Синхронизация данных** - автоматическое обновление информации

## 🏗️ Технологический стек

### Frontend (React Native)
- **React Native** `0.76.4` - кроссплатформенная мобильная разработка
- **Expo** `~53.0.22` - платформа для быстрой разработки
- **TypeScript** - типизированный JavaScript
- **Redux Toolkit** - управление состоянием приложения
- **React Navigation** - навигация между экранами
- **Expo Router** - файловая маршрутизация
- **React Native Reanimated** - плавные анимации
- **Expo Linear Gradient** - градиентные фоны

### Backend (Django)
- **Django** `5.0+` - веб-фреймворк на Python
- **Django REST Framework** - API для мобильного приложения
- **Python** `3.9+` - серверная логика
- **SQLite/PostgreSQL** - база данных
- **Django CORS Headers** - поддержка CORS

## 🚀 Быстрый старт

### Предварительные требования

Убедитесь, что у вас установлено:

- **Node.js** (версия 18 или выше) - [Скачать](https://nodejs.org/)
- **Python** (версия 3.9 или выше) - [Скачать](https://python.org/)
- **Git** - [Скачать](https://git-scm.com/)
- **Expo CLI** (глобально):
  ```bash
  npm install -g @expo/cli
  ```

### 📦 Установка

#### 1. Клонирование репозитория
```bash
git clone https://github.com/scrollDynasty/tiueapp.git
cd tiueapp
```

#### 2. Настройка Frontend (React Native)
```bash
# Установка зависимостей
npm install

# Или с yarn
yarn install
```

#### 3. Настройка Backend (Django)
```bash
# Переход в папку backend
cd backend

# Создание виртуального окружения
python -m venv venv

# Активация виртуального окружения
# На Windows:
venv\Scripts\activate
# На macOS/Linux:
source venv/bin/activate

# Установка зависимостей Python
pip install -r requirements.txt

# Применение миграций базы данных
python manage.py migrate

# Создание суперпользователя (администратора)
python manage.py createsuperuser

# Возврат в корневую папку
cd ..
```

## 🎮 Запуск приложения

### Backend сервер (Django)
```bash
# В папке backend с активированным venv
cd backend
python manage.py runserver

# Сервер будет доступен по адресу: http://localhost:8000
```

### Frontend приложение (React Native)
```bash
# В корневой папке проекта
npx expo start

# Или для запуска с очисткой кеша
npx expo start --clear
```

### 📱 Варианты запуска мобильного приложения

После выполнения `npx expo start` выберите один из вариантов:

1. **📱 Expo Go** (для быстрого тестирования):
   - Установите [Expo Go](https://expo.dev/go) на телефон
   - Отсканируйте QR-код с терминала

2. **🤖 Android эмулятор**:
   ```bash
   npx expo run:android
   ```

3. **🍎 iOS симулятор** (только на macOS):
   ```bash
   npx expo run:ios
   ```

4. **🌐 Веб-версия**:
   ```bash
   npx expo start --web
   ```

## 📂 Структура проекта

```
tiueapp/
├── 📱 app/                    # React Native приложение
│   ├── (auth)/               # Экраны аутентификации
│   ├── (tabs)/               # Основные вкладки приложения
│   ├── admin/                # Административные экраны
│   ├── news/                 # Экраны новостей
│   └── login.tsx             # Экран входа
├── 🎨 components/            # Переиспользуемые компоненты
├── 🎯 constants/             # Константы (цвета, стили)
├── 🔄 contexts/              # React контексты (темы)
├── 🪝 hooks/                 # Пользовательские хуки
├── 🏪 store/                 # Redux store и слайсы
├── 🔧 services/              # API сервисы
├── 📐 types/                 # TypeScript типы
├── 🎨 styles/                # Глобальные стили
├── 🖼️ assets/               # Изображения, шрифты
└── 🗄️ backend/              # Django backend
    ├── authentication/       # Аутентификация
    ├── users/               # Управление пользователями
    ├── news/                # Новости
    ├── schedule/            # Расписание
    ├── groups/              # Учебные группы
    └── tiuebackend/         # Настройки Django
```

## 🛠️ Доступные команды

### Frontend команды
```bash
# Запуск в режиме разработки
npm start

# Запуск на Android
npm run android

# Запуск на iOS
npm run ios

# Запуск в веб-браузере
npm run web

# Линтинг кода
npm run lint

# Сброс проекта к начальному состоянию
npm run reset-project
```

### Backend команды
```bash
# Запуск сервера разработки
python manage.py runserver

# Создание миграций
python manage.py makemigrations

# Применение миграций
python manage.py migrate

# Создание суперпользователя
python manage.py createsuperuser

# Открытие Django shell
python manage.py shell
```

## 🎨 Особенности дизайна

- **🌙 Адаптивная тема** - поддержка светлой и темной тем
- **📱 Мобильный дизайн** - оптимизация для мобильных устройств
- **🎭 Плавные анимации** - использование React Native Reanimated
- **🎨 Современный UI** - Material Design принципы
- **♿ Доступность** - поддержка accessibility features

## 🔧 Конфигурация

### Environment Variables

Создайте файл `.env` в папке `backend/`:

```env
SECRET_KEY=your-secret-key-here
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
DATABASE_URL=sqlite:///db.sqlite3
```

### API Endpoints

Backend предоставляет следующие API endpoints:

- `POST /api/auth/login/` - Вход в систему
- `POST /api/auth/logout/` - Выход из системы
- `GET /api/news/` - Список новостей
- `GET /api/schedule/` - Расписание
- `GET /api/users/` - Управление пользователями (только админ)

## 🧪 Тестирование

```bash
# Запуск тестов React Native
npm test

# Запуск тестов Django
cd backend
python manage.py test
```

## 📱 Сборка для продакшена

### Android APK
```bash
# Сборка APK
npx expo build:android

# Или создание standalone приложения
eas build --platform android
```

### iOS App Store
```bash
# Сборка для iOS (требуется macOS)
npx expo build:ios

# Или с EAS Build
eas build --platform ios
```

## 🤝 Вклад в проект

1. Форкните репозиторий
2. Создайте ветку для фичи (`git checkout -b feature/amazing-feature`)
3. Зафиксируйте изменения (`git commit -m 'Add amazing feature'`)
4. Отправьте в ветку (`git push origin feature/amazing-feature`)
5. Откройте Pull Request

## 📄 Лицензия

Этот проект распространяется под лицензией MIT. Подробности в файле [LICENSE](LICENSE).

## 👥 Команда

- **Разработчик**: scrollDynasty
- **Университет**: ТИУЭ (Таджикский исламский университет имени Хожи Умара)

## 📞 Поддержка

Если у вас есть вопросы или проблемы:

- 🐛 [Создайте Issue](https://github.com/scrollDynasty/tiueapp/issues)
- 📧 Напишите на email: support@tiue.edu.tj
- 💬 Telegram: @tiue_support

---

<div align="center">

**Сделано с ❤️ для студентов ТИУЭ**

</div>

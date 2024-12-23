#mindmap
### 1. Диаграмма Mindmap

Система приложения для кинотеатра предназначена для упрощения взаимодействия пользователей с кинотеатром. Она позволяет просматривать расписание, бронировать места, покупать билеты, заказывать закуски и оставлять отзывы. Приложение также предоставляет инструменты для администрации, улучшая управление и взаимодействие с клиентами, что повышает удобство и эффективность работы кинотеатра.

```mermaid
mindmap
  root((Приложение для кинотеатра))
    Пользователи
      Авторизация
        Вход
        Регистрация
      Профиль
        История сеансов
        Настройки пользователя
    Покупки
      Билеты
        Покупка
        Бронирование мест
      Попкорн и закуски
        Предзаказ
        Комбо-наборы
    Афиша
      Фильмы в прокате
        Жанры
        Рейтинги
        Описание
      Расписание сеансов
    Интерактив
      Оценки фильмов
      Комментарии
      Отзывы
    Администрация
      Управление пользователями
      Аналитика
        Популярные фильмы
        Загруженность сеансов

```
### 2. Диаграмма путешествия пользователя (User Journey Diagram)
```mermaid
journey
  title Путешествие пользователя в приложении кинотеатра
  section Регистрация и авторизация
    Заполняет форму регистрации: 5: Пользователь
    Вводит логин и пароль: 4: Пользователь
  section Изучение афиши
    Просматривает фильмы в прокате: 4: Пользователь
    Читает описание фильма: 5: Пользователь
    Сравнивает расписание сеансов: 3: Пользователь
  section Покупка билетов
    Выбирает место: 5: Пользователь
    Оформляет покупку: 4: Пользователь
  section Предзаказ закусок
    Выбирает комбо-набор: 3: Пользователь
    Оформляет заказ: 4: Пользователь
  section Посещение кинотеатра
    Использует QR-код для входа: 5: Пользователь
    Забирает заказ в баре: 4: Пользователь
  section Оставление отзыва
    Ставит оценку фильму: 4: Пользователь
    Пишет отзыв: 3: Пользователь

```
### 3. Квадрант-граф

```mermaid
quadrantChart
    title Importance and Complexity of Cinema App Features
    x-axis "Низкий приоритет" --> "Высокий приоритет"
    y-axis "Низкая сложность" --> "Высокая сложность"
    quadrant-1 "Реализовать немедленно"
    quadrant-2 "Планировать в ближайшее время"
    quadrant-3 "Возможно, стоит отказаться"
    quadrant-4 "Требует тщательного анализа"
    "Покупка билетов": [0.8, 0.9]
    "Бронирование мест": [0.7, 0.8]
    "Рейтинг фильмов": [0.4, 0.6]
    "Предзаказ закусок": [0.5, 0.7]
    "История сеансов": [0.3, 0.4]
    "Просмотр расписания фильмов": [0.9, 0.55]
    "Отзывы пользователей": [0.4, 0.3]
    "Вход в систему и настройки профиля": [0.6, 0.4]
```
### 4. Гит граф (Gitgraph)
```mermaid
gitGraph
   commit id: "Начало разработки"
   branch feature/authorization
   checkout feature/authorization
   commit id: "Реализована авторизация"
   checkout main
   merge feature/authorization
   branch feature/ticket_booking
   checkout feature/ticket_booking
   commit id: "Добавлена покупка билетов"
   commit id: "Реализовано бронирование мест"
   checkout main
   merge feature/ticket_booking
   branch feature/food_preorder
   checkout feature/food_preorder
   commit id: "Добавлен предзаказ закусок"
   checkout main
   merge feature/food_preorder
   branch feature/movies_schedule
   checkout feature/movies_schedule
   commit id: "Добавлено расписание фильмов"
   commit id: "Просмотр фильмов в прокате"
   checkout main
   merge feature/movies_schedule
   commit id: "Релиз первой версии"

```

# java-explore-with-me
Онлайн сервис для публикации событий и поиска участников
https://github.com/Sergey-Tel/java-explore-with-me/pull/6

### Стек
- Java 11
- Spring Boot
- Hibernate
- PostgreSQL
- Docker

### Приложение состоит из двух микросервисов:
- main-service - основной сервис для пользователей
- stats-service - вспомогательный сервис для сбора статистики

### Основные эндпоинты
#### публичное API
- /compilations - просмотр готовых подборок событий
- /categories - просмотр событий по категориям
- /events - просмотр событий по выбранным категориям и датам

#### пользовательское API
- /users/{userId}/events - GET просмотр событий пользователя
- /users/{userId}/events - POST создать новое событие
- /users/{userId}/requests - GET просмотр списка событий на которые подписан пользователь
- /users/{userId}/requests - POST подписаться на событий

#### API администратора
- /admin/users - GET просмотр списка пользователей
- /admin/users - POST зарегистрировать нового пользователя
- /admin/categories - POST создать новую категорию
- /admin/compilations - POST создать новую подборку

### Дополнительная функциональность
позволяет комментировать события
- /admin/comments - GET просмотр комментариев администратором
- /users/{userId}/comments - POST создание пользователем комментария
- /comments?eventId=xxx - GET просмотр комментариев к событию


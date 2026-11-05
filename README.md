# Вариант 22. Сравнение Job и Service

## Цель работы
Изучить различия между Job Container и Service Container в GitHub Actions.

## Сравнение

| Тип | Назначение | Пример |
|---|---|---|
| Job Container | Среда, в которой выполняются шаги Job | Python, Node.js |
| Service Container | Дополнительный сервис для выполнения задач | PostgreSQL, Redis |

## Job Container
Job Container используется для запуска команд и выполнения шагов Workflow внутри контейнера.

Пример:
```yaml
container:
  image: node:20
```

## Service Container
Service Container запускает вспомогательные сервисы, например базу данных PostgreSQL.

Пример:
```yaml
services:
  postgres:
    image: postgres:16
    env:
      POSTGRES_PASSWORD: demo_password
```

## Конфигурация Workflow
Workflow запускается при отправке изменений в репозиторий или вручную. В проекте используется PostgreSQL как Service Container.

## Результат
Создан Workflow GitHub Actions, демонстрирующий работу Job и Service Container.

## Вывод
Job Container предназначен для выполнения команд, а Service Container предоставляет дополнительные сервисы, необходимые для работы приложения.

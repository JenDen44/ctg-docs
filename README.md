# Coffee-to-go API Documentation

[![CI Status](https://github.com/JenDen44/ctg-docs/actions/workflows/openapi-ci.yml/badge.svg)](https://github.com/JenDen44/ctg-docs/actions)
[![GitHub Pages](https://img.shields.io/badge/docs-online-blue)](https://jenden44.github.io/ctg-docs/)

Документация API для сервиса Coffee-to-go в формате OpenAPI 3.1.


## Требования

- Node.js 20+
- Docker (для контейнеризации)
- Docker Compose (опционально)

## Установка и запуск

### 1. Установка зависимостей

Выполните:

```
npm install
```

После установки доступны команды:

```
npm run build  # Сборка документации
npm run lint   # Проверка спецификации
```

### 2. Локальный запуск

Для сборки и открытия документации:

```
npm run build && open dist/index.html
```

Для Linux:
```
npm run build && xdg-open dist/index.html
```

### 3. Запуск через Docker

```
docker-compose up --build -d
```

Документация будет доступна по адресу:
http://localhost:8080

## Основные команды

| Команда            | Действие                          |
|--------------------|-----------------------------------|
| `npm run build`    | Сборка документации               |
| `npm run lint`     | Проверка OpenAPI-спецификации     |
| `docker-compose up`| Запуск в Docker                   |

## Особенности реализации

- Генерация через Redocly CLI
- Модульная структура спецификации
- Production-сборка на nginx

## Лицензия

[MIT License](LICENSE)
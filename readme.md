# Docker — Базовые команды

## 1. Информация о Docker

```bash
docker --version          # Версия Docker
docker info               # Информация о Docker Engine
docker compose version    # Информация о Docker Compose
```

## 2. Работа с образами (Images)

```bash
docker pull image_name    # Скачивание образа
docker build -t name .    # Сборка образа из Dockerfile
docker images             # Список локальных образов
docker rmi image_name     # Удаление образа
docker system prune -a    # Очистка неиспользуемых образов и контейнеров
```

## 3. Работа с контейнерами (Containers)

```bash
docker run -it image_name                      # Запуск контейнера в интерактивном режиме
docker run -it --name my_container image_name  # Задать имя контейнеру
docker run -d -p 8080:80 image_name            # Запуск в фоне с пробросом порта
docker ps                                      # Список запущенных контейнеров
docker ps -a                                   # Все контейнеры (включая остановленные)
docker stop container_name                     # Остановка контейнера
docker start container_name                    # Запуск остановленного контейнера
docker restart container_name                  # Перезапуск контейнера
docker rm container_name                       # Удаление контейнера
docker exec -it container_name /bin/bash       # Подключение к работающему контейнеру
docker logs container_name                     # Просмотр логов контейнера
docker inspect container_name                  # Подробная информация о контейнере
```

## 4. Docker Compose

```bash
docker compose up --build -d    # Сборка и запуск всех сервисов в фоне
docker compose up               # Запуск сервисов в текущем терминале
docker compose build            # Только сборка образов
dicker compose down             # Остановка и удаление контейнеров, сетей
dicker compose down -v          # Остановка и удаление контейнеров, сетей, томов
docker compose logs             # Логи всех сервисов
docker compose logs -f service  # Логи конкретного сервиса в реальном времени
```

## 5. Работа с volume

```bash
docker volume ls            # Список volume
docker volume inspect name  # Информация о volume
docker volume rm name       # Удаление volume
```

## 6. Полезные команды

```bash
docker network ls                # Список сетей Docker
docker network inspect name      # Информация о сети
```

## 7. Очистка ресурсов

```bash
docker system prune               # Очистка остановленных контейнеров и неиспользуемых образов
docker system prune -a            # Полная очистка
docker container prune            # Удаление всех остановленных контейнеров
docker volume prune               # Удаление всех неиспользуемых volume
```

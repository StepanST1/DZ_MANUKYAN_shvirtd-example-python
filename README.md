# Практическое применение Docker (Занятие 5)

## Задача 0 — Проверка docker compose


`docker-compose --version` → command not found (удалён старый пакет)  
`docker compose version` → v2.x.x (или v5.0.2 на ВМ)
![version](img/Screenshot_1.png)

## Задача 1 — Dockerfile.python (multistage сборка)

Создан `Dockerfile.python` на базе `python:3.12-slim` с multistage-сборкой.  
Использованы `COPY . .` и `CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "5000"]`.  
Создан `.dockerignore` для исключения ненужных файлов.

Ссылка на форк [shvirtd-example-python](https://github.com/SavkinILYA/shvirtd-example-python)

Локальный запуск контейнера (без БД — ожидаемая ошибка подключения):

![ERROR](img/23.04.58.png)

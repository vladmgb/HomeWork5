# Решение к домашнему заданию к [занятию 5](https://github.com/netology-code/virtd-homeworks/tree/shvirtd-1/05-virt-04-docker-in-practice)

## Задача 1

Ссылка на [fork](https://github.com/vladmgb/shvirtd-example-python) 

## Задача 3

Cкриншот sql-запроса

![task3](https://github.com/user-attachments/assets/9b62bc3d-ff44-4e4e-9a14-86e9f279d9ad)

## Задача 4

Cкриншот sql-запроса

![task4](https://github.com/user-attachments/assets/9653513f-4804-4ae2-9d2c-2a8180e57bb8)

[Ссылка на репозиторий](https://github.com/vladmgb/shvirtd-example-python)

Bash скрипт
```bash
#!/bin/bash

#Рабочий каталог
TARGET_DIR="/opt/shvirtd-example-python"

#Обновляем или клонируем репозиторий
if [ -d "$TARGET_DIR" ]; then
  echo "Обновляем репозиторий..."
  cd "$TARGET_DIR" || exit
  git pull origin main
else
  echo "Клонируем репозиторий..."
  git clone https://github.com/vladmgb/shvirtd-example-python.git "$TARGET_DIR"
  cd "$TARGET_DIR" || exit
fi

#Запускаем проект
echo "Запускаем проект..."
cd "$TARGET_DIR" && /usr/libexec/docker/cli-plugins/docker-compose up --detach

#Проверяем статус
echo "Статус сервисов:"
/usr/libexec/docker/cli-plugins/docker-compose ps

#Получаем IP
PUBLIC_IP=$(curl -s ifconfig.me)
echo "Готово! Приложение доступно по адресу:"
echo "http://$PUBLIC_IP:8090"
```

## Задача 6

Используя dive и docker save

![task6 0_1](https://github.com/user-attachments/assets/40b4d573-01de-4393-8c01-cc50fc2db424)


![task6 0_2](https://github.com/user-attachments/assets/76f6cc32-adfc-44f3-90a5-177b5fb8b2fc)


## Задача 6.1

Используя docker cp

![task6 1](https://github.com/user-attachments/assets/69ed6af8-b08b-433f-a73b-d1f9a9b3ccc4)




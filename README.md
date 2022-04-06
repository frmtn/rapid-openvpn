# Чтобы развернуть OpenVPN сервер нужно выполнить:

1. Копируем проект
* git clone https://github.com/frmtn/rapid-openvpn.git

2. Создаем папку для конфигураций клинетов
*  cd rapid-openvpn && mkdir client_configs

3. Генерируем конфигурацию сервера
* make genconfig host=YOUR_SERVER_IP

4. Генерация сертификатов (PKI инфраструктуры)
* make initpki

5. Создание нового пользователя
* make new username=YOUR_USER

6. Запуск сервера
* make up


Далее копируем YOUR_USER.ovpn из client_configs/YOUR_USER.ovpn к себе в OpenVPN-клиент и пользуемся. 

## Добавление нового пользователя:
* make new username=YOUR_USER_2
Будет сгенирирован файл YOUR_USER_2.ovpn client_configs/YOUR_USER_2.ovpn

## Отзыв доступа к клиента:
* make revoke username=YOUR_USER

## Запуск VPN сервера
* make up

## Остановка VPN сервера 
* make stop

## Статус VPN сервера (контейнера)
* make ps

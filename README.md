# Теперь для того чтобы развернуть OpenVPN достаточно на сервере выполнить:

1. git clone https://github.com/frmtn/rapid-openvpn.git

2. cd rapid-openvpn && mkdir client_configs

3. make genconfig host=YOUR_SERVER_IP

4. make initpki

5. make new username=YOUR_USER

6. make up
Сервер будет запущен. Далее копируем YOUR_USER.ovpn из client_configs/YOUR_USER.ovpn к себе в OpenVPN-клиент и пользуемся. 


## Добавление нового пользователя:
make new username=YOUR_USER_2
Будет сгенирирован файл YOUR_USER_2.ovpn client_configs/YOUR_USER_2.ovpn

## Отзыв доступа к клиента:
make revoke username=YOUR_USER

## Запуск VPN сервера
make up

## Остановка VPN сервера 
make stop

## Статус VPN сервера (контейнера)
make ps

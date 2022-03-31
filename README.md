Теперь для того чтобы развернуть OpenVPN достаточно на сервере выполнить:

git clone https://github.com/frmtn/rapid-openvpn.git

cd rapid-openvpn/

make genconfig host=YOUR_SERVER_IP

make initpki

make new username=YOUR_USER

make up

Копируем example.ovpn из client_configs/example.ovpn к себе в OpenVPN-клиент и пользуемся

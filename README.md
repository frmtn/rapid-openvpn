Теперь для того чтобы развернуть OpenVPN достаточно на сервере выполнить:

git clone https://github.com/frmtn/rapid-openvpn.git
cd docker-compose-openvpn/
make genconfig host=vpn.example.com
make initpki
make new username=example
make up
Копируем example.ovpn из client_configs/example.ovpn к себе в OpenVPN-клиент и пользуемся
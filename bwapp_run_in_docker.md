#### В консоли (везде нужно sudo)
```
apt install -y  ca-certificates curl gnupg

install -m 0755 -d /etc/apt/keyrings

curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

chmod a+r /etc/apt/keyrings/docker.gpg

echo   "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/debian \
/etc/os-release && echo "$VERSION_CODENAME")" stable" |   sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

apt update 
apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

docker run -d -p 8080:80 --name bwapp raesene/bwapp
```
#### В браузере 
в адресной строке вбить
```127.0.0.1:8080/install.php```
нажать на install. Он отпишет что успешно установил. После этого можно нажать на Login
логин: bee
пароль: bug

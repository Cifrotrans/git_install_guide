https://only-to-top.ru/blog/tools/2019-12-08-git-ssh-windows.html?ysclid=leer3fw4ko184654651.

 [источник](https://www.google.com)
# 1. генерация ssh ключа
# 2. Добавление SSH ключа в SSH-agent
# 3. добавление  ключа у учетку гитхаб

_______________________________

* проверяем, что чтоит openSsh
* заходим в папку ssh
`cd ¬.ssh`

`ssh-keygen -t rsa -b 4096 -C "ваша@почта.com"`

Запускаем  ssh agent:

`eval `ssh-agent -s``

 добавляем закрытый ssh ключ :
`ssh-add ~/.ssh/id_rsa`

выводим в консоль публичный ключ, копируем
`cat ~/.ssh/id_rsa.pub`
добавляем публичный ключ в учетку гита
https://github.com/settings/keys

Обрати внимание на 
1. куда пушишь -  https || ssh
2. какую ветку пушишь. там то мэйн, то мастер - следи.
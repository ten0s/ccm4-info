## Содержание

- [Установка Wine](#установка-wine)
- [Установка КриптоПро](#установка-криптопро)
- [Установка Менеджера Конфигурации](#установка-менеджера-конфигурации)

## Ubuntu

### Установка Wine

Установить Wine как описано здесь https://wiki.winehq.org/Ubuntu

Пример минимально необходимой установки для Ubuntu 22.04


```
$ sudo dpkg --add-architecture i386
```

```
$ sudo mkdir -p -m755 /etc/apt/keyrings
$ sudo wget -O /etc/apt/keyrings/winehq-archive.key https://dl.winehq.org/wine-builds/winehq.key
$ sudo wget -NP /etc/apt/sources.list.d/ https://dl.winehq.org/wine-builds/ubuntu/dists/jammy/winehq-jammy.sources
```

```
$ sudo apt update
$ sudo apt install --install-recommends winehq-stable
```

```
$ wine --version
wine-9.0
```

### Установка КриптоПро

Скачать сертифицированную версию КриптоПро CSP 5.0 R2<br>
https://cryptopro.ru/sites/default/files/private/csp/50/12000/linux-amd64_deb.tgz

```
$ tar xf linux-amd64_deb.tgz
$ cd linux-amd64_deb/
```

```
$ sudo ./install_gui.sh
```

Установить следующие обязательные компоненты:

```
[*] KC1 Cryptographic Service Provider
[*] GUI dialogs component
[*] cptools, GUI application for various tasks
```

Проверить установку:

```
$ /opt/cprocsp/bin/amd64/cryptcp -help | head -1
CryptCP 5.0 (c) "Crypto-Pro", 2002-2021.
```

### Установка Менеджера Конфигурации

```
$ sh ccm-4.1.9.2585-install.run --target ~/CCM
```

Если установка прошла без ошибок на рабочем столе должны появиться два ярлыка:
* Континент 4. Менеджер Конфигурации
* Менеджер Сертификатов (Wine + КриптоПро)

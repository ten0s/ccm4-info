## Содержание

- [Установка Wine](#установка-wine)
- [Установка КриптоПро](#установка-криптопро)
- [Установка Менеджера Конфигурации](#установка-менеджера-конфигурации)

## Astra Linux

### Установка Wine

Установить Wine как описано здесь https://wiki.astralinux.ru/pages/viewpage.action?pageid=27362502

Пример минимально необходимой установки для Astra Linux Special Edition 1.7.3


Подключить базовый и расширенный репозитории пакетов

```
$ cat /etc/apt/sources.list
...
deb https://download.astralinux.ru/astra/stable/1.7_x86-64/repository-main/ 1.7_x86-64 main contrib non-free
deb https://download.astralinux.ru/astra/stable/1.7_x86-64/repository-update/ 1.7_x86-64 main contrib non-free

deb https://download.astralinux.ru/astra/stable/1.7_x86-64/repository-base/ 1.7_x86-64 main contrib non-free
deb https://download.astralinux.ru/astra/stable/1.7_x86-64/repository-extended/ 1.7_x86-64 main contrib non-free
...
```

```
$ sudo apt update
$ sudo apt dist-upgrade
```

Установить Wine

```
$ sudo apt install wine ia32-libs
```

```
$ wine --version
wine-8.0.1
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
[*] Криптопровайдер KC1
[*] Графические диалоги
[*] cptools, многоцелевое графическое приложение
```

Проверить установку:

```
$ /opt/cprocsp/bin/amd64/cryptcp -help | head -1
CryptCP 5.0 (c) "КРИПТО-ПРО", 2002-2021.
```

### Установка Менеджера Конфигурации

```
$ sh ccm4.run --target ~/CCM
```

Если установка прошла без ошибок на рабочем столе должны появиться два ярлыка:
* Континент 4. Менеджер Конфигурации
* Менеджер Сертификатов (Wine + КриптоПро)

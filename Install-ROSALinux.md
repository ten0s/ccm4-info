## Содержание

- [Установка Wine](#установка-wine)
- [Установка КриптоПро](#установка-криптопро)
- [Установка Менеджера Конфигурации](#установка-менеджера-конфигурации)

## ROSA Linux

### Установка Wine

Пример минимально необходимой установки для ROSA Linux 12.5

```
$ sudo yum update
```

Установить Wine

```
$ sudo yum install wine64-stable
```

```
$ wine --version
wine-8.0.2
```

### Установка КриптоПро

Скачать сертифицированную версию КриптоПро CSP 5.0 R2<br>
https://cryptopro.ru/sites/default/files/private/csp/50/12000/linux-amd64.tgz

```
$ tar xf linux-amd64.tgz
$ cd linux-amd64/
```

```
$ sudo yum install lsb-core newt
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
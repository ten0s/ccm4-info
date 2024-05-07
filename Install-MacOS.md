## Содержание

- [Установка Wine](#установка-wine)
- [Установка КриптоПро](#установка-криптопро)
- [Установка Менеджера Конфигурации](#установка-менеджера-конфигурации)

## MacOS

### Установка Wine

Следующие команды предполагают, что установлен [Homebrew](https://brew.sh/).

Пример минимально необходимой установки для MacOS.

```
% brew tap homebrew/cask-versions
```

```
% brew install --cask --no-quarantine wine-stable
```

```
% wine64 --version
wine-8.0.1
```

### Установка КриптоПро

Cертифицированная версия КриптоПро CSP 5.0 R2<br>
https://cryptopro.ru/sites/default/files/private/csp/50/12000/macos-uni.tgz
не устанавливается из-за блокировки Apple.

Скачать и установить версию отсюда<br>
https://support.cryptopro.ru/index.php?/Knowledgebase/Article/View/455/8/ustnovk-kriptopro-csp-n-macos-posle-blokirovki

Проверить установку:

```
% /opt/cprocsp/bin/cryptcp -help | head -1
CryptCP 5.0 (c) "Crypto-Pro", 2002-2024.
```

### Установка Менеджера Конфигурации

```
% sh ccm-4.1.9.2585-install.run --target $HOME/CCM
```

Если установка прошла без ошибок на рабочем столе должны появиться два ярлыка:
* ССC - Континент 4. Менеджер Конфигурации
* CertMan - Менеджер Сертификатов (Wine + КриптоПро)

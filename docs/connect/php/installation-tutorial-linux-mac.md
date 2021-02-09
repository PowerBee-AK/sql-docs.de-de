---
title: Linux- und macOS-Installation für die Treiber für PHP
description: In diesen Anweisungen erfahren Sie, wie Sie die Microsoft-Treiber für PHP für SQL Server für Linux oder macOS installieren.
ms.date: 01/29/2021
ms.prod: sql
ms.prod_service: connectivity
ms.custom: ''
ms.technology: connectivity
ms.topic: conceptual
author: David-Engel
ms.author: v-daenge
manager: v-mabarw
ms.openlocfilehash: dfb8494912ae2f11590ec8a8b679f0f23064f930
ms.sourcegitcommit: f30b5f61c514437ea58acc5769359c33255b85b5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2021
ms.locfileid: "99076452"
---
# <a name="linux-and-macos-installation-tutorial-for-the-microsoft-drivers-for-php-for-sql-server"></a>Tutorial zur Linux- und macOS-Installation für die Microsoft-Treiber für PHP für SQL Server
Die folgende Anleitung setzt eine bereinigte Umgebung voraus und zeigt, wie PHP 8.0, der Microsoft ODBC-Treiber, der Apache-Webserver und die Microsoft-Treiber für PHP für SQL Server unter Ubuntu 16.04, 18.04 und 20.04, Red Hat 7 und 8, Debian 9 und 10, SUSE 12 und 15, Alpine 3.11 und 3.12 sowie macOS 10.14, 10.15 und 11.0 installiert werden. In dieser Anleitung wird empfohlen, die Treiber mit PECL zu installieren, aber Sie können auch die vorab erstellten Binärdateien von der GitHub-Projektseite [Microsoft Drivers for PHP for SQL Server](https://github.com/Microsoft/msphpsql/releases) (Microsoft-Treiber für PHP für SQL Server) herunterladen und gemäß den Anweisungen unter [Laden der Microsoft-Treiber für PHP für SQL Server](../../connect/php/loading-the-php-sql-driver.md) installieren. Eine Beschreibung des Ladevorgangs von Erweiterungen und die Gründe, warum die Erweiterungen nicht zur php.ini-Datei hinzugefügt werden, finden Sie im Abschnitt zum [Laden der Treiber](../../connect/php/loading-the-php-sql-driver.md#loading-the-driver-at-php-startup).

In der folgenden Anleitung wird gezeigt, wie Sie PHP 8.0 standardmäßig mit `pecl install` installieren, wenn die PHP 8.0-Pakete verfügbar sind. Möglicherweise müssen Sie zuerst `pecl channel-update pecl.php.net` ausführen. In einige unterstützte Linux-Distributionen ist standardmäßig PHP 7.1 oder niedriger integriert. Dies wird für die neuste Version der PHP-Treiber für SQL Server nicht unterstützt. Lesen Sie sich die Hinweise am Anfang der einzelnen Abschnitte durch, um zu erfahren, wie Sie stattdessen PHP 7.4 oder 7.3 installieren.

In dieser Anleitung sind auch Anweisungen zum Installieren von PHP FastCGI Process Manager (PHP-FPM) unter Ubuntu enthalten. Dieser ist bei Verwendung des nginx-Webservers anstelle von Apache erforderlich.

Diese Anweisungen enthalten zwar Befehle zum Installieren von SQLSRV- und PDO_SQLSRV-Treibern, die Treiber können jedoch unabhängig installiert und funktionsfähig sein. Benutzer, die mit der Anpassung Ihrer Konfiguration vertraut sind, können diese Anweisungen SQLSRV- oder PDO_SQLSRV-spezifisch anpassen. Die Abhängigkeiten beider Treiber sind abgesehen von den unten angegebenen Ausnahmen identisch.

## <a name="contents-of-this-page"></a>Inhalt dieser Seite

- [Installieren der Treiber unter Ubuntu 16.04, 18.04 und 20.04](#installing-the-drivers-on-ubuntu-1604-1804-and-2004)
- [Installieren der Treiber mit PHP-FPM unter Ubuntu](#installing-the-drivers-with-php-fpm-on-ubuntu)
- [Installieren der Treiber unter Red Hat 7 und 8](#installing-the-drivers-on-red-hat-7-and-8)
- [Installieren der Treiber unter Debian 9 und 10](#installing-the-drivers-on-debian-9-and-10)
- [Installieren der Treiber unter Suse 12 und 15](#installing-the-drivers-on-suse-12-and-15)
- [Installieren der Treiber unter Alpine 3.11 und 3.12](#installing-the-drivers-on-alpine-311-and-312)
- [Installieren der Treiber unter macOS Mojave, Catalina und Big Sur](#installing-the-drivers-on-macos-mojave-catalina-and-big-sur)

## <a name="installing-the-drivers-on-ubuntu-1604-1804-and-2004"></a>Installieren der Treiber unter Ubuntu 16.04, 18.04 und 20.04

> [!NOTE]
> Ersetzen Sie die Versionsnummer 8.0 in den folgenden Befehlen durch 7.4 oder 7.3, um PHP 7.4 bzw. 7.3 zu installieren.

### <a name="step-1-install-php"></a>Schritt 1: Installieren von PHP
```bash
sudo su
add-apt-repository ppa:ondrej/php -y
apt-get update
apt-get install php8.0 php8.0-dev php8.0-xml -y --allow-unauthenticated
```
### <a name="step-2-install-prerequisites"></a>Schritt 2: Installieren der erforderlichen Komponenten
Installieren Sie den ODBC-Treiber für Ubuntu, indem Sie die Anleitung auf der Seite zur [Installation des Microsoft ODBC Driver for SQL Server (Linux)](../../connect/odbc/linux-mac/installing-the-microsoft-odbc-driver-for-sql-server.md) befolgen.

### <a name="step-3-install-the-php-drivers-for-microsoft-sql-server"></a>Schritt 3: Installieren der PHP-Treiber für Microsoft SQL Server
```bash
sudo pecl install sqlsrv
sudo pecl install pdo_sqlsrv
sudo su
printf "; priority=20\nextension=sqlsrv.so\n" > /etc/php/8.0/mods-available/sqlsrv.ini
printf "; priority=30\nextension=pdo_sqlsrv.so\n" > /etc/php/8.0/mods-available/pdo_sqlsrv.ini
exit
sudo phpenmod -v 8.0 sqlsrv pdo_sqlsrv
```

Wenn nur eine PHP-Version im System vorhanden ist, kann der letzte Schritt zu `phpenmod sqlsrv pdo_sqlsrv` vereinfacht werden.

### <a name="step-4-install-apache-and-configure-driver-loading"></a>Schritt 4. Installieren von Apache und Konfigurieren des Treiberladevorgangs
```bash
sudo su
apt-get install libapache2-mod-php8.0 apache2
a2dismod mpm_event
a2enmod mpm_prefork
a2enmod php8.0
exit
```
### <a name="step-5-restart-apache-and-test-the-sample-script"></a>Schritt 5: Neustarten von Apache und Testen des Beispielskripts
```bash
sudo service apache2 restart
```
Hinweise zum [Testen der Installation](#testing-your-installation) finden Sie am Ende dieses Dokuments.

## <a name="installing-the-drivers-with-php-fpm-on-ubuntu"></a>Installieren der Treiber mit PHP-FPM unter Ubuntu

> [!NOTE]
> Ersetzen Sie die Versionsnummer 8.0 in den folgenden Befehlen durch 7.4 oder 7.3, um PHP 7.4 bzw. 7.3 zu installieren.

### <a name="step-1-install-php"></a>Schritt 1: Installieren von PHP
```bash
sudo su
add-apt-repository ppa:ondrej/php -y
apt-get update
apt-get install php8.0 php8.0-dev php8.0-fpm php8.0-xml -y --allow-unauthenticated
```
Überprüfen des Status des PHP-FPM-Diensts durch Ausführen von
```bash
systemctl status php8.0-fpm
```
### <a name="step-2-install-prerequisites"></a>Schritt 2: Installieren der erforderlichen Komponenten
Installieren Sie den ODBC-Treiber für Ubuntu, indem Sie die Anleitung auf der Seite zur [Installation des Microsoft ODBC Driver for SQL Server (Linux)](../../connect/odbc/linux-mac/installing-the-microsoft-odbc-driver-for-sql-server.md) befolgen.

### <a name="step-3-install-the-php-drivers-for-microsoft-sql-server"></a>Schritt 3: Installieren der PHP-Treiber für Microsoft SQL Server
```bash
sudo pecl config-set php_ini /etc/php/8.0/fpm/php.ini
sudo pecl install sqlsrv
sudo pecl install pdo_sqlsrv
sudo su
printf "; priority=20\nextension=sqlsrv.so\n" > /etc/php/8.0/mods-available/sqlsrv.ini
printf "; priority=30\nextension=pdo_sqlsrv.so\n" > /etc/php/8.0/mods-available/pdo_sqlsrv.ini
exit
sudo phpenmod -v 8.0 sqlsrv pdo_sqlsrv
```
Wenn nur eine PHP-Version im System vorhanden ist, kann der letzte Schritt zu `phpenmod sqlsrv pdo_sqlsrv` vereinfacht werden.

Überprüfen Sie, ob `sqlsrv.ini` und `pdo_sqlsrv.ini` sich in `/etc/php/8.0/fpm/conf.d/` befinden:
```bash
ls /etc/php/8.0/fpm/conf.d/*sqlsrv.ini
```
Starten Sie den PHP-FPM-Dienst neu:
```bash
sudo systemctl restart php8.0-fpm
```

### <a name="step-4-install-and-configure-nginx"></a>Schritt 4. Installieren und Konfigurieren von nginx
```bash
sudo apt-get update
sudo apt-get install nginx
sudo systemctl status nginx
```
Zum Konfigurieren von nginx müssen Sie die Datei `/etc/nginx/sites-available/default` bearbeiten. Fügen Sie `index.php` zu der Liste unterhalb des Abschnitts `# Add index.php to the list if you are using PHP` hinzu:
```
# Add index.php to the list if you are using PHP
index index.html index.htm index.nginx-debian.html index.php;
```
Heben Sie als Nächstes die Auskommentierung auf, und ändern Sie den auf `# pass PHP scripts to FastCGI server` folgenden Abschnitt wie folgt:
```
# pass PHP scripts to FastCGI server
#
location ~ \.php$ {
        include snippets/fastcgi-php.conf;
        fastcgi_pass unix:/run/php/php8.0-fpm.sock;
}
```
### <a name="step-5-restart-nginx-and-test-the-sample-script"></a>Schritt 5: Neustarten von nginx und Testen des Beispielskripts
```bash
sudo systemctl restart nginx.service
```
Hinweise zum [Testen der Installation](#testing-your-installation) finden Sie am Ende dieses Dokuments.

## <a name="installing-the-drivers-on-red-hat-7-and-8"></a>Installieren der Treiber unter Red Hat 7 und 8

### <a name="step-1-install-php"></a>Schritt 1: Installieren von PHP

Führen Sie zum Installieren von PHP unter Red Hat 7 Folgendes aus:
> [!NOTE]
> Ersetzen Sie die Zeichenfolge „remi-php80“ in den folgenden Befehlen durch „remi-php74“ oder „remi-php73“, um PHP 7.4 bzw. 7.3 zu installieren.
```bash
sudo su
yum install https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
yum install https://rpms.remirepo.net/enterprise/remi-release-7.rpm
subscription-manager repos --enable=rhel-7-server-optional-rpms
yum install yum-utils
yum-config-manager --enable remi-php80
yum update
# Note: The php-pdo package is required only for the PDO_SQLSRV driver
yum install php php-pdo php-xml php-pear php-devel re2c gcc-c++ gcc
```

Führen Sie zum Installieren von PHP unter Red Hat 8 Folgendes aus:
> [!NOTE]
> Ersetzen Sie die Zeichenfolge „remi-8.0“ in den folgenden Befehlen durch „remi-7.4“ oder „remi-7.3“, um PHP 7.4 bzw. 7.3 zu installieren.
```bash
sudo su
dnf install https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm
dnf install https://rpms.remirepo.net/enterprise/remi-release-8.rpm
dnf install yum-utils
dnf module reset php
dnf module install php:remi-8.0
subscription-manager repos --enable codeready-builder-for-rhel-8-x86_64-rpms
dnf update
# Note: The php-pdo package is required only for the PDO_SQLSRV driver
dnf install php-pdo php-pear php-devel
```

### <a name="step-2-install-prerequisites"></a>Schritt 2: Installieren der erforderlichen Komponenten
Installieren Sie den ODBC-Treiber für Red Hat 7 oder 8, indem Sie die Anleitung auf der Seite zur [Installation des Microsoft ODBC Driver for SQL Server (Linux)](../../connect/odbc/linux-mac/installing-the-microsoft-odbc-driver-for-sql-server.md) befolgen.

### <a name="step-3-install-the-php-drivers-for-microsoft-sql-server"></a>Schritt 3: Installieren der PHP-Treiber für Microsoft SQL Server
```bash
sudo pecl install sqlsrv
sudo pecl install pdo_sqlsrv
sudo su
echo extension=pdo_sqlsrv.so >> `php --ini | grep "Scan for additional .ini files" | sed -e "s|.*:\s*||"`/30-pdo_sqlsrv.ini
echo extension=sqlsrv.so >> `php --ini | grep "Scan for additional .ini files" | sed -e "s|.*:\s*||"`/20-sqlsrv.ini
exit
```

Alternativ dazu können Sie die Treiber auch aus dem Remi-Repository installieren:
```bash
sudo yum install php-sqlsrv
```
### <a name="step-4-install-apache"></a>Schritt 4. Installieren von Apache
```bash
sudo yum install httpd
```
SELinux wird standardmäßig installiert und im Modus „Erzwingen“ ausgeführt. Damit Apache über SELinux eine Verbindung mit Datenbanken herstellen kann, führen Sie den folgenden Befehl aus:
```bash
sudo setsebool -P httpd_can_network_connect_db 1
```
### <a name="step-5-restart-apache-and-test-the-sample-script"></a>Schritt 5: Neustarten von Apache und Testen des Beispielskripts
```bash
sudo apachectl restart
```
Hinweise zum [Testen der Installation](#testing-your-installation) finden Sie am Ende dieses Dokuments.

## <a name="installing-the-drivers-on-debian-9-and-10"></a>Installieren der Treiber unter Debian 9 und 10

> [!NOTE]
> Ersetzen Sie die Versionsnummer 8.0 in den folgenden Befehlen durch 7.4 oder 7.3, um PHP 7.4 bzw. 7.3 zu installieren.

### <a name="step-1-install-php"></a>Schritt 1: Installieren von PHP
```bash
sudo su
apt-get install curl apt-transport-https
wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg
echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list
apt-get update
apt-get install -y php8.0 php8.0-dev php8.0-xml php8.0-intl
```
### <a name="step-2-install-prerequisites"></a>Schritt 2: Installieren der erforderlichen Komponenten
Installieren Sie den ODBC-Treiber für Debian, indem Sie die Anleitung auf der Seite zur [Installation des Microsoft ODBC Driver for SQL Server (Linux)](../../connect/odbc/linux-mac/installing-the-microsoft-odbc-driver-for-sql-server.md) befolgen. 

Möglicherweise müssen Sie auch das richtige Gebietsschema generieren, damit die PHP-Ausgabe in einem Browser korrekt angezeigt wird. Führen Sie zum Beispiel für das Gebietsschema „en_US UTF-8“ die folgenden Befehle aus:
```bash
sudo su
sed -i 's/# en_US.UTF-8 UTF-8/en_US.UTF-8 UTF-8/g' /etc/locale.gen
locale-gen
```
Möglicherweise müssen Sie `/usr/sbin` zu `$PATH` hinzufügen, da sich die ausführbare Datei `locale-gen` dort befindet.

### <a name="step-3-install-the-php-drivers-for-microsoft-sql-server"></a>Schritt 3: Installieren der PHP-Treiber für Microsoft SQL Server
```bash
sudo pecl install sqlsrv
sudo pecl install pdo_sqlsrv
sudo su
printf "; priority=20\nextension=sqlsrv.so\n" > /etc/php/8.0/mods-available/sqlsrv.ini
printf "; priority=30\nextension=pdo_sqlsrv.so\n" > /etc/php/8.0/mods-available/pdo_sqlsrv.ini
exit
sudo phpenmod -v 8.0 sqlsrv pdo_sqlsrv
```

Wenn nur eine PHP-Version im System vorhanden ist, kann der letzte Schritt zu `phpenmod sqlsrv pdo_sqlsrv` vereinfacht werden. Ebenso wie `locale-gen` befindet sich auch `phpenmod` in `/usr/sbin`, daher müssen Sie dieses Verzeichnis möglicherweise zu `$PATH` hinzufügen.

### <a name="step-4-install-apache-and-configure-driver-loading"></a>Schritt 4. Installieren von Apache und Konfigurieren des Treiberladevorgangs
```bash
sudo su
apt-get install libapache2-mod-php8.0 apache2
a2dismod mpm_event
a2enmod mpm_prefork
a2enmod php8.0
```
### <a name="step-5-restart-apache-and-test-the-sample-script"></a>Schritt 5: Neustarten von Apache und Testen des Beispielskripts
```bash
sudo service apache2 restart
```
Hinweise zum [Testen der Installation](#testing-your-installation) finden Sie am Ende dieses Dokuments.

## <a name="installing-the-drivers-on-suse-12-and-15"></a>Installieren der Treiber unter Suse 12 und 15

> [!NOTE]
> Ersetzen Sie `<SuseVersion>` in der folgenden Anleitung durch Ihre SUSE-Version. Wenn Sie SUSE Enterprise Linux 15 verwenden, lautet der Wert SLE_15_SP1 oder SLE_15_SP2. Verwenden Sie SLE_12_SP4 (oder höher, sofern zutreffend) für SUSE 12. Nicht alle Versionen von PHP sind für alle Versionen von SUSE Linux verfügbar. Unter `http://download.opensuse.org/repositories/devel:/languages:/php` erfahren Sie, welche Versionen von SUSE über die Standardversion von PHP verfügen, und unter `http://download.opensuse.org/repositories/devel:/languages:/php:/`, welche anderen Versionen von PHP für welche Versionen von SUSE verfügbar sind.

> [!NOTE]
> Pakete für PHP 7.4 oder höher sind für SUSE 12 nicht verfügbar, und das Paket für PHP 8.0 ist für SUSE 15 noch nicht verfügbar.
> Zum Installieren von PHP 7.3 ersetzen Sie die unten gezeigte Repository-URL durch folgende URL: `https://download.opensuse.org/repositories/devel:/languages:/php:/php73/<SuseVersion>/devel:languages:php:php73.repo`.

### <a name="step-1-install-php"></a>Schritt 1: Installieren von PHP
```bash
sudo su
zypper -n ar -f https://download.opensuse.org/repositories/devel:languages:php/<SuseVersion>/devel:languages:php.repo
zypper --gpg-auto-import-keys refresh
zypper -n install php7 php7-devel php7-openssl
```
### <a name="step-2-install-prerequisites"></a>Schritt 2: Installieren der erforderlichen Komponenten
Installieren Sie den ODBC-Treiber für SUSE, indem Sie die Anleitung auf der Seite zur [Installation des Microsoft ODBC Driver for SQL Server (Linux)](../../connect/odbc/linux-mac/installing-the-microsoft-odbc-driver-for-sql-server.md) befolgen.

### <a name="step-3-install-the-php-drivers-for-microsoft-sql-server"></a>Schritt 3: Installieren der PHP-Treiber für Microsoft SQL Server
> [!NOTE]
> Wenn die Fehlermeldung „`Connection to 'pecl.php.net:443' failed: Unable to find the socket transport "ssl"`“ angezeigt wird, bearbeiten Sie das pecl-Skript unter /usr/bin/pecl und entfernen in der letzten Zeile den Parameter `-n`. Dieser Parameter verhindert, dass PECL beim Aufruf von PHP INI-Dateien lädt, wodurch das Laden der OpenSSL-Erweiterung verhindert wird.

```bash
sudo pecl install sqlsrv
sudo pecl install pdo_sqlsrv
sudo su
echo extension=pdo_sqlsrv.so >> `php --ini | grep "Scan for additional .ini files" | sed -e "s|.*:\s*||"`/pdo_sqlsrv.ini
echo extension=sqlsrv.so >> `php --ini | grep "Scan for additional .ini files" | sed -e "s|.*:\s*||"`/sqlsrv.ini
exit
```
### <a name="step-4-install-apache-and-configure-driver-loading"></a>Schritt 4. Installieren von Apache und Konfigurieren des Treiberladevorgangs
```bash
sudo su
zypper install apache2 apache2-mod_php7
a2enmod php7
echo "extension=sqlsrv.so" >> /etc/php7/apache2/php.ini
echo "extension=pdo_sqlsrv.so" >> /etc/php7/apache2/php.ini
exit
```
### <a name="step-5-restart-apache-and-test-the-sample-script"></a>Schritt 5: Neustarten von Apache und Testen des Beispielskripts
```bash
sudo systemctl restart apache2
```
Hinweise zum [Testen der Installation](#testing-your-installation) finden Sie am Ende dieses Dokuments.

## <a name="installing-the-drivers-on-alpine-311-and-312"></a>Installieren der Treiber unter Alpine 3.11 und 3.12

> [!NOTE]
> Die Standardversion von PHP ist 7.3. PHP 7.4 oder höher ist möglicherweise über Test- oder Edgerepositorys für Alpine verfügbar. Sie können PHP stattdessen aus der Quelle kompilieren.

### <a name="step-1-install-php"></a>Schritt 1: Installieren von PHP
PHP-Pakete für Alpine finden Sie im `edge/community`-Repository. Aktivieren Sie auf der Wiki-Seite die Option [Enable Community Repository](https://wiki.alpinelinux.org/wiki/Enable_Community_Repository) (Communityrepository aktivieren). Fügen Sie folgende Zeile zu `/etc/apk/repositories` hinzu, und ersetzen Sie dabei `<mirror>` durch die URL eines Alpine-Repositoryspiegels:
```bash
http://<mirror>/alpine/edge/community
```
Führen Sie dann Folgendes aus:
```bash
sudo su
apk update
# Note: The php7-pdo package is required only for the PDO_SQLSRV driver
apk add php7 php7-dev php7-pear php7-pdo php7-openssl autoconf make g++
```
### <a name="step-2-install-prerequisites"></a>Schritt 2: Installieren der erforderlichen Komponenten
Installieren Sie den ODBC-Treiber für Alpine, indem Sie die Anleitung auf der Seite zur [Installation des Microsoft ODBC Driver for SQL Server (Linux)](../../connect/odbc/linux-mac/installing-the-microsoft-odbc-driver-for-sql-server.md) befolgen. 

### <a name="step-3-install-the-php-drivers-for-microsoft-sql-server"></a>Schritt 3: Installieren der PHP-Treiber für Microsoft SQL Server
```bash
sudo pecl install sqlsrv
sudo pecl install pdo_sqlsrv
sudo su
echo extension=pdo_sqlsrv.so >> `php --ini | grep "Scan for additional .ini files" | sed -e "s|.*:\s*||"`/10_pdo_sqlsrv.ini
echo extension=sqlsrv.so >> `php --ini | grep "Scan for additional .ini files" | sed -e "s|.*:\s*||"`/00_sqlsrv.ini
```

### <a name="step-4-install-apache-and-configure-driver-loading"></a>Schritt 4. Installieren von Apache und Konfigurieren des Treiberladevorgangs
```bash
sudo apk add php7-apache2 apache2
```
### <a name="step-5-restart-apache-and-test-the-sample-script"></a>Schritt 5: Neustarten von Apache und Testen des Beispielskripts
```bash
sudo rc-service apache2 restart
```
Hinweise zum [Testen der Installation](#testing-your-installation) finden Sie am Ende dieses Dokuments.


## <a name="installing-the-drivers-on-macos-mojave-catalina-and-big-sur"></a>Installieren der Treiber unter macOS Mojave, Catalina und Big Sur

Falls noch nicht vorhanden, installieren Sie Brew wie folgt:
```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

> [!NOTE]
> Ersetzen Sie php@8.0 in den folgenden Befehlen durch php@7.4 oder php@7.3, um PHP 7.4 bzw. 7.3 zu installieren.

### <a name="step-1-install-php"></a>Schritt 1: Installieren von PHP

```bash
brew tap
brew tap homebrew/core
brew install php@8.0
```
PHP sollte sich nun unter Ihrem Pfad befinden. Führen Sie `php -v` aus, um zu überprüfen, ob Sie die richtige PHP-Version verwenden. Falls PHP nicht in dem Pfad zu finden ist oder nicht die richtige Version aufweist, führen Sie Folgendes aus:
```bash
brew link --force --overwrite php@8.0
```

### <a name="step-2-install-prerequisites"></a>Schritt 2: Installieren der erforderlichen Komponenten
Installieren Sie den ODBC-Treiber für macOS, indem Sie die Anleitung auf der Seite zur [Installation des Microsoft ODBC Driver for SQL Server (macOS)](../../connect/odbc/linux-mac/install-microsoft-odbc-driver-sql-server-macos.md) befolgen. 

Darüber hinaus kann es erforderlich sein, die GNU-Erstellungstools zu installieren:
```bash
brew install autoconf automake libtool
```

### <a name="step-3-install-the-php-drivers-for-microsoft-sql-server"></a>Schritt 3: Installieren der PHP-Treiber für Microsoft SQL Server
```bash
sudo pecl install sqlsrv
sudo pecl install pdo_sqlsrv
```
### <a name="step-4-install-apache-and-configure-driver-loading"></a>Schritt 4. Installieren von Apache und Konfigurieren des Treiberladevorgangs
```bash
brew install apache2
```
Führen Sie folgenden Befehl aus, um nach der Apache-Konfigurationsdatei (`httpd.conf`) für Ihre Apache-Installation zu suchen: 
```bash
/usr/local/bin/apachectl -V | grep SERVER_CONFIG_FILE
``` 
Mit den folgenden Befehlen wird die erforderliche Konfiguration an `httpd.conf` angefügt. Stellen Sie sicher, dass Sie den vom vorherigen Befehl zurückgegebenen Pfad durch `/usr/local/etc/httpd/httpd.conf` ersetzen:
```bash
echo "LoadModule php7_module /usr/local/opt/php@8.0/lib/httpd/modules/libphp7.so" >> /usr/local/etc/httpd/httpd.conf
(echo "<FilesMatch .php$>"; echo "SetHandler application/x-httpd-php"; echo "</FilesMatch>";) >> /usr/local/etc/httpd/httpd.conf
```
### <a name="step-5-restart-apache-and-test-the-sample-script"></a>Schritt 5: Neustarten von Apache und Testen des Beispielskripts
```bash
sudo apachectl restart
```
Hinweise zum [Testen der Installation](#testing-your-installation) finden Sie am Ende dieses Dokuments.

## <a name="testing-your-installation"></a>Testen der Installation

Wenn Sie dieses Beispielskript testen möchten, erstellen Sie eine Datei namens „testsql.php“ im Dokumentenstamm Ihres Systems. Unter Ubuntu, Debian und Red Hat ist dies `/var/www/html/`, unter SUSE `/srv/www/htdocs`, unter Alpine `/var/www/localhost/htdocs` und unter macOS `/usr/local/var/www`. Kopieren Sie folgendes Skript und fügen Sie es dort ein, indem Sie ggf. Server, Datenbank, Benutzername und Kennwort ersetzen.

### <a name="sqlsrv-example"></a>SQLSRV-Beispiel

```php
<?php
$serverName = "yourServername";
$connectionOptions = array(
    "database" => "yourDatabase",
    "uid" => "yourUsername",
    "pwd" => "yourPassword"
);

function exception_handler($exception) {
    echo "<h1>Failure</h1>";
    echo "Uncaught exception: " , $exception->getMessage();
    echo "<h1>PHP Info for troubleshooting</h1>";
    phpinfo();
}

set_exception_handler('exception_handler');

// Establishes the connection
$conn = sqlsrv_connect($serverName, $connectionOptions);
if ($conn === false) {
    die(formatErrors(sqlsrv_errors()));
}

// Select Query
$tsql = "SELECT @@Version AS SQL_VERSION";

// Executes the query
$stmt = sqlsrv_query($conn, $tsql);

// Error handling
if ($stmt === false) {
    die(formatErrors(sqlsrv_errors()));
}
?>

<h1> Success Results : </h1>

<?php
while ($row = sqlsrv_fetch_array($stmt, SQLSRV_FETCH_ASSOC)) {
    echo $row['SQL_VERSION'] . PHP_EOL;
}

sqlsrv_free_stmt($stmt);
sqlsrv_close($conn);

function formatErrors($errors)
{
    // Display errors
    echo "<h1>SQL Error:</h1>";
    echo "Error information: <br/>";
    foreach ($errors as $error) {
        echo "SQLSTATE: ". $error['SQLSTATE'] . "<br/>";
        echo "Code: ". $error['code'] . "<br/>";
        echo "Message: ". $error['message'] . "<br/>";
    }
}
?>
```

### <a name="pdo_sqlsrv-example"></a>PDO_SQLSRV-Beispiel

```php
<?php
try {
    $serverName = "yourServername";
    $databaseName = "yourDatabase";
    $uid = "yourUsername";
    $pwd = "yourPassword";
    
    $conn = new PDO("sqlsrv:server = $serverName; Database = $databaseName;", $uid, $pwd);

    // Select Query
    $tsql = "SELECT @@Version AS SQL_VERSION";

    // Executes the query
    $stmt = $conn->query($tsql);
} catch (PDOException $exception1) {
    echo "<h1>Caught PDO exception:</h1>";
    echo $exception1->getMessage() . PHP_EOL;
    echo "<h1>PHP Info for troubleshooting</h1>";
    phpinfo();
}

?>

<h1> Success Results : </h1>

<?php
try {
    while ($row = $stmt->fetch(PDO::FETCH_ASSOC)) {
        echo $row['SQL_VERSION'] . PHP_EOL;
    }
} catch (PDOException $exception2) {
    // Display errors
    echo "<h1>Caught PDO exception:</h1>";
    echo $exception2->getMessage() . PHP_EOL;
}

unset($stmt);
unset($conn);
?>
```

Verweisen Sie den Browser auf https://localhost/testsql.php (https://localhost:8080/testsql.php unter macOS). Jetzt sollten Sie eine Verbindung zu Ihrer SQL Server-/Azure SQL-Datenbank herstellen können. Wenn Sie keine Erfolgsmeldung mit SQL-Versionsinformationen sehen, können Sie einige grundlegende Problembehandlungen durchführen, indem Sie das Skript über die Befehlszeile ausführen:

```bash
php testsql.php
```

Wenn die Ausführung über die Befehlszeile erfolgreich ist, aber in Ihrem Browser nichts angezeigt wird, überprüfen Sie die [Apache-Protokolldateien](https://linuxize.com/post/apache-log-files/#location-of-the-log-files). Weitere Informationen finden Sie in den entsprechenden [Supportressourcen](support-resources-for-the-php-sql-driver.md).

## <a name="see-also"></a>Weitere Informationen  
[Getting Started with the Microsoft Drivers for PHP for SQL Server (Erste Schritte mit dem Microsoft-Treiber für PHP für SQL Server)](../../connect/php/getting-started-with-the-php-sql-driver.md)

[Loading the Microsoft Drivers for PHP for SQL Server (Laden von Microsoft-Treibern für PHP für SQL Server)](../../connect/php/loading-the-php-sql-driver.md)

[Systemanforderungen für Microsoft-Treiber für PHP für SQL Server](../../connect/php/system-requirements-for-the-php-sql-driver.md)

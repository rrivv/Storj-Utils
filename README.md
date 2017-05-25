# Storj-Utils

Скрипт проверки основных параметров работы нод Storjshare-Cli для Linux.<br/>

![Storj bash health script](http://maxrival.com/content/images/2017/05/storj-bash-healt-script-v1.0.2.png)

Скрипт работает на CentOS Linux release 7.0.1406 (Core)
<hr>
Установка

```
wget https://raw.githubusercontent.com/AntonMZ/Storj-Utils/master/health.sh
```
<hr>

- [**NodeID**] - уникальный идентификатор ноды.<br/>
Данные берутся из **storjshare status**

<hr>

- [**ResponseTime**] - показатель стабильности работы ноды.<br/>

 Выставляется непосредственно бриджем.<br/>
Чем ниже, тем больше шансов получить новые контракты.<br/>
Уменьшается со временем.<br/>
Чем стабильнее работает нода, тем меньше данный показатель.<br/>
Данные берутся с api.storj.io

 Cтатусы
    
 **good** - в пределах нормы<br/>
 **bad** - не в пределах нормы

 *Для Москвы нормой считается значение данного показателя до 1000*<br/>
    
 Выставляется непосредственно бриджем.<br/>
 Данные берутся с api.storj.io

<hr>

- [**Address**] - текущий IP адрес ноды.<br/>
Данные берутся локально с сервера ноды.<br/>

<hr>

- [**User Agent**] - версия агента на ноде.<br/>

 Данные берутся с api.storj.io<br/>

<hr>

- [**Last Seen**] - последнее время появления ноды в сети.

 Последнее появление ноды в сети зафиксированное бриджем.<br/>
Данные берутся с api.storj.io<br/>

<hr>

- [**Port**] - порт ноды<br/>
Данные берутся с api.storj.io<br/>

 При запуску скрипта осуществляется проверка порта на ***открыт/закрыт*** через внешний api ресурс.
    
 Cтатусы<br/>
    
 **open** - порт открыт<br/>
 **close** - порт закрыт

 Порт может быть закрыт по многим причинам.
    
 Самые распространенные:
 
 * порт закрыт брандмауэром Windows или iptables
 * порт не "проброшен" в роутере/маршрутизаторе

<hr>

- [**Protocol**] - версия протокола storjshare-cli<br/>
Данные берутся с api.storj.io<br/>

<hr>

- [**Last Timeout**] - <br/>
Данные берутся с api.storj.io

<hr>

- [**Timeout Rate**] - <br/>
Данные берутся с api.storj.io

<hr>

- [**DeltaTime**] - временная дельта<br/>
Параметр показывает разницу локального времени и времени эталонного NTP сервера.<br/>
Параметр передается непосредственно бриджем сети.<br/>

<hr>
Описание всех параметров будет представлено отдельной публикацией на сайте http://maxrival.com

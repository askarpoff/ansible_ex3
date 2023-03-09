# 08-ansible-03-yandex

Playbook устанавливает Clickhouse, Vector и Lighthouse на три хоста, доступные по по ssh, запускает службы `clickhouse-server`, `vector`, создает базу `logs` в `clickhouse`,устанавливает и запускает веб-север nginx, разворачивает web-интерфейс `lighthouse`

### Variables
В каталоге group_vars задаются версии дистрибутивов.

|clickhouse_version|версия clickhouse| 
|vector_version|версия vector|
|lighthouse_src|ссылка на zip-архив ветки master в  git lighthouse|
|nginx_user_name|пользователь для запуска  nginx|
    
### Install Clickhouse
 Скачиваются rpm пакеты, устанавливается Сlickhouse, создается база logs. 
 
### Install Vector
Скачиваются пакеты, устанавливается Vector. Запуск службы.

### Install Lighthouse
Устанавливается веб-сервер nginx. Настраивается конфиги веб-сервера. Добавляется сервис nginx в автозагрузку. Создается директория /var/www/
Распапковываются файлы lighthouse.

### Tags

|clickhouse| Устанавливает только Сlickhouse| 
|vector| Устанавливает только Vector|
|lighthouse| Устанавливает только Lighthouse|
   

# FTP_service

## Основные задания:
- Посмотреть содержимое папки 
 - Верхнее окно 
 - клиент 
 - нижнее
 - сервер.

- Создать папку
  - Домашняя папка пользователя
  - В ней созданная нами
  - Удалить папку

### Удалить файл, cоздание и переименование далее
- Переименовать файл

- Скопировать файл с клиента на сервер

- Скопировать файл с сервера на клиент

- Клиент запущен в корневой директории сервера поэтому получается, что скопировали в рабобую директорию клиент, которая является и рабочей директорией сервера

- Выход (отключение клиента от сервера);
  - командой exit закрывается клиентское приложение

### Дополнительные задания:
1. Ограничьте возможности пользователя рамками одной определенной директории. Внутри нее он может делать все, что хочет: создавать и удалять любые файлы и папки. Нужно проследить, чтобы пользователь не мог совершить никаких действий вне пределов этой директории. Пользователь, в идеале, вообще не должен догадываться, что за пределами этой директории что-то есть. Как видно было из предыдщуих скринов выйти за пределы папки - корня не может, а это рабочая папка пользователя у admin эта папка - корень сервера.


2. Добавьте логирование всех действий сервера в файл. Можете использовать разные файлы для разных действий, например: подключения, авторизации, операции с файлами. Логи пишутся в файл корень сервера log.txt

3. Добавьте возможность авторизации пользователя на сервере. Можно увидеть на каждом скриншоте.

4. Добавьте возможность регистрации новых пользователей на сервере. При регистрации для пользователя создается новая рабочая папка (проще всего для ее имени использовать логин пользователя) и сфера деятельности этого пользователя ограничивается этой папкой. пользоваталь вводит логин пароль, если такой пользователь не существует - то создается, если существует, то проверяется корректность введенных данных.


Неудачная авторизация 

9. Реализуете квотирование дискового пространства для каждого пользователя. По 10Мб на пользователя, пример неудачной попытки:

- Папка весит уже почти 9Мб. попытаемся переместить в нее файл 3 Мб


11. Реализуйте учётную запись администратора сервера.

- log/pass = admin/admin, рабочая директория - рабочая директория сервера, то есть папка с папками пользователя 13. Напишите отладочный клиент. Клиент должен подключаться к серверу и в автоматическом режиме тестировать корректность его работы. Используйте подход, аналогичный написанию модульных тестов. Клиент должен вывести предупреждающее сообщение, если сервер работает некорректно. файл ftp-test-client log/pass = test/test

4. Создайте структуру
• Структура папки (архитектурный шаблон MVC)
Пример: https://www.codeproject.com/Articles/1080626/Code-Your-Own-PHP-MVC-Framework-in-Hour
• Файлы (index.php, формы, стартовая страница ...)

5. Создайте соединение базы данных с сервером Linux на PHP.
• Объектно-ориентированный (БД классов)
• mySQLi
 
6. Создайте сценарий входа в систему PHP.
• Страница входа для пользователей (пользователей класса)
• Страница входа для администратора (администратора класса)
• Пароль должен быть хеширован
• Используйте операторы подготовки MySQLi
 
 
7. Создайте портал пользователя / администратора PHP.
• Вход / выход пользователя
• Заголовок / панель навигации с именем пользователя (использовать сеанс)
• Раздел / ы
 название раздела (в заголовке)
 Список сообщений
 Собственные сообщения CRUD
Пример загрузки изображения: https://www.codexworld.com/upload-store-image-file-in-database-using-php-mysql/
 
8. Создайте административную панель PHP.
• Вход / выход
• Заголовок / панель навигации с именем пользователя
• Список пользователей (все пользователи)
• Список разделов (все разделы)
• разделы CRUD
• Пользователи CRUD
 Если новый пользователь создается / изменяется, проверьте почтовый индекс с помощью JS, чтобы форма не перезагружалась

Продолжительность экзамена
Начало 8:00
Предисловие - 5-10 мин.
Настройка компьютера - 10-15 мин.
Установить редактор кода настройки -10-15 мин.
Импортировать образ в ВМ
Проверьте настройки сетевого моста
Создать SSH-соединение (WinSCP)
Запустить сценарий отладки (замазка)
{tail -f / var / log / httpd / error_log}
План реализации (+ время)
Графическая ER диаграмма из БД
Создайте подключение к вашей виртуальной машине в Windows
Создайте файл «Hello World» и вызовите его в браузере Win (показать код)
Показать информацию о настройках сервера PHP (phpinfo ();)
Информационный сайт PHP
V1 .: в index.php (после подключения к базе данных)
phpinfo ();
V2.
нано /var/www/html/info.php
<? php
phpinfo ();
?>
Создать документацию
Доставка в 10:00
Реализация части 1:
Есть сайт ассоциации "Клуб".
Есть 3 области интересов:
Мото
автомобиль
грузовая машина
Администратор может создавать учетные записи пользователей. С помощью которого пользователь может затем войти на сайт.
При создании пользователя должна быть создана проверка создания (только цифры, не пустая) с предупреждающей информацией. Но все же прошу сэкономить.
Пользователь и администратор имеют отдельные страницы входа.

 
Создайте базу данных (phpmyadmin (не забудьте изменить настройки пользователя и db)
Создать структуру папок
Создайте соединение mysqli с базой данных (объектно-ориентированное)
Создайте функцию входа в систему (создайте и используйте класс)
Должно быть 2 отдельные страницы входа для пользователей и

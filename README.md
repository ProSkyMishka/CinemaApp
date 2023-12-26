# CinemaApp
Для хранения информации было принято решение написать базу данных и для взаимодействия использовать SQLite(согласовано с семинаристом)
Для взаимодействия с базой данных в kotlin надо подключить в зависимости проекта драйвер jdbc(он уже скачен и лежит в проекте в папке lib)
Вот как это сделать:
1. Открываете проект в IDEA
2. Нажимаете правой кнопкой мыши на проект
3. Выбираете пункт "Open Module Settings"
4. Выбираете пункт "Dependencies"
5. Нажимаете на +
6. Выбираете "Jars or ..."
7. Выбираете rdbc драйвер(называется sqlite-jdbc-3.43.0.0.jar)
8. Нажимаете OK

к пользоваться:
При запуске пользователю предлагается выбор:

1 Регистрация

2 Авторизация 

0 Остановить приложение


При выборе пункта остановить приложение, приложение останавливается

При остальных двух выборах пользователь вводит своё пользовательское имя и пароль, который шифруется. Если это регистрация, то программа проверяет, есть ли в бд пользователь с таким именем и если нет, то добавляет его в бл, если есть, то сообщает пользователю и снова предлагает тот же выбор. Если это авторизация, то программа ищет пользователя в бд, если не находит, то сообщает пользователю и возвращает его к предыдущему выбору. Если находит, то сравнивает пароль в бд с хешированной строкой введенного пользователем пароля, если не сходятся, то программа сообщает об этом пользователю и возвращает его к первому выбору, если сходятся, то выдаётся сообщение All right и пользователю предлагают выбор:

1 Удалить аккаунт(при выборе пункта, аккаунт пользователя удаляется, а сам пользователь возвращается к первому выбору)

2 Работать с фильмами(описание ниже)

3 Вывести всех работников(выводятся все зарегистрированные аккаунты, после чего пользователю снова предлагается этот выбор)

4 Назад(пользователь возвращается к предыдущему выбору)


При выборе работать с фильмами пользователю открывается выбор:

1 Добавить фильм(пользователь вводит название и длительность, после чего возвращается к этому же выбору)

2 Вывести фильмы(выводятся все фильмы, которые есть у кинотеатра, после чего пользователь возвращается к этому же выбору)

3 Выбрать фильм(описание ниже)

4 Вывести сеансы(выводятся все сеансы, которые ещё не закончились, после чего пользователь возвращается к этому же выбору)

5 Вывести историю сеансов(выводятся все сеансы которые есть, были и будут, после чего пользователь возвращается к этому же выбору)

0 Назад(возвращает пользователя к предыдущему выбору)

При выборе пункта выбрать фильм пользователю предлагают выбрать один фильм из всех, что есть у кинотеатра, после выбора пользователю предлагается выбрать действие с этим фильмом:

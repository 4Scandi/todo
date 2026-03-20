1. 

открываем в браузере http://localhost/phpmyadmin =)
создай новую базу данных  имя: todo_app
выбери базу todo_app слева
перейди во вкладку SQL
вставь и выполни этот код(Для удобства)


SQLCREATE TABLE todos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    completed TINYINT(1) DEFAULT 0,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);


2. надо положи серверную часть в правильное место
Папка server должна лежать здесь: (ну лично у меня так)
C:\xampp\htdocs\todo-app\server\api\

3. проверяем сервер работает или гет
Открой в браузере:
http://localhost/todo-app/server/api/todos.php
должен появиться такой текст:
{"todos":[],"stats":{"total":0,"completed":0}}
если ошибка  проверь путь к папке или config.php (логин root, пароль пустой).

4. запуск фронтенда

надо открыть терминал (CMD или powershell)
переходим  в папку client
cd путь к проекту\client
(например G:\todo\client)
качаем зависимости
npm install

всё осталось запустить

npm run dev
откроется браузер (а если не появится  http://localhost:5173 или http://localhost:5174 какой покажет терминал вообщем)


// вроде всё написал что нужно и  наврядли будут ошибки, но на всякий я еще видео сделаю если лень будет разворачивать сайт на своем пк. Также закину презентацию 

layout: page
title: "Test page"
permalink: /


<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Quick Start</title>
    <script src="https://telegram.org/js/telegram-web-app.js?63"></script>
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" integrity="sha256-p4NxAoJBhIIN+hmNHrzRCf9tD/miZyoHS5obTRR9BMY=" crossorigin=""/>
  </head>
  <body>
<style>
#map { height: 280px; width: 280px; }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f0f8ff; /* Очень светлый голубой фон */
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        /* Стили самой формы */
        .blue-form {
            background: linear-gradient(135deg, #e1f5fe 0%, #b3e5fc 100%); /* Градиент голубых цветов */
            border: 2px solid #81d4fa;
            border-radius: 15px;
            padding: 30px 40px;
            box-shadow: 0 8px 20px rgba(3, 155, 229, 0.2);
            color: #01579b; /* Темно-синий текст для контраста */
            display: flex;
            flex-direction: column;
            gap: 20px;
            width: 280px;
        }

        /* Стили для лейбла и чекбокса */
        .checkbox-container {
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 20px;
            font-weight: 600;
            cursor: pointer;
            user-select: none;
        }

        /* Красим сам чекбокс в голубой цвет */
        input[type="checkbox"] {
            width: 20px;
            height: 20px;
            accent-color: #0288d1; 
            cursor: pointer;
        }

        /* Стили кнопки */
        .blue-button {
            background-color: #29b6f6;
            color: white;
            border: none;
            border-radius: 8px;
            padding: 12px 20px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(2, 136, 209, 0.3);
        }

        /* Эффект при наведении на кнопку */
        .blue-button:hover {
            background-color: #0288d1;
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(2, 136, 209, 0.4);
        }

        .blue-button:active {
            transform: translateY(0);
        }

        /* Поле для вывода результата */
        #result {
            text-align: center;
            font-size: 16px;
            font-weight: 500;
            min-height: 24px;
            margin-top: 5px;
            color: #0277bd;
        }
</style>

    <form class="blue-form" id="myForm" onsubmit="return false;">
        <label class="checkbox-container">
            <input type="checkbox" id="autoCheckbox">
            Авто?
        </label>
        
        <button type="button" class="blue-button" id="actionBtn">Применить</button>
        <div id="map"></div>
    </form>
  </body>
</html>

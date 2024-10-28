<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>رسالة إعجاب</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(to bottom right, #ffcccb, #ff99cc);
            color: #333;
            text-align: center;
            padding: 50px;
            animation: backgroundAnimation 10s infinite alternate;
        }

        @keyframes backgroundAnimation {
            0% { background-color: #ffcccb; }
            100% { background-color: #ff99cc; }
        }

        h1 {
            font-size: 2.5em;
            color: #ff4d4d;
            margin-bottom: 20px;
        }

        p {
            font-size: 1.5em;
            margin: 20px 0;
        }

        .button {
            padding: 10px 20px;
            font-size: 18px;
            background-color: #ff4d4d;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s, transform 0.3s;
            margin: 10px;
        }

        .button:hover {
            background-color: #ff1a1a;
            transform: scale(1.1);
        }

        .hearts {
            font-size: 50px;
            color: #ff4d4d;
        }

        .flowers {
            font-size: 30px;
        }
        
        .sparkle {
            display: none;
            position: fixed;
            width: 100%;
            height: 100%;
            background: url('https://media.giphy.com/media/3o7buu6M3s1ZFxICpC/giphy.gif') center center no-repeat;
            background-size: cover;
            z-index: 1000;
        }
    </style>
</head>
<body>

    <h1>مرحباً!</h1>
    <p class="flowers">🌹🌺🌸🌼🌷</p>
    <p id="message"></p>
    <div class="hearts">❤️❤️❤️❤️❤️</div>
    
    <button class="button" onclick="showMessage()">عرض رسالة إعجاب</button>
    <button class="button" onclick="showSparkle()">انبهر!</button>

    <div class="sparkle" id="sparkleEffect"></div>

    <script>
        function showMessage() {
            const message = "يا صاحبة أجمل عينين في الكون!";
            document.getElementById("message").innerText = message;
        }

        function showSparkle() {
            const sparkleEffect = document.getElementById("sparkleEffect");
            sparkleEffect.style.display = 'block';

            // اختفاء التأثير بعد 3 ثوانٍ
            setTimeout(() => {
                sparkleEffect.style.display = 'none';
            }, 3000);
        }
    </script>

</body>
</html>

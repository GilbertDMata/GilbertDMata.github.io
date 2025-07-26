<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Smart Blizzard Layout</title>
    <style>
        body {
            background-image: url('haw.png');
            background-size: cover;
            background-position: bottom;
            background-repeat: no-repeat;
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
            height: 200vh;
            overflow: hidden;
        }

        .top-section {
            text-align: center;
            padding: 40px 20px 20px 20px;
            position: relative;
            z-index: 2;
        }

        .top-text {
            font-size: 3rem;
            color: #fff;
            transition: 0.3s ease;
            cursor: pointer;
            margin-bottom: 20px;
        }

        .top-text:hover {
            color: #9eb2e9;
            transform: scale(1.1);
        }

        .button-row {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        .button-row button {
            padding: 12px 29px;
            border: none;
            border-radius: 10px;
            background-color: rgba(255, 255, 255, 0.8);
            color: #333;
            font-size: 1rem;
            cursor: pointer;
            transition: 0.3s ease;
        }

        .button-row button:hover {
            background-color: #ff4040b9;
            color: white;
            transform: scale(1.05);
        }

        .container {
            background-color: rgba(255, 255, 255, 0.8);
            padding: 70px;
            border-radius: 12px;
            text-align: center;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
            max-width: 500px;
            margin: 100px auto;
            position: relative;
            z-index: 2;
        }

        .container p {
            font-size: 1.2rem;
            color: #555;
        }

        /* Blizzard Animation */
        .snowflake {
            position: fixed;
            top: -10px;
            color:gradient(rgba(248, 242, 242, 0.897), rgb(197, 9, 34));
;
            font-size: 1em;
            user-select: none;
            z-index: 1;
            animation-name: fall;
            animation-duration: 10s;
            animation-timing-function: linear;
            animation-iteration-count: infinite;
        }

        @keyframes fall {
            to {
                transform: translateY(110vh) rotate(360deg);
                opacity: 0;
            }
        }
    </style>
</head>
<body>

    <!-- Top Text -->
    <div class="top-section">
        <h1 class="top-text">ARR ARR ARR ARR မင်းနေသားကျသွားမှာပါ!</h1>
        <div class="button-row">
            <button onclick="showMessage('အာနာမိတယ်')">အာနာမိတယ်</button>
            <button onclick="showMessage('ဖျားနားပြီး')">ဖျားနားပြီး</button>
            <button onclick="showMessage('သွားစရာမရှိ')">သွားစရာမရှိ</button>
            <button onclick="showMessage('နင်ပျော်လား')">နင်ပျော်လား</button>
        </div>
    </div>

    <!-- Main Content Box -->
    <div class="container">
        <p>This page has a beautiful background image hee hee hee 🍃</p>
    </div>

    <!-- JS for Button Clicks -->
    <script>
        function showMessage(message) {
            alert("📣 " + message);
        }

        // ❄️ Snowfall / Blizzard effect
        function createSnowflake() {
            const snowflake = document.createElement('div');
            snowflake.classList.add('snowflake');
            snowflake.innerText = '‌=======================================================================================================================================  ';

            // Random horizontal position
            snowflake.style.left = Math.random() * 100 + 'vw';

            // Random font size
            snowflake.style.fontSize = Math.random() * 10 + 10 + 'px';

            // Random animation duration
            snowflake.style.animationDuration = Math.random() * 5 + 5 + 's';

            document.body.appendChild(snowflake);

            // Remove after animation
            setTimeout(() => {
                snowflake.remove();
            }, 10000);
        }

        // Generate flakes every 300ms
        setInterval(createSnowflake, 300);
    </script>

</body>
</html>



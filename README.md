<!DOCTYPE html><html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>العد التنازلي للثانوية العامة</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
        }
        #countdown {
            font-size: 2em;
            margin-top: 20%;
            background: white;
            padding: 20px;
            display: inline-block;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body>
    <h1>العد التنازلي لانتهاء الثانوية العامة</h1>
    <div id="countdown"></div>
    <script>
        function updateCountdown() {
            const targetDate = new Date("July 1, 2025 12:00:00").getTime();
            const now = new Date().getTime();
            const difference = targetDate - now;const days = Math.floor(difference / (1000 * 60 * 60 * 24));
        const hours = Math.floor((difference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        const minutes = Math.floor((difference % (1000 * 60 * 60)) / (1000 * 60));
        const seconds = Math.floor((difference % (1000 * 60)) / 1000);

        document.getElementById("countdown").innerHTML = 
            `${days} يوم ${hours} ساعة ${minutes} دقيقة ${seconds} ثانية`;

        if (difference < 0) {
            document.getElementById("countdown").innerHTML = "انتهت الثانوية العامة!";
        }
    }
    setInterval(updateCountdown, 1000);
    updateCountdown();
</script>

</body>
</html>

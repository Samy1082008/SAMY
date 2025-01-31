<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>إعلان</title>
    <style>
        /* الخلفية تغطي الشاشة بالكامل */
        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.9); /* لون داكن مع شفافية */
            display: none;
            z-index: 1000;
        }

        /* النافذة تظهر في المنتصف بحجم كبير */
        .popup {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 90%;
            height: 90%;
            background-color: white;
            text-align: center;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 15px rgba(255, 255, 255, 0.3);
            display: none;
            z-index: 1001;
        }

        /* زر إغلاق الإعلان */
        .close-btn {
            position: absolute;
            top: 10px;
            right: 15px;
            font-size: 30px;
            cursor: pointer;
            color: red;
        }

        /* زر زيارة الموقع */
        .visit-btn {
            padding: 15px 30px;
            border: none;
            background-color: red;
            color: white;
            font-size: 20px;
            cursor: pointer;
            border-radius: 5px;
            margin-top: 20px;
        }
    </style>
</head>
<body>

    <!-- الخلفية الشفافة التي تغطي الشاشة بالكامل -->
    <div class="overlay" id="overlay"></div>

    <!-- نافذة الإعلان -->
    <div class="popup" id="popup">
        <span class="close-btn" onclick="closePopup()">×</span>
        <h2>🔥 إعلان هام! 🔥</h2>
        <p>قم بزيارة موقعي الآن واحصل على أفضل العروض والخدمات!</p>
        <a href="https://yourwebsite.com" target="_blank">
            <button class="visit-btn">زيارة الموقع</button>
        </a>
    </div>

    <script>
        // تشغيل الإعلان بعد 3 ثوانٍ
        window.onload = function() {
            setTimeout(function() {
                document.getElementById("popup").style.display = "block";
                document.getElementById("overlay").style.display = "block";
            }, 3000);
        };

        // إغلاق الإعلان عند الضغط على زر × أو الخلفية
        function closePopup() {
            document.getElementById("popup").style.display = "none";
            document.getElementById("overlay").style.display = "none";
        }

        document.getElementById("overlay").onclick = closePopup;
    </script>

</body>
</html># SAMY

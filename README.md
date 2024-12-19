# sN
<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="theme-color" content="#000000"> <!-- تخصيص اللون في المتصفح -->
    <title>اختار بروفايلك في دسكورد</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(to bottom, #000000, #555555);
            color: white;
            height: -webkit-fill-available;
            max-height: -webkit-fill-available;
            height: 100vh;
            max-height: 100vh;
        }

        header {
            background-color: #333;
            color: white;
            padding: 20px;
            text-align: center;
            border-bottom: 2px solid #444;
        }

        .profile-container {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            margin: 20px;
        }

        .profile {
            background-color: #444;
            border-radius: 10px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            width: 200px;
            margin-bottom: 20px;
            cursor: pointer;
            transition: transform 0.3s ease-in-out;
        }

        .profile img {
            width: 100%;
            height: 150px;
            object-fit: cover;
        }

        .profile-details {
            padding: 10px;
            text-align: center;
        }

        .profile:hover {
            transform: scale(1.1);
        }

        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 10px;
            position: absolute;
            bottom: 0;
            width: 100%;
        }

        .download-btn {
            background-color: #007BFF;
            color: white;
            padding: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 10px;
            transition: background-color 0.3s;
        }

        .download-btn:hover {
            background-color: #0056b3;
        }

        .discord-link {
            text-align: center;
            margin-top: 20px;
        }

        .discord-link a {
            background-color: #ffffff;
            color: rgb(0, 0, 0);
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 5px;
            font-size: 16px;
            transition: background-color 0.3s;
        }

        .discord-link a:hover {
            background-color: #5b6eae;
        }

        @media (max-width: 500px) {
            header {
                min-height: 0;  /* تحسين عرض الواجهة على الشاشات الصغيرة */
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>اختار بروفايلك</h1>
    </header>

    <div class="profile-container">
        <!-- بروفايل 1 -->
        <div class="profile" onclick="downloadProfile('images/avatar1.jpg', 'images/banner1.jpg')">
            <img src="images/avatar1.jpg" alt="Avatar 1">
            <div class="profile-details">
                <h3>بروفايل 1</h3>
                <button class="download-btn">تحميل البروفايل</button>
            </div>
        </div>

        <!-- بروفايل 2 -->
        <div class="profile" onclick="downloadProfile('images/avatar2.jpg', 'images/banner2.jpg')">
            <img src="images/avatar2.jpg" alt="Avatar 2">
            <div class="profile-details">
                <h3>بروفايل 2</h3>
                <button class="download-btn">تحميل البروفايل</button>
            </div>
        </div>

        <!-- بروفايل 3 -->
        <div class="profile" onclick="downloadProfile('images/avatar3.jpg', 'images/banner3.jpg')">
            <img src="images/avatar3.jpg" alt="Avatar 3">
            <div class="profile-details">
                <h3>بروفايل 3</h3>
                <button class="download-btn">تحميل البروفايل</button>
            </div>
        </div>
    </div>

    <div class="discord-link">
        <a href="https://discord.gg/AKe9HG22" target="_blank">Discord</a>
    </div>

    <footer>
        <p>&copy; 2024 جميع الحقوق محفوظة</p>
    </footer>

    <script>
        function downloadProfile(avatar, banner) {
            let avatarLink = document.createElement('a');
            avatarLink.href = avatar;
            avatarLink.download = avatar;
            avatarLink.click();

            let bannerLink = document.createElement('a');
            bannerLink.href = banner;
            bannerLink.download = banner;
            bannerLink.click();
        }
    </script>
</body>
</html>


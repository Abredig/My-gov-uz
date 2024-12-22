# MyGov Uz - Interaktiv davlat xizmatlari portali
Bu yerda MyGov Uz portali haqida ma'lumot beriladi.

## Foydalanish
1. **PIN-kodni kiriting** va "Ochish" tugmasini bosing.
2. Faylni ko'rish yoki yuklab olish mumkin.

## Aloqa
[MyGov Uz] rasmiy sayti
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="description" content="MyGov Uz - Interaktiv davlat xizmatlari portali">
    <meta name="keywords" content="my.gov.uz, interaktiv xizmatlar, davlat xizmatlari">
    <meta name="author" content="MyGov Uz">
    <title>MyGov Uz - Interaktiv davlat xizmatlari</title>
    <link rel="icon" href="your_logo_favicon.ico" type="image/x-icon">
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" rel="stylesheet">
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        .navbar-brand img {
            width: 150px;
            height: auto;
        }
        .header {
            text-align: center;
            margin-top: 50px;
        }
        .pin-form {
            max-width: 400px;
            margin: 0 auto;
            padding: 30px;
            border: 1px solid #ddd;
            border-radius: 10px;
            background-color: #f9f9f9;
        }
        .footer {
            text-align: center;
            padding: 20px;
            background-color: #f1f1f1;
            margin-top: 50px;
        }
        .btn-primary {
            background-color: #007bff;
            border-color: #007bff;
        }
        .footer a {
            text-decoration: none;
            color: #007bff;
        }
    </style>
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <a class="navbar-brand" href="https://my.gov.uz/">
            <img src="your_logo_path.png" alt="MyGov Uz Logo">
        </a>
    </nav>

    <div class="header">
        <h1>MyGov Uz Portali</h1>
        <p>Bizning interaktiv xizmatlarimizdan foydalaning!</p>
    </div>

    <div class="container">
        <div class="pin-form">
            <h3 class="text-center">Fayldagi kodni kiriting</h3>
            <form id="pin-form" method="POST">
                <div class="form-group">
                    <label for="pin-code">PIN-kod:</label>
                    <input type="text" class="form-control" id="pin-code" name="pin_code" placeholder="PIN kodni kiriting" required>
                </div>
                <button type="submit" class="btn btn-primary btn-block">Ochish</button>
            </form>
        </div>
    </div>

    <div class="footer">
        <p>© 2024 <a href="http://uzinfocom.uz/" target="_blank">UZINFOCOM</a> - Ishlaydi <a href="http://www.yiiframework.com/" target="_blank">Yii Framework</a></p>
    </div>

    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.2/dist/umd/popper.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>

    <script>
        // Faylni ochish uchun JavaScript kodini qo'shamiz
        document.getElementById('pin-form').addEventListener('submit', function(event) {
            event.preventDefault(); // Formaning normal yuborilishiga to'sqinlik qiladi

            var pinCode = document.getElementById('pin-code').value;

            // To'g'ri PIN kodi misol uchun: '2376'
            if(pinCode === '2376') {
                // To'g'ri PIN kodi bo'lsa, PDF faylni ochish
                window.location.href = 'https://drive.google.com/file/d/1jdj2u19HQrMmUBOfF3KFl077xxrVQToO/view?usp=drivesdk';
            } else {
                // Agar PIN kodi noto'g'ri bo'lsa, foydalanuvchiga xabar berish
                alert('PIN kodi noto\'g\'ri, iltimos qayta urinib ko\'ring.');
            }
        });
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="description" content="MyGov Uz - Интерактивные государственные услуги">
    <meta name="keywords" content="my.gov.uz, интерактивные услуги, государственные услуги">
    <meta name="author" content="MyGov Uz">
    <title>MyGov Uz - Интерактивные государственные услуги</title>
    <link rel="icon" href="https://raw.githubusercontent.com/Abredig/My-gov-uz/main/logo_mobile.png" type="image/x-icon">
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" rel="stylesheet">
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.8; /* Elementlar orasidagi masofa oshirildi */
            background-color: #ffffff; /* Oq fon */
        }
        .navbar-brand img {
            width: 50px; /* Logotip kichik */
            height: auto;
        }
        .pin-form {
            max-width: 400px;
            margin: 20px auto;
            padding: 30px;
            background-color: #ffffff; /* Bir xil fon */
        }
        h5, .pin-code-label {
            font-size: 14px;
            margin-bottom: 15px; /* Orasidagi masofa oshirildi */
        }
        .pin-code-label {
            font-weight: bold; /* "ПИН код:" qalin yozildi */
        }
        .btn-primary {
            background-color: #28a745; /* Yashil tugma */
            border-color: #28a745;
            margin-top: 20px;
        }
        .pin-code-description {
            color: #003366; /* Toʻq koʻk rang */
            font-weight: bold; /* Qalin shriftda */
            text-align: left; /* Chapga tekislash */
            font-size: 12px; /* Harf o'lchami kichiklashtirildi */
            margin-top: 20px; /* Tugma bilan orasidagi masofa oshirildi */
        }
        .pin-code-image {
            width: 55%; /* 10% kattalashtirish */
            display: block;
            margin: 30px auto;
        }
    </style>
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <a class="navbar-brand" href="https://my.gov.uz/">
            <img src="https://raw.githubusercontent.com/Abredig/My-gov-uz/main/logo_mobile.png" alt="MyGov Uz Logo">
        </a>
    </nav>

    <div class="container">
        <div class="pin-form">
            <h5>Введите PIN-код для просмотра документа</h5>
            <form id="pin-form" method="POST">
                <div class="form-group">
                    <label for="pin-code" class="pin-code-label">ПИН код:</label>
                    <input type="text" class="form-control" id="pin-code" name="pin_code" placeholder="Введите ПИН код" required>
                </div>
                <button type="submit" class="btn btn-primary btn-block">Открыть</button>
                <p class="pin-code-description">PIN-код размещается рядом с QR-кодом документа</p>
            </form>
            <img src="https://raw.githubusercontent.com/Abredig/My-gov-uz/main/pin_code_document.jpg" alt="Pin Code Document" class="pin-code-image">
        </div>
    </div>

    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.2/dist/umd/popper.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>

    <script>
        document.getElementById('pin-form').addEventListener('submit', function(event) {
            event.preventDefault();

            var pinCode = document.getElementById('pin-code').value;

            if(pinCode === '7413') {
                window.location.href = 'https://drive.google.com/file/d/1jdj2u19HQrMmUBOfF3KFl077xxrVQToO/view?usp=drivesdk';
            } else {
                alert('Неправильный PIN-код, попробуйте снова.');
            }
        });
    </script>
</body>
</html>

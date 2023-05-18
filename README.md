<!DOCTYPE html>
<html>
<head>
    <title>تخمين الرقم</title>
    <script>
        function guessNumber() {
            var randomNumber = Math.floor(Math.random() * 10) + 1;
            var userGuess = document.getElementById("guess").value;

            if (userGuess == randomNumber) {
                alert("تهانينا! لقد حزرت الرقم الصحيح.");
            } else {
                alert("للأسف، حاول مرة أخرى. الرقم الصحيح هو: " + randomNumber);
            }
        }
    </script>
</head>
<body>
    <h1>تخمين الرقم</h1>
    <p>قم بإدخال رقم بين 1 و 10:</p>
    <input type="text" id="guess" />
    <button onclick="guessNumber()">تخمين</button>
</body>
</html>

<!DOCTYPE html>
<html>
<head>
    <title>لعبة سباق السيارات</title>
    <style>
        #road {
            width: 500px;
            height: 600px;
            background-color: #000;
            position: relative;
        }

        #car {
            width: 50px;
            height: 100px;
            background-color: #f00;
            position: absolute;
            bottom: 0;
        }
    </style>
</head>
<body>
    <h1>لعبة سباق السيارات</h1>
    <div id="road">
        <div id="car"></div>
    </div>

    <script>
        document.addEventListener('keydown', function (event) {
            if (event.code === 'ArrowLeft') {
                moveLeft();
            } else if (event.code === 'ArrowRight') {
                moveRight();
            }
        });

        function moveLeft() {
            var car = document.getElementById('car');
            var currentLeft = parseInt(car.style.left) || 0;
            var newLeft = currentLeft - 10;
            if (newLeft >= 0) {
                car.style.left = newLeft + 'px';
            }
        }

        function moveRight() {
            var car = document.getElementById('car');
            var currentLeft = parseInt(car.style.left) || 0;
            var newLeft = currentLeft + 10;
            if (newLeft <= 450) {
                car.style.left = newLeft + 'px';
            }
        }
    </script>
</body>
</html>

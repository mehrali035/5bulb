# 5bulb
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bulb</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        h1 {
            margin-left: 604px;
            margin-top: 89px;

        }

        .light {
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .light img {
            width: 150px;
            height: 150px;
            margin-left: 10px;
            margin-top: 70px;
        }

        .light figcaption {
            margin-left: 565px;
        }

        .btn {
            margin-left: 650px;
            margin-top: 40px;
            background-color: black;
            color: white;
            border-radius: 5px;

        }
    </style>
</head>

<body>

    <h1 id="heading">Light OFF</h1>
    <main class="light">
        <!-- <div id="heading"> <h1>Light OFF</h1></div> -->

        <figure>
            <img src="BO.jpg" id="on1" alt="">
        </figure>
        <figure>
            <img src="BO.jpg" id="on2" alt="">
        </figure>
        <figure>
            <img src="BO.jpg" id="on3" alt="">
        </figure>
        <figure>
            <img src="BO.jpg" id="on4" alt="">
        </figure>
        <figure>
            <img src="BO.jpg" id="on5" alt="">
        </figure>

    </main>
    <button class="btn" onclick="lighton()">On/Off</button>

    <script>

        const lighton = () => {
            let ltext = document.getElementById('heading');

            for (x = 1; x < 6; x++) {
                let bid = document.getElementById('on'.concat(x));
                if (bid.src.match('BON.jpg')) {
                    bid.src = 'BO.jpg';
                    ltext.innerHTML = "Light OFF";
                    ltext.style.color = 'black';

                } else {
                    bid.src = 'BON.jpg';
                    ltext.innerHTML = "Light ON";
                    ltext.style.color = 'red';
                }
            }
        } 
    </script>

</body>

</html>

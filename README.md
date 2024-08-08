<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Carta para Keily</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f8f9fa;
            margin: 0;
        }
        .envelope {
            position: relative;
            width: 300px;
            height: 200px;
            background: #fff;
            border: 2px solid #ddd;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            cursor: pointer;
            transition: transform 0.5s ease;
        }
        .heart {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 50px;
            height: 50px;
            background-color: red;
            clip-path: polygon(50% 0%, 61% 16%, 76% 16%, 100% 38%, 50% 100%, 0 38%, 24% 16%, 39% 16%);
            transition: transform 0.5s ease;
        }
        .message {
            display: none;
            padding: 20px;
            text-align: center;
            font-size: 1.2em;
            background-color: #fff;
            border: 2px solid #ddd;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        .open .envelope {
            transform: rotateY(180deg);
        }
        .open .heart {
            display: none;
        }
        .open .message {
            display: block;
        }
    </style>
</head>
<body>
    <div class="card-container">
        <div class="envelope" id="envelope">
            <div class="heart"></div>
        </div>
        <div class="message" id="message">
            Querida Keily.<br>
            Tu calidez, tu risa y tu cariño siempre iluminan mis días, incluso en los momentos más difíciles. Eres una persona increíble, y me siento muy afortunado de tenerte en mi vida. Gracias por ser tú y por estar siempre ahí. <br>
            Te quiero muchísimo.<br><br>
            Con todo mi cariño,<br>
            Yordi
        </div>
    </div>
    <script>
        document.getElementById('envelope').addEventListener('click', function() {
            document.body.classList.add('open');
        });
    </script>
</body>
</html>

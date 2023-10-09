
vose aceita? 
<!DOCTYPE html>
<html>
<head>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        
        a {
            /* Estilo para links (a) aqui */
        }
        
        .box {
            text-decoration: none;
            font-size: 20px;
            color: white;
            height: 250px;
            width: 350px;
            border-radius: 10px;
            background: #191919;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        
        .buttons-container {
            display: flex;
            justify-content: space-around;
            height: 50px;
            width: 150px;
        }
        
        button {
            height: 30px;
            width: 50px;
            background: white;
            border-radius: 5px;
            color: blue;
            font-weight: 600;
        }
    </style>
</head>
<body>
    <div class="box">
        <p>Cuzinho hoje?</p>
        <div class="buttons-container">
            <a class="button" href="https://youtu.be/8ScAnaU0FFE?si=32FewzP3s1TDSC-Z">Sim</a>
            <button id="no">Não</button>
        </div>
    </div>

    <script>
        let button = document.getElementById('no');
        let height = window.innerHeight - 50;
        let width = window.innerWidth - 50;

        // Evento para dispositivos móveis (touchstart)
        button.addEventListener('touchstart', function (e) {
            e.preventDefault(); // Impede o comportamento padrão do toque (por exemplo, zoom)
            button.style.position = "absolute";
            button.style.top = Math.random() * height + "px";
            button.style.left = Math.random() * width + "px";
        });

        // Evento para desktop (mouseover)
        button.addEventListener('mouseover', function () {
            button.style.position = "absolute";
            button.style.top = Math.random() * height + "px";
            button.style.left = Math.random() * width + "px";
        });
    </script>
</body>
</html>

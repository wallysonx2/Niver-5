<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jornada do Meu Aniversário</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f9;
            margin: 0;
            padding: 20px;
        }
        h1, h2 {
            color: #4CAF50;
        }
        p {
            font-size: 18px;
            color: #333;
            margin: 20px 0;
        }
        iframe {
            width: 100%;
            max-width: 720px;
            height: 405px;
            border: none;
            border-radius: 15px;
            margin: 20px 0;
        }
        button {
            padding: 15px 30px;
            font-size: 16px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        #senha-container, #conteudo, #localizacao {
            display: none;
        }
        input[type="text"] {
            padding: 10px;
            font-size: 16px;
            border: 1px solid #ccc;
            border-radius: 5px;
            margin-right: 10px;
        }
    </style>
    <script>
        function iniciarJornada() {
            document.querySelector('#senha-container').style.display = 'block';
        }

        function verificarSenha() {
            const senha = document.querySelector('#senha').value;
            if (senha === "2327") {
                document.querySelector('#senha-container').style.display = 'none';
                document.querySelector('#conteudo').style.display = 'block';
            } else {
                alert("Senha incorreta. Tente novamente.");
            }
        }

        function verificarResposta() {
            const resposta = document.querySelector('#resposta').value.toLowerCase();
            if (resposta === "valerian") {
                document.querySelector('#misterio').style.display = 'none';
                document.querySelector('#localizacao').style.display = 'block';
            } else {
                alert("Resposta incorreta. Tente novamente.");
            }
        }
    </script>
</head>
<body>
    <h1>Jornada do Meu Aniversário</h1>
    <button onclick="iniciarJornada()">Continuar Jornada</button>
    <div id="senha-container">
        <p>Digite a senha para continuar:</p>
        <input type="text" id="senha">
        <button onclick="verificarSenha()">Entrar</button>
    </div>
    <div id="conteudo">
        <h2>Feliz Aniversário, Kamilly!</h2>
        <p>Você é uma guerreira determinada e uma pessoa incrível. Sua família te ama imensamente e sente um orgulho enorme por tudo que você conquistou. Cada desafio que você enfrentou te tornou ainda mais forte, e todos que te cercam são gratos por terem você em suas vidas. Continue brilhando e espalhando sua luz por onde passa! ❤️</p>
        <iframe src="https://www.youtube.com/embed/QW7EIOxCL4k" allowfullscreen></iframe>
        <div id="misterio">
            <h2>Hora do Mistério</h2>
            <p>Entre estrelas, mistério e cor, <br>
               uma cidade cheia de esplendor. <br>
               Mil mundos em um só lugar, <br>
               uma aventura que nos faz sonhar.</p>
            <input type="text" id="resposta">
            <button onclick="verificarResposta()">Responder</button>
        </div>
        <div id="localizacao">
            <p>Envie uma mensagem para Layza dizendo a seguinte frase, <strong>"Minha melhor amiga"</strong> e encontrará sua próxima homenagem.</p>
        </div>
    </div>
</body>
</html>

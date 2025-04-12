<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Pedido pra Laura</title>
  <style>
    body {
      background: #ffd6e0;
      font-family: 'Press Start 2P', cursive;
      text-align: center;
      padding-top: 100px;
      color: #333;
    }

    h1 {
      font-size: 18px;
      margin-bottom: 50px;
    }

    .button {
      background: #ff5e78;
      color: white;
      border: none;
      padding: 15px 30px;
      font-size: 14px;
      border-radius: 8px;
      margin: 20px;
      cursor: pointer;
      transition: transform 0.3s;
    }

    .button:hover {
      transform: scale(1.1);
    }

    #noBtn {
      position: absolute;
    }

    #msgFinal {
      display: none;
      margin-top: 40px;
      font-size: 16px;
      color: #444;
      padding: 20px;
    }
  </style>
</head>
<body>

  <h1>Laura, quer namorar comigo?</h1>

  <button class="button" onclick="dizerSim()">SIM</button>
  <button class="button" id="noBtn" onmouseover="fugir()">NÃO</button>

  <div id="msgFinal">
    <h2>Parabéns, Laura!</h2>
    <p>
      Você desbloqueou um novo nível:<br>
      <strong>Namoro com o Dev mais fofo do mundo!</strong><br>
      A partir de agora, seu coração estará em modo multiplayer!
    </p>
  </div>

  <script>
    const noBtn = document.getElementById("noBtn");

    function fugir() {
      const i = Math.floor(Math.random() * window.innerWidth - 100);
      const j = Math.floor(Math.random() * window.innerHeight - 50);
      noBtn.style.left = `${i}px`;
      noBtn.style.top = `${j}px`;
    }

    function dizerSim() {
      document.getElementById("msgFinal").style.display = "block";
    }

    // Posição inicial do botão NÃO
    window.onload = () => fugir();
  </script>

</body>
</html>

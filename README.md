<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dois Anos de Amor</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(to bottom, #ffd5e5, #ffa7b4);
      text-align: center;
      padding: 20px;
      margin: 0;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
    }
    #container {
      background-color: rgba(255, 255, 255, 0.8);
      border-radius: 10px;
      padding: 20px;
      box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
      max-width: 90%;
      width: 300px;
      margin-top: 20px;
      display: none;
      position: relative;
    }
    h1 {
      color: #e74c3c;
    }
    p {
      font-size: 16px;
      line-height: 1.6;
      margin-bottom: 20px;
    }
    #revealButton {
      background-color: #e74c3c;
      color: #fff;
      border: none;
      padding: 10px 20px;
      border-radius: 5px;
      cursor: pointer;
      font-size: 14px;
      transition: background-color 0.3s ease-in-out;
    }
    #revealButton:hover {
      background-color: #c0392b;
    }
    #marryQuestion {
      font-size: 20px;
      margin-top: 20px;
      transition: all 0.3s ease-in-out;
    }
    #marryQuestion:hover {
      transform: translateX(20px);
    }
    .options {
      display: flex;
      flex-direction: column;
      margin-top: 10px;
    }
    .option {
      font-size: 14px;
      margin: 5px 0;
      cursor: pointer;
      transition: color 0.3s ease-in-out;
    }
    .option:hover {
      color: #e74c3c;
    }
    .option-yes {
      font-weight: bold;
      color: #e74c3c;
    }
    .option-no {
      font-weight: bold;
      color: #000000;
    }
    .link {
      color: #000000;
      text-decoration: underline;
      cursor: pointer;
    }
    .confetti {
      position: absolute;
      width: 10px;
      height: 10px;
      background-color: #e74c3c;
      border-radius: 50%;
      animation: confetti-fall 3s infinite;
    }
    @keyframes confetti-fall {
      0% {
        transform: translateY(-100%);
      }
      100% {
        transform: translateY(100vh);
      }
    }
  </style>
</head>
<body>
  <button id="revealButton">Revelar Mensagem</button>
  <div id="container">
    <h1>Dois Anos de Amor</h1>
    <p>18/08/21. A data mais importante da minha vida...</p>
    <p>.</p>
  </div>
  <div id="marryQuestion">Quer casar comigo?</div>
  <div class="options">
    <a href="https://www.youtube.com/watch?v=iDHp8G5ddNs" class="option option-yes">Sim</a>
    <span class="option option-no">Não</span>
  </div>
  <p class="link"><a href="https://www.example.com">com todo amor e carinho</a></p>
  <script>
    const revealButton = document.getElementById("revealButton");
    const container = document.getElementById("container");
    const options = document.querySelectorAll(".option");
    const marryQuestion = document.getElementById("marryQuestion");

    revealButton.addEventListener("click", () => {
      container.style.display = "block"; // Exibe a mensagem ao clicar no botão
      createConfetti();
    });

    marryQuestion.addEventListener("mouseover", () => {
      marryQuestion.style.transform = "translateX(20px)";
    });

    marryQuestion.addEventListener("mouseout", () => {
      marryQuestion.style.transform = "translateX(0)";
    });

    function createConfetti() {
      for (let i = 0; i < 50; i++) {
        const confetti = document.createElement("div");
        confetti.className = "confetti";
        confetti.style.left = Math.random() * window.innerWidth + "px";
        confetti.style.animationDuration = Math.random() * 3 + 2 + "s";
        document.body.appendChild(confetti);
      }
    }
  </script>
</body>
</html>

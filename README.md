<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <title>Für Jess ❤️</title>
  <style>
    /* Body & Schrift */
    body {
      margin: 0;
      background: #b3e5fc; /* babyblau */
      overflow: hidden;
      font-family: Arial, sans-serif;
      text-align: center;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    h1 {
      color: white;
      margin-top: 30px;
      font-size: 50px;
    }

    /* Otter */
    .otter {
      position: absolute;
      width: 120px;
      cursor: pointer;
      animation: float 3s ease-in-out infinite;
    }

    @keyframes float {
      0% { transform: translateY(0); }
      50% { transform: translateY(-25px); }
      100% { transform: translateY(0); }
    }

    /* Liebesnachricht */
    #message {
      display: none;
      font-size: 42px;
      color: #ff4d6d;
      margin-top: 80px;
      animation: glow 1.5s infinite alternate;
    }

    @keyframes glow {
      from { text-shadow: 0 0 10px white; }
      to { text-shadow: 0 0 25px pink; }
    }

    /* Herzregen */
    .heart {
      position: absolute;
      color: red;
      font-size: 24px;
      animation: fall 3s linear forwards;
    }

    @keyframes fall {
      to { transform: translateY(100vh); opacity: 0; }
    }
  </style>
</head>

<body>

  <h1>Klicke alle Otter 🦦</h1>

  <!-- 2 Otter -->
  <img src="images/Otter.png1" class="otter" style="top:80px; left:100px;" onclick="clickOtter(this)">
  <img src="images/Otter.png1" class="otter" style="top:200px; left:300px;" onclick="clickOtter(this)">

  <div id="message">Jess ich liebe dich über alles! ❤️❤️❤️</div>

  <script>
    let count = 0;

    function clickOtter(otter) {
      // Herz-Explosion beim Klick
      for (let i = 0; i < 2; i++) {
        let heart = document.createElement("div");
        heart.innerHTML = "❤️";
        heart.className = "heart";
        heart.style.left = otter.offsetLeft + "px";
        heart.style.top = otter.offsetTop + "px";
        document.body.appendChild(heart);
        setTimeout(() => heart.remove(), 3000);
      }

      otter.style.display = "none";
      count++;

      if (count === 2) {
        document.getElementById("message").style.display = "block";
        // Hintergrund wird rosa
        setTimeout(() => {
          document.body.style.background = "#ffc0cb";
          heartRain();
        }, 1200);
      }
    }

    // Herzregen
    function heartRain() {
      setInterval(() => {
        let heart = document.createElement("div");
        heart.innerHTML = "❤️";
        heart.className = "heart";
        heart.style.left = Math.random() * window.innerWidth + "px";
        heart.style.top = "-20px";
        document.body.appendChild(heart);
        setTimeout(() => heart.remove(), 3000);
      }, 200);
    }
  </script>

</body>
</html>

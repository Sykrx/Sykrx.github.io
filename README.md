# Sykrx.github.io
<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<title>Für Jessica ❤️</title>

<style>
body {
  background: linear-gradient(to bottom, #ff9a9e, #fad0c4);
  font-family: Arial, sans-serif;
  text-align: center;
  overflow: hidden;
}

h1 {
  margin-top: 80px;
  font-size: 40px;
  color: white;
}

button {
  padding: 15px 30px;
  font-size: 20px;
  margin: 20px;
  border: none;
  border-radius: 12px;
  cursor: pointer;
}

#yes {
  background: #ff4d6d;
  color: white;
}

#no {
  background: #444;
  color: white;
  position: absolute;
}

#heartScene {
  display: none;
  font-size: 28px;
  color: white;
  margin-top: 60px;
  animation: float 3s infinite alternate ease-in-out;
}

@keyframes float {
  from { transform: translateY(0px); }
  to { transform: translateY(-30px); }
}
</style>
</head>

<body>

<h1>Jessica Schaar ❤️<br>Liebst du deinen Otter?</h1>

<button id="yes" onclick="showLove()">JA 💖</button>
<button id="no" onmouseover="moveNo()">NEIN 😈</button>

<div id="heartScene">
  🦦💞🦦<br>
  Für Jessica — die Liebe meines Lebens ❤️
</div>

<script>
let moves = 0;

function moveNo() {
  const btn = document.getElementById("no");
  const x = Math.random() * (window.innerWidth - 100);
  const y = Math.random() * (window.innerHeight - 100);

  btn.style.left = x + "px";
  btn.style.top = y + "px";

  moves++;
  btn.style.transform = "scale(" + (1 - moves * 0.15) + ")";

  if (moves >= 5) {
    btn.style.display = "none";
  }
}

function showLove() {
  document.getElementById("yes").style.display = "none";
  document.getElementById("no").style.display = "none";
  document.getElementById("heartScene").style.display = "block";
}
</script>

</body>

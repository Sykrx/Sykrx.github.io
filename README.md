<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<title>Für Jessica ❤️</title>
<style>
body {
  margin: 0;
  padding: 0;
  background-color: #b3e5fc; /* Babyblauer Hintergrund */
  overflow: hidden;
  font-family: Arial, sans-serif;
  text-align: center;
}

.otter {
  position: absolute;
  width: 100px; /* Größe der Otter */
  cursor: pointer;
  transition: transform 0.3s;
}

.otter:hover {
  transform: scale(1.1);
}

#message {
  display: none;
  font-size: 36px;
  color: #ff4d6d;
  margin-top: 50px;
}

</style>
</head>
<body>

<h1>Finde alle Otter und klicke sie! 🦦</h1>

<!-- Otter-Bilder einfügen -->
<img src="otter.png" class="otter" style="top:50px; left:100px;" onclick="clickOtter(this)">
<img src="otter.png" class="otter" style="top:150px; left:300px;" onclick="clickOtter(this)">
<img src="otter.png" class="otter" style="top:250px; left:500px;" onclick="clickOtter(this)">
<img src="otter.png" class="otter" style="top:350px; left:200px;" onclick="clickOtter(this)">
<img src="otter.png" class="otter" style="top:100px; left:600px;" onclick="clickOtter(this)">
<img src="otter.png" class="otter" style="top:400px; left:400px;" onclick="clickOtter(this)">

<div id="message">Jess, ich liebe dich über alles! ❤️❤️❤️</div>

<script>
let ottersClicked = 0;

function clickOtter(otter) {
  otter.style.display = 'none'; // Otter verschwindet
  ottersClicked++;
  
  if (ottersClicked === 6) { // Alle Otter geklickt
    document.getElementById('message').style.display = 'block';
    setTimeout(() => {
      // Weiterleitung zur rosa Seite
      window.location.href = 'rosa.html'; // <-- Hier deine rosa Seite angeben
    }, 2000); // 2 Sekunden warten
  }
}
</script>

</body>
</html>

<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<title>Rosa Seite</title>
<style>
body { background-color: #ffc0cb; text-align:center; font-family:Arial; }
h1 { margin-top:50px; color:#fff; }
</style>
</head>
<body>
<h1>Für Jessica ❤️</h1>
<p>Danke, dass du so süß bist 😘</p>
</body>

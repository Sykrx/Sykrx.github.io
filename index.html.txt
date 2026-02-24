<!DOCTYPE html>
<html>
<head>
  <title>Meine Website</title>
  <style>
    .otter { width: 100px; cursor: pointer; }
    #menu { display: none; }
  </style>
</head>
<body>

<div id="otter-container">
  <img src="otter1.png" class="otter">
  <img src="otter2.png" class="otter">
  <img src="otter3.png" class="otter">
  <img src="otter4.png" class="otter">
  <img src="otter5.png" class="otter">
  <img src="otter6.png" class="otter">
</div>

<div id="menu">
  <h1>Hauptmenü</h1>
  <ul>
    <li onclick="openSection('erinnerungen')">Erinnerungsbilder</li>
    <li onclick="openSection('liebesnachrichten')">Liebesnachrichten</li>
    <li onclick="openSection('musik')">Musik</li>
    <li onclick="openSection('videos')">Videos</li>
    <li onclick="openSection('überraschungen')">Überraschungen</li>
  </ul>
</div>

<div id="erinnerungen" style="display:none;">Hier deine Erinnerungsbilder...</div>
<div id="liebesnachrichten" style="display:none;">Hier deine Liebesnachrichten...</div>

<script>
let otters = document.querySelectorAll('.otter');
let clicked = 0;

otters.forEach(otter => {
  otter.addEventListener('click', () => {
    otter.style.display = 'none';
    clicked++;
    if(clicked === 6) {
      document.getElementById('otter-container').style.display = 'none';
      document.getElementById('menu').style.display = 'block';
    }
  });
});

function openSection(id) {
  document.querySelectorAll('div[id]').forEach(d => d.style.display = 'none');
  document.getElementById('menu').style.display = 'block';
  document.getElementById(id).style.display = 'block';
}
</script>

</body>
</html>

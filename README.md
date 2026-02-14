<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Galaxia de Amor 💫</title>
<style>
body {
  margin:0;
  padding:0;
  background:black;
  overflow:hidden;
  font-family: Arial, sans-serif;
}

/* Estrellas de fondo */
.estrella {
  position:absolute;
  width:2px;
  height:2px;
  background:white;
  border-radius:50%;
  animation: moverEstrella linear infinite;
}

@keyframes moverEstrella {
  0% { transform: translateY(0); }
  100% { transform: translateY(1000px); }
}

/* Galaxia central */
.galaxia {
  position:absolute;
  top:50%;
  left:50%;
  width:250px;
  height:250px;
  margin-left:-125px;
  margin-top:-125px;
  border-radius:50%;
  background: radial-gradient(circle, #8a6cff, #2b0a55, black);
  box-shadow:0 0 100px #8a6cff;
}

/* Contenedor del texto giratorio */
.orbita {
  position:absolute;
  top:50%;
  left:50%;
  width:500px;
  height:500px;
  margin-left:-250px;
  margin-top:-250px;
  animation:girar 60s linear infinite;
}

@keyframes girar {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}

.orbita span {
  position:absolute;
  left:50%;
  top:50%;
  transform-origin:0 0;
  white-space:nowrap;
  font-size:16px;
  color:#ff6b6b;
}
</style>
</head>
<body>

<div class="galaxia"></div>
<div class="orbita" id="orbita"></div>

<script>
const idiomas = [
"Te amo ❤️", "I love you ❤️", "Je t'aime ❤️", "Ti amo ❤️", "Ich liebe dich ❤️",
"Eu te amo ❤️", "Я тебя люблю ❤️", "我爱你 ❤️", "사랑해 ❤️", "Te iubesc ❤️",
"Σ'αγαπώ ❤️", "Mahal kita ❤️", "Ik hou van jou ❤️", "Aishiteru ❤️",
"Aku cinta kamu ❤️", "Jag älskar dig ❤️", "Jeg elsker dig ❤️", "S'agapo ❤️",
"Kocham cię ❤️", "Te quiero ❤️", "Ana behibak ❤️", "Main tumse pyaar karta hoon ❤️",
"Ngiyakuthanda ❤️", "Ek het jou lief ❤️", "Mi amas vin ❤️", "Ke aloha au iā ʻoe ❤️"
];

const orbita = document.getElementById("orbita");
const radio = 220;
const total = idiomas.length;

idiomas.forEach((texto, i) => {
  const span = document.createElement("span");
  span.innerText = texto;
  const angulo = (360 / total) * i;
  span.style.transform = `rotate(${angulo}deg) translate(${radio}px) rotate(-${angulo}deg)`;
  orbita.appendChild(span);
});

// Crear estrellas
for (let i=0;i<150;i++){
  const estrella = document.createElement("div");
  estrella.className="estrella";
  estrella.style.top = Math.random() * window.innerHeight + "px";
  estrella.style.left = Math.random() * window.innerWidth + "px";
  estrella.style.width = (Math.random()*2+1)+"px";
  estrella.style.height = (Math.random()*2+1)+"px";
  estrella.style.opacity = Math.random();
  estrella.style.animationDuration = (Math.random()*10+5)+"s";
  document.body.appendChild(estrella);
}
</script>

</body>
</html># Nuestra-galaxia-

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy New Year 🎉</title>
<style>
body {
    margin: 0;
    background: black;
    color: gold;
    text-align: center;
    font-family: Arial;
    overflow: hidden;
}
h1 {
    margin-top: 100px;
    font-size: 55px;
}
h2 {
    font-size: 26px;
    color: white;
}
p {
    font-size: 20px;
    color: #ddd;
}
button {
    margin-top: 30px;
    padding: 15px 30px;
    font-size: 18px;
    border: none;
    border-radius: 8px;
    background: gold;
    cursor: pointer;
}
canvas {
    position: fixed;
    top: 0;
    left: 0;
}
</style>
</head>

<body>
<canvas id="canvas"></canvas>

<h1>🎊 Happy New Year 2026 🎊</h1>
<h2>✨ Wishes from <b>Jitesh</b> ✨</h2>
<p>May this year bring you happiness, success & peace 💖</p>

<button onclick="startCelebration()">🎆 Start Celebration</button>

<!-- Sounds -->
<audio id="fireSound" loop>
  <source src="https://www.soundjay.com/explosion/fireworks-1.mp3" type="audio/mpeg">
</audio>

<audio id="bgMusic" loop>
  <source src="https://www.soundjay.com/misc/sounds/bell-ringing-05.mp3" type="audio/mpeg">
</audio>

<script>
const canvas = document.getElementById("canvas");
const ctx = canvas.getContext("2d");
canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

function firework() {
    const x = Math.random() * canvas.width;
    const y = Math.random() * canvas.height / 2;
    for (let i = 0; i < 120; i++) {
        ctx.beginPath();
        ctx.arc(
            x + Math.random()*120 - 60,
            y + Math.random()*120 - 60,
            2,
            0,
            Math.PI*2
        );
        ctx.fillStyle = `hsl(${Math.random()*360},100%,50%)`;
        ctx.fill();
    }
}

setInterval(() => {
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    firework();
}, 500);

function startCelebration() {
    document.getElementById("fireSound").play();
    document.getElementById("bgMusic").play();
}
</script>

</body>
</html>

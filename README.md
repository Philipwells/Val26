<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>For My Love 💖</title>

<style>

body {
  margin: 0;
  padding: 0;
  background: linear-gradient(to bottom right, #ff5f9e, #ffb3d9);
  font-family: 'Segoe UI', sans-serif;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: white;
  overflow: hidden;
}

.container {
  max-width: 600px;
  padding: 25px;
  animation: fadeIn 2s ease;
}

h1 {
  font-size: 2.5em;
  margin-bottom: 10px;
}

h2 {
  font-weight: normal;
  margin-bottom: 20px;
}

p {
  font-size: 1.2em;
  line-height: 1.6;
  min-height: 80px;
}

button {
  margin-top: 25px;
  padding: 12px 28px;
  border: none;
  border-radius: 30px;
  background: white;
  color: #ff3f7f;
  font-size: 1em;
  cursor: pointer;
  transition: 0.3s;
}

button:hover {
  background: #ffe0ec;
  transform: scale(1.05);
}

.heart {
  position: absolute;
  bottom: -20px;
  font-size: 20px;
  animation: float 6s linear infinite;
  opacity: 0.8;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(40px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes float {
  from {
    transform: translateY(0);
  }
  to {
    transform: translateY(-110vh);
  }
}

</style>
</head>

<body>

<div class="container">

  <h1>💖 Boluwatife 💖</h1>
  <h2>From Olawale</h2>

  <p id="text">
    My love, you are the best thing that ever happened to me.
  </p>

  <button onclick="nextText()">Tap Me ❤️</button>

</div>

<script>

const messages = [

  "My love, you are the best thing that ever happened to me.",

  "Every day I wake up grateful that you are in my life.",

  "Your smile makes my heart beat faster.",

  "With you, I feel safe, happy, and complete.",

  "No matter what happens, I will always choose you.",

  "You are my peace in chaos.",

  "You are my happiness in sadness.",

  "You are my forever and always.",

  "I promise to love you sincerely.",

  "Today, tomorrow, and forever... I love you 💕"

];

let i = 0;

function nextText() {

  i++;

  if (i >= messages.length) {
    i = 0;
  }

  document.getElementById("text").innerText = messages[i];

  createHeart();
}

function createHeart() {

  const heart = document.createElement("div");

  heart.className = "heart";

  heart.innerHTML = "❤️";

  heart.style.left = Math.random() * 100 + "vw";

  heart.style.fontSize = (Math.random() * 20 + 15) + "px";

  document.body.appendChild(heart);

  setTimeout(() => {
    heart.remove();
  }, 6000);

}

</script>

</body>
</html>

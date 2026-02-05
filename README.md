# Valentine.html-2
Sadu
<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Happy Valentine My Love 💖</title>
  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(180deg, #ffb6c1, #ffc0cb);
      height: 100vh;
      overflow: hidden;
      color: #ff2e63;
    }.slides {
  display: flex;
  width: 500vw;
  height: 100vh;
  transition: transform 0.6s ease;
}

.slide {
  width: 100vw;
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 20px;
}

h1 {
  font-size: 2.3rem;
  margin-bottom: 10px;
}

p {
  font-size: 1.2rem;
  max-width: 320px;
}

.buttons {
  margin-top: 25px;
  display: flex;
  gap: 15px;
}

button {
  padding: 12px 22px;
  border-radius: 25px;
  border: none;
  font-size: 1rem;
  cursor: pointer;
  background: #ff2e63;
  color: white;
  box-shadow: 0 4px 10px rgba(0,0,0,0.2);
}

button.secondary {
  background: white;
  color: #ff2e63;
}

.heart {
  position: fixed;
  bottom: -20px;
  font-size: 22px;
  animation: floatUp 6s linear infinite;
  opacity: 0.8;
}

@keyframes floatUp {
  0% { transform: translateY(0); opacity: 0; }
  10% { opacity: 1; }
  100% { transform: translateY(-110vh); opacity: 0; }
}

.photo {
  width: 220px;
  height: 220px;
  border-radius: 20px;
  background: white;
  margin-bottom: 15px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.9rem;
  color: #999;
}

.kitty {
  font-size: 3rem;
  margin-bottom: 10px;
}

  </style>
</head>
<body>  <!-- Background Music -->  <audio id="music" autoplay loop>
    <!-- Replace song.mp3 with your romantic song file -->
    <source src="song.mp3" type="audio/mpeg">
  </audio>  <div class="slides" id="slides"><!-- Slide 1 -->
<div class="slide">
  <div class="kitty">🎀😺</div>
  <h1>Hey My Hello Kitty 💕</h1>
  <p>I made something special for you… just us 🥹</p>
  <div class="buttons">
    <button onclick="next()">Yes 💖</button>
  </div>
</div>

<!-- Slide 2 -->
<div class="slide">
  <h1>Happy Valentine’s Day 🌹</h1>
  <p>You are my favorite person, my comfort, my home.</p>
  <div class="buttons">
    <button class="secondary" onclick="prev()">⬅ Back</button>
    <button onclick="next()">Next 💌</button>
  </div>
</div>

<!-- Slide 3 (Photos) -->
<div class="slide">
  <h1>Us 🥰</h1>
  <div class="photo">Add our photo here</div>
  <div class="photo">Add our photo here</div>
  <div class="buttons">
    <button class="secondary" onclick="prev()">⬅ Back</button>
    <button onclick="next()">Next 💕</button>
  </div>
</div>

<!-- Slide 4 -->
<div class="slide">
  <h1>My Love 💖</h1>
  <p>I choose you today, tomorrow, and always. Forever us.</p>
  <div class="buttons">
    <button class="secondary" onclick="prev()">⬅ Back</button>
    <button onclick="next()">Next 💍</button>
  </div>
</div>

<!-- Slide 5 -->
<div class="slide">
  <div class="kitty">🎀😺</div>
  <h1>Will you be my Valentine? 💌</h1>
  <div class="buttons">
    <button onclick="alert('Yay! I love you 😭💖')">YES 💖</button>
    <button class="secondary" onclick="alert('Too bad 😌 You are mine anyway 😘')">NO 🙈</button>
  </div>
</div>

  </div>  <script>
    let index = 0;
    const slides = document.getElementById('slides');

    function update() {
      slides.style.transform = `translateX(-${index * 100}vw)`;
    }

    function next() {
      if (index < 4) index++;
      update();
    }

    function prev() {
      if (index > 0) index--;
      update();
    }

    function createHeart() {
      const heart = document.createElement('div');
      heart.className = 'heart';
      heart.innerText = '💖';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = (4 + Math.random() * 3) + 's';
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 7000);
    }

    setInterval(createHeart, 400);
  </script></body>
</html>

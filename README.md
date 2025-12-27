<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Happy Birthday Vrunda 🎂</title>
  <style>
    body {
      margin: 0;
      font-family: 'Comic Sans MS', cursive, sans-serif;
      background: linear-gradient(135deg, #ffd6e8, #fff);
      text-align: center;
      color: #ff4d88;
    }
    .container {
      padding: 20px;
    }
    h1 {
      font-size: 2.5rem;
      margin-top: 20px;
    }
    h2 {
      font-size: 1.5rem;
    }
    .card {
      background: white;
      border-radius: 20px;
      padding: 20px;
      margin: 20px auto;
      max-width: 350px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.1);
    }
    button {
      background: #ff4d88;
      border: none;
      padding: 12px 20px;
      color: white;
      border-radius: 25px;
      font-size: 1rem;
      cursor: pointer;
      margin-top: 10px;
    }
    button:hover {
      background: #ff1a66;
    }
    .hidden {
      display: none;
    }
    #countdown {
      font-size: 1.2rem;
      margin-top: 10px;
      color: #ff3385;
    }
    .heart {
      font-size: 2rem;
      animation: float 1.5s infinite;
    }
    @keyframes float {
      0% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
      100% { transform: translateY(0); }
    }
  </style>
</head>
<body>
  <audio autoplay loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
  </audio>

  <div class="container">
    <h1>🎉 Happy Birthday Vrunda 🎉</h1>
    <div class="heart">💖💖💖</div>

    <div class="card">
      <h2>🎂 Special Day: 26 January</h2>
      <div id="countdown"></div>
    </div>

    <div class="card">
      <h2>💌 Birthday Wish</h2>
      <p>Dear Vrunda 💕<br>
      Tumhari smile duniya ki sabse cute cheez hai 😄<br>
      Aaj ka din sirf tumhare liye hai 🎈<br>
      Hamesha khush raho ✨</p>
    </div>

    <div class="card">
      <button onclick="showSurprise()">🎁 Click for Surprise</button>
      <p id="surprise" class="hidden">
        🌸 Tum meri zindagi ka ek bahut hi special hissa ho 💖<br>
        Thank you for being you 🥰<br><br>
        — From Smeet 💌
      </p>
    </div>
  </div>

  <script>
    const birthday = new Date("January 26, 2026 00:00:00").getTime();

    setInterval(() => {
      const now = new Date().getTime();
      const diff = birthday - now;

      const days = Math.floor(diff / (1000 * 60 * 60 * 24));
      const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
      const seconds = Math.floor((diff % (1000 * 60)) / 1000);

      document.getElementById("countdown").innerHTML =
        `⏳ ${days}d ${hours}h ${minutes}m ${seconds}s left`;
    }, 1000);

    function showSurprise() {
      document.getElementById("surprise").classList.remove("hidden");
    }
  </script>
</body>
</html>

<!DOCTYPE html>  
<html lang="en">  
<head>  
  <meta charset="UTF-8">  
  <title>For Rishu ❤️</title>  
  <style>  
    body {  
      margin: 0;  
      height: 100vh;  
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);  
      display: flex;  
      align-items: center;  
      justify-content: center;  
      font-family: 'Comic Sans MS', cursive;  
      overflow: hidden;  
    }  
  
    .card {  
      background: white;  
      padding: 30px 40px;  
      border-radius: 20px;  
      text-align: center;  
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);  
      z-index: 2;  
      position: relative;  
    }  
  
    h1 {  
      color: #ff4d6d;  
      margin-bottom: 10px;  
    }  
  
    p {  
      color: #555;  
      margin-bottom: 25px;  
    }  
  
    button {  
      font-size: 18px;  
      padding: 12px 25px;  
      margin: 10px;  
      border: none;  
      border-radius: 30px;  
      cursor: pointer;  
      transition: transform 0.2s;  
      position: relative;  
    }  
  
    button:hover {  
      transform: scale(1.1);  
    }  
  
    .yes {  
      background: #ff4d6d;  
      color: white;  
    }  
  
    .no {  
      background: #ccc;  
      color: #333;  
      position: absolute;  
    }  
  
    .heart {  
      position: absolute;  
      color: rgba(255, 77, 109, 0.6);  
      font-size: 20px;  
      animation: float 6s infinite;  
    }  
  
    @keyframes float {  
      0% {  
        transform: translateY(100vh) scale(0.8);  
        opacity: 0;  
      }  
      50% {  
        opacity: 1;  
      }  
      100% {  
        transform: translateY(-10vh) scale(1.2);  
        opacity: 0;  
      }  
    }  
  </style>  
</head>  
<body>  
  
  <div class="card">  
    <h1>💌 Rishu, will you be my Valentine? 💌</h1>  
    <p>  
      No matter the distance,<br>  
      my heart always finds its way to you 💕<br>  
      Today, tomorrow, always.  
    </p>  
  
    <button class="yes"  
      onclick="location.href='https://wa.me/?text=YES%20I%20will%20be%20your%20Valentine%20forever%20💖💘🥰'">  
      YES 💖  
    </button>  
  
    <button class="no" id="noBtn">  
      No 😢  
    </button>  
  </div>  
  
  <!-- Floating Hearts -->  
  <script>  
    const hearts = ['💖','💘','💕','💗','❤️'];  
    for (let i = 0; i < 25; i++) {  
      const heart = document.createElement('div');  
      heart.className = 'heart';  
      heart.innerText = hearts[Math.floor(Math.random() * hearts.length)];  
      heart.style.left = Math.random() * 100 + 'vw';  
      heart.style.animationDelay = Math.random() * 5 + 's';  
      heart.style.fontSize = 16 + Math.random() * 24 + 'px';  
      document.body.appendChild(heart);  
    }  
  
    // Runaway NO button 😈  
    const noBtn = document.getElementById('noBtn');  
    noBtn.addEventListener('mouseover', () => {  
      const x = Math.random() * 200 - 100;  
      const y = Math.random() * 200 - 100;  
      noBtn.style.transform = `translate(${x}px, ${y}px)`;  
    });  
  </script>  
  
</body>  
</html>  

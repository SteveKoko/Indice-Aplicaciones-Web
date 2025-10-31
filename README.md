<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>🌐 Mis Prácticas de Clase</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');

    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #1f1c2c, #928dab);
      color: white;
      overflow-x: hidden;
      min-height: 100vh;
    }

    header {
      text-align: center;
      padding: 50px 20px;
      position: relative;
      z-index: 10;
    }

    header h1 {
      font-size: 3em;
      margin-bottom: 10px;
      animation: fadeDown 1.2s ease;
    }

    header p {
      font-size: 1.2em;
      opacity: 0.8;
      animation: fadeIn 2s ease;
    }

    .container {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-wrap: wrap;
      gap: 30px;
      padding: 40px;
      position: relative;
      z-index: 10;
    }

    .card {
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(8px);
      border-radius: 20px;
      padding: 30px;
      width: 220px;
      text-align: center;
      color: white;
      transition: transform 0.4s ease, background 0.3s;
      cursor: pointer;
      animation: float 5s ease-in-out infinite;
    }

    .card:hover {
      transform: translateY(-10px) scale(1.05);
      background: rgba(255, 255, 255, 0.25);
    }

    .card img {
      width: 80px;
      height: 80px;
      margin-bottom: 15px;
      transition: transform 0.4s ease;
    }

    .card:hover img {
      transform: rotate(10deg) scale(1.1);
    }

    .card h2 {
      margin-bottom: 10px;
      font-size: 1.3em;
    }

    .card p {
      font-size: 0.95em;
      opacity: 0.9;
    }

    footer {
      text-align: center;
      padding: 20px;
      font-size: 0.9em;
      opacity: 0.8;
      z-index: 10;
      position: relative;
    }

    #bubbles {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 1;
      overflow: hidden;
      background: radial-gradient(ellipse at bottom, #1b2735 0%, #090a0f 100%);
    }

    .bubble {
      position: absolute;
      bottom: -100px;
      background: rgba(255, 255, 255, 0.15);
      border-radius: 50%;
      animation: rise 8s infinite ease-in;
    }

    @keyframes rise {
      0% { transform: translateY(0) scale(1); opacity: 1; }
      100% { transform: translateY(-1200px) scale(1.5); opacity: 0; }
    }

    @keyframes fadeDown {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
  </style>
</head>
<body>
  <div id="bubbles"></div>

  <header>
    <h1>💻 Mis Prácticas de Clase</h1>
    <p>Repositorio con ejemplos de HTML, CSS y JavaScript</p>
  </header>

  <main class="container">
    <div class="card">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="HTML Logo">
      <h2>HTML</h2>
      <p>Estructura básica de páginas web</p>
    </div>
    <div class="card">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" alt="CSS Logo">
      <h2>CSS</h2>
      <p>Diseños y animaciones con estilo</p>
    </div>
    <div class="card">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" alt="JS Logo">
      <h2>JavaScript</h2>
      <p>Interactividad y dinamismo</p>
    </div>
  </main>

  <footer>
    ✨ Diseñado con cariño y código por <b>TuNombre</b> 💫
  </footer>

  <script>
    const bubbleContainer = document.getElementById('bubbles');
    const numBubbles = 30;

    for (let i = 0; i < numBubbles; i++) {
      const bubble = document.createElement('div');
      bubble.classList.add('bubble');
      const size = Math.random() * 80 + 20 + 'px';
      bubble.style.width = size;
      bubble.style.height = size;
      bubble.style.left = Math.random() * 100 + '%';
      bubble.style.animationDuration = 6 + Math.random() * 4 + 's';
      bubble.style.animationDelay = Math.random() * 5 + 's';
      bubbleContainer.appendChild(bubble);
    }
  </script>
</body>
</html>

    html, body {
      margin: 0;
      padding: 0;
      font-family: 'Poppins', sans-serif;
      background: #000;
      color: #fff;
      overflow: hidden;
    }

    body {
      display: flex;
      flex-direction: column;
      align-items: center;
      min-height: 100vh;
      position: relative;
      z-index: 1;
      padding: 40px 20px;
    }

    /* Fundo com partículas */
    .background {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: #000;
      z-index: 0;
      overflow: hidden;
    }

    .particle {
      position: absolute;
      width: 3px;
      height: 3px;
      background: #0ff;
      border-radius: 50%;
      opacity: 0.6;
      animation: float 10s linear infinite;
    }

    @keyframes float {
      0% { transform: translateY(100vh) scale(0.5); opacity: 0.3; }
      100% { transform: translateY(-10vh) scale(1); opacity: 0; }
    }

    header {
      z-index: 2;
      max-width: 600px;
      text-align: center;
      margin-bottom: 50px;
    }

    .neon-title {
      font-size: 2.2rem;
      font-weight: 700;
      margin: 0;
      background: linear-gradient(90deg, #00fff7, #6e00ff, #ff00cc);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      text-shadow: 0 0 10px rgba(0,255,255,0.2), 0 0 20px rgba(110,0,255,0.2);
      animation: floatText 4s ease-in-out infinite;
      text-align: center;
    }

    @keyframes floatText {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }

    main {
      z-index: 2;
      display: flex;
      flex-direction: column;
      gap: 20px;
      align-items: center;
      width: 100%;
    }

    .button-wrapper {
      position: relative;
      display: inline-block;
    }

    .button-wrapper::before {
      content: "";
      position: absolute;
      top: -6px;
      left: -6px;
      right: -6px;
      bottom: -6px;
      border-radius: 40px;
      background: conic-gradient(white, transparent, white);
      animation: spin 2s linear infinite;
      z-index: -1;
      filter: blur(4px);
    }

    @keyframes spin {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }

    a.button-link {
      background: #111;
      color: #fff;
      text-decoration: none;
      font-weight: 500;
      padding: 10px 24px;
      border-radius: 30px;
      text-align: center;
      font-size: 1rem;
      border: 1px solid #333;
      transition: 0.3s ease;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      position: relative;
      z-index: 1;
    }

    a.button-link:hover {
      background: #222;
      transform: translateY(-2px);
    }

    .icon-chat {
      width: 18px;
      height: 18px;
      background: url('https://upload.wikimedia.org/wikipedia/commons/0/04/ChatGPT_logo.svg') no-repeat center;
      background-size: contain;
      display: inline-block;
    }

    footer {
      z-index: 2;
      margin-top: auto;
      padding: 15px;
      font-size: 0.9rem;
      color: rgba(255,255,255,0.4);
      text-align: center;
    }

    @media (max-width: 640px) {
      .neon-title {
        font-size: 1.6rem;
      }

      a.button-link {
        font-size: 0.95rem;
        padding: 8px 18px;
      }

      .button-wrapper::before {
        top: -4px; left: -4px; right: -4px; bottom: -4px;
      }
    }
  </style>
</head>
<body>
  <div class="background" id="particles"></div>

  <header>
    <h1 class="neon-title">Aprenda a Lucrar com IA</h1>
  </header>

  <main>
    <div class="button-wrapper">
      <a href="#" class="button-link">
        <span class="icon-chat"></span>
        Geração Prompt
      </a>
    </div>
    <div class="button-wrapper">
      <a href="#" class="button-link">Link 2</a>
    </div>
    <div class="button-wrapper">
      <a href="#" class="button-link">Link 3</a>
    </div>
    <div class="button-wrapper">
      <a href="#" class="button-link">Link 4</a>
    </div>
  </main>

  <footer>
    © 2025 Seus eBooks. Todos os direitos reservados.
  </footer>

  <script>
    // Geração de partículas no fundo
    const particlesContainer = document.getElementById('particles');
    for (let i = 0; i < 80; i++) {
      const particle = document.createElement('div');
      particle.className = 'particle';
      particle.style.left = ${Math.random() * 100}%;
      particle.style.top = ${Math.random() * 100}vh;
      particle.style.animationDuration = ${6 + Math.random() * 6}s;
      particlesContainer.appendChild(particle);
    }
  </script>
</body>
</html>

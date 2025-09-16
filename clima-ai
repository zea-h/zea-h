<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>CLIMA-AI | Luxury Smart Wear</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --blue: #004e92;
      --green: #00c9a7;
      --dark: #111;
      --light: #f8f9fa;
      --white: #ffffff;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(to right, #cdeffd, #d6fff5);
      color: #111;
      scroll-behavior: smooth;
    }

    header {
      position: fixed;
      top: 0;
      width: 100%;
      background-color: var(--blue);
      color: white;
      padding: 1rem 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      z-index: 999;
      transition: top 0.3s;
    }

    header h1 {
      font-size: 2rem;
      font-weight: 700;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin-left: 2rem;
      font-weight: 500;
      transition: opacity 0.3s;
    }

    nav a:hover {
      opacity: 0.7;
    }

    .hero {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 6rem 2rem;
      background: linear-gradient(to right, #004e92, #00c9a7);
      color: white;
    }

    .hero h2 {
      font-size: 3rem;
      font-weight: 700;
      margin-bottom: 1.5rem;
    }

    .hero p {
      max-width: 700px;
      font-size: 1.3rem;
      line-height: 1.7;
    }

    section {
      padding: 4rem 2rem;
      max-width: 1200px;
      margin: auto;
    }

    .section-title {
      font-size: 2.5rem;
      font-weight: 600;
      margin-bottom: 1.5rem;
      color: var(--blue);
      text-align: center;
    }

    .solution-text {
      font-size: 1.2rem;
      line-height: 1.8;
      background-color: var(--white);
      padding: 3rem;
      border-radius: 20px;
      box-shadow: 0 12px 30px rgba(0, 0, 0, 0.1);
      max-width: 900px;
      margin: auto;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
      margin-top: 3rem;
    }

    .card {
      background: white;
      padding: 2.5rem;
      border-radius: 15px;
      box-shadow: 0 12px 30px rgba(0, 0, 0, 0.15);
      transition: transform 0.3s;
    }

    .card:hover {
      transform: translateY(-8px);
    }

    .card h3 {
      color: var(--green);
      margin-bottom: 1rem;
      font-weight: 700;
      font-size: 1.5rem;
    }

    .card p {
      font-size: 1rem;
      color: #333;
    }

    footer {
      background-color: var(--dark);
      color: white;
      text-align: center;
      padding: 2.5rem;
      font-size: 1rem;
      margin-top: 5rem;
    }

    /* Temperature Control Section */
    .temp-control {
      text-align: center;
      margin-top: 3rem;
    }

    .slider-container {
      margin: 2rem auto;
      width: 80%;
      max-width: 500px;
    }

    input[type="range"] {
      width: 100%;
      -webkit-appearance: none;
      height: 15px;
      border-radius: 10px;
      background: linear-gradient(to right, blue, red);
      outline: none;
      transition: background 0.3s;
    }

    input[type="range"]::-webkit-slider-thumb {
      -webkit-appearance: none;
      appearance: none;
      width: 25px;
      height: 25px;
      border-radius: 50%;
      background: #fff;
      border: 3px solid var(--blue);
      cursor: pointer;
      transition: 0.3s;
    }

    input[type="range"]::-webkit-slider-thumb:hover {
      transform: scale(1.2);
    }

    .temp-display {
      font-size: 2rem;
      font-weight: bold;
      margin-top: 1rem;
      transition: color 0.3s;
    }

    .mode-buttons {
      margin-top: 2rem;
    }

    .mode-buttons button {
      margin: 0.5rem;
      padding: 0.8rem 1.5rem;
      border: none;
      border-radius: 10px;
      font-size: 1rem;
      font-weight: 600;
      cursor: pointer;
      background: var(--blue);
      color: white;
      transition: 0.3s;
    }

    .mode-buttons button:hover {
      opacity: 0.8;
      transform: scale(1.05);
    }

    /* Dashboard Section */
    .dashboard {
      background: white;
      border-radius: 15px;
      box-shadow: 0 8px 25px rgba(0,0,0,0.1);
      padding: 2rem;
      margin-top: 4rem;
    }

    .dashboard h3 {
      color: var(--blue);
      margin-bottom: 1.5rem;
      text-align: center;
    }

    .dashboard-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1.5rem;
    }

    .dashboard-card {
      background: var(--light);
      padding: 1.5rem;
      border-radius: 10px;
      text-align: center;
      box-shadow: 0 4px 15px rgba(0,0,0,0.05);
    }

    .dashboard-card h4 {
      font-size: 1.2rem;
      margin-bottom: 0.5rem;
      color: var(--green);
    }

    canvas {
      max-width: 100%;
      height: 200px !important; /* keeps charts neat */
    }

    /* Header hide/show on scroll */
    .hide {
      top: -100px;
    }
  </style>
</head>
<body>

  <header id="mainHeader">
    <h1>CLIMA-AI</h1>
    <nav>
      <a href="#problem">The Problem</a>
      <a href="#solution">Our Solution</a>
      <a href="#features">Features</a>
      <a href="#control">Temperature Control</a>
      <a href="#dashboard">Dashboard</a>
    </nav>
  </header>

  <section class="hero">
    <h2>The Future of Smart Comfort</h2>
    <p>Discover CLIMA-AI — the luxury wearable clothing that adjusts to your body’s needs, keeping you in perfect comfort no matter the temperature.</p>
  </section>

  <section id="problem">
    <h2 class="section-title">Why CLIMA-AI?</h2>
    <p class="solution-text">
      Traditional clothing can’t adapt to the varying temperatures and body conditions we face. Whether it’s the summer sun or winter chill, existing clothes often leave us feeling uncomfortable and inefficient. It’s time to experience the future of wearable technology.
    </p>
  </section>

  <section id="solution">
    <h2 class="section-title">Experience the Innovation</h2>
    <p class="solution-text">
      CLIMA-AI isn't just clothing—it's an experience. Designed with the latest AI technology, it intelligently adjusts your body temperature in real-time, ensuring comfort wherever you go. Whether you’re at work, traveling, or relaxing, CLIMA-AI learns your preferences, adapting to your unique needs without lifting a finger.
    </p>
  </section>

  <section id="features">
    <h2 class="section-title">What Makes CLIMA-AI Special?</h2>
    <div class="grid">
      <div class="card">
        <h3>🔥❄ Adaptive Comfort</h3>
        <p>Real-time temperature adjustments based on your environment and body.</p>
      </div>
      <div class="card">
        <h3>🧠 AI Powered</h3>
        <p>Continuous learning to adapt to your daily activity and preferences.</p>
      </div>
      <div class="card">
        <h3>📱 Seamless Control</h3>
        <p>Control everything via an intuitive mobile app for maximum ease.</p>
      </div>
      <div class="card">
        <h3>🔋 Energy Efficient</h3>
        <p>Save energy with smart zones that activate only when necessary.</p>
      </div>
      <div class="card">
        <h3>💎 Premium Design</h3>
        <p>Lightweight, sleek, and durable — a stylish, modern wardrobe essential.</p>
      </div>
      <div class="card">
        <h3>💚 Future of Fashion</h3>
        <p>The luxury smart garment that takes you into the next generation of wearables.</p>
      </div>
    </div>
  </section>

  <!-- Interactive Temperature Control -->
  <section id="control">
    <h2 class="section-title">Manual Temperature Control & Modes</h2>
    <div class="temp-control">
      <p>Drag the slider or select a mode to set your comfort temperature.</p>
      <div class="slider-container">
        <input type="range" min="10" max="40" value="25" id="tempSlider">
      </div>
      <div id="tempDisplay" class="temp-display">25°C</div>

      <div class="mode-buttons">
        <button onclick="setMode('Active')">🏃 Active</button>
        <button onclick="setMode('Rest')">🛋 Rest</button>
        <button onclick="setMode('Outdoor')">🌳 Outdoor</button>
        <button onclick="setMode('Indoor')">🏠 Indoor</button>
      </div>
    </div>
  </section>

  <!-- Dashboard Section -->
  <section id="dashboard">
    <h2 class="section-title">Smart Dashboard</h2>
    <div class="dashboard">
      <h3>Live Monitoring</h3>
      <div class="dashboard-grid">
        <div class="dashboard-card">
          <h4>Temperature Trends</h4>
          <canvas id="tempChart"></canvas>
        </div>
        <div class="dashboard-card">
          <h4>Battery Status</h4>
          <canvas id="batteryChart"></canvas>
        </div>
        <div class="dashboard-card">
          <h4>Mode Usage</h4>
          <canvas id="modeChart"></canvas>
        </div>
      </div>
    </div>
  </section>

  <footer>
    <p>© 2025 CLIMA-AI | Designed for the future, powered by intelligence.</p>
  </footer>

  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <script>
    // Sticky header hide/show logic
    let lastScrollTop = 0;
    const header = document.getElementById("mainHeader");

    window.addEventListener("scroll", function () {
      const scrollTop = window.pageYOffset || document.documentElement.scrollTop;
      if (scrollTop > lastScrollTop) {
        header.classList.add("hide");
      } else {
        header.classList.remove("hide");
      }
      lastScrollTop = scrollTop;
    });

    // Temperature Control Logic
    const slider = document.getElementById("tempSlider");
    const display = document.getElementById("tempDisplay");

    function updateTempDisplay(value) {
      display.textContent = value + "°C";
      if (value < 20) {
        display.style.color = "blue";
        slider.style.background = "linear-gradient(to right, blue, lightblue)";
      } else if (value > 30) {
        display.style.color = "red";
        slider.style.background = "linear-gradient(to right, orange, red)";
      } else {
        display.style.color = "green";
        slider.style.background = "linear-gradient(to right, blue, red)";
      }
    }

    slider.addEventListener("input", function () {
      updateTempDisplay(slider.value);
    });

    // Mode presets
    function setMode(mode) {
      let temp;
      if (mode === "Active") temp = 22;
      if (mode === "Rest") temp = 24;
      if (mode === "Outdoor") temp = 28;
      if (mode === "Indoor") temp = 26;

      slider.value = temp;
      updateTempDisplay(temp);
    }

    // Initialize display
    updateTempDisplay(slider.value);

    // Dashboard Charts
    const tempCtx = document.getElementById('tempChart');
    new Chart(tempCtx, {
      type: 'line',
      data: {
        labels: ['Mon','Tue','Wed','Thu','Fri','Sat','Sun'],
        datasets: [{
          label: 'Temperature (°C)',
          data: [24,25,26,27,26,25,24],
          borderColor: '#004e92',
          fill: false,
          tension: 0.3
        }]
      },
      options: { responsive: true, plugins: { legend: { display: false } } }
    });

    const batteryCtx = document.getElementById('batteryChart');
    new Chart(batteryCtx, {
      type: 'doughnut',
      data: {
        labels: ['Used', 'Remaining'],
        datasets: [{
          data: [30, 70],
          backgroundColor: ['#00c9a7','#e0e0e0']
        }]
      },
      options: { responsive: true, plugins: { legend: { position: 'bottom' } } }
    });

    const modeCtx = document.getElementById('modeChart');
    new Chart(modeCtx, {
      type: 'bar',
      data: {
        labels: ['Active','Rest','Outdoor','Indoor'],
        datasets: [{
          data: [10,15,7,20],
          backgroundColor: '#004e92'
        }]
      },
      options: { responsive: true, plugins: { legend: { display: false } }, scales: { y: { beginAtZero: true } } }
    });
  </script>
</body>
</html>

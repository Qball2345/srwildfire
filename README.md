
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>S&R Wildfire Systems</title>
  <style>
    :root {
      --bg: #050505;
      --panel: rgba(12, 12, 12, 0.92);
      --text: #f4f4f4;
      --muted: #b7c0c8;
      --pink: #ff2f92;
      --cyan: #16e0ff;
      --yellow: #ffc72c;
      --line: rgba(22, 224, 255, 0.25);
    }

    * {
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      font-family: Arial, Helvetica, sans-serif;
      background:
        radial-gradient(circle at top, rgba(255, 47, 146, 0.08), transparent 25%),
        radial-gradient(circle at right, rgba(22, 224, 255, 0.08), transparent 20%),
        #050505;
      color: var(--text);
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    /* NAV */
    .nav {
      position: sticky;
      top: 0;
      z-index: 1000;
      background: rgba(5, 5, 5, 0.92);
      backdrop-filter: blur(8px);
      border-bottom: 1px solid rgba(22, 224, 255, 0.18);
    }

    .nav-inner {
      max-width: 1200px;
      margin: 0 auto;
      padding: 16px 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 12px;
      font-weight: 800;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      color: var(--cyan);
      text-shadow: 0 0 10px rgba(22, 224, 255, 0.5);
    }

    .brand img {
      width: 42px;
      height: 42px;
      object-fit: contain;
      border-radius: 6px;
    }

    .nav-links {
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
      font-size: 0.95rem;
      color: var(--muted);
    }

    .nav-links a:hover {
      color: var(--pink);
    }

    /* HERO */
    .hero {
      position: relative;
      overflow: hidden;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 80px 20px;
    }

    .hero::before {
      content: "";
      position: absolute;
      inset: 0;
      background:
        linear-gradient(to bottom, rgba(0,0,0,0.2), rgba(0,0,0,0.8)),
        linear-gradient(rgba(22, 224, 255, 0.08) 1px, transparent 1px),
        linear-gradient(90deg, rgba(22, 224, 255, 0.08) 1px, transparent 1px);
      background-size: auto, 40px 40px, 40px 40px;
      mask-image: linear-gradient(to bottom, rgba(0,0,0,1), rgba(0,0,0,0.35));
      pointer-events: none;
    }

    .hero-content {
      position: relative;
      z-index: 2;
      max-width: 1100px;
      width: 100%;
      text-align: center;
    }

    .hero-logo {
      width: min(440px, 85vw);
      max-width: 100%;
      margin-bottom: 24px;
      filter:
        drop-shadow(0 0 8px rgba(255, 47, 146, 0.35))
        drop-shadow(0 0 18px rgba(22, 224, 255, 0.25));
    }

    .eyebrow {
      color: var(--yellow);
      text-transform: uppercase;
      letter-spacing: 0.22em;
      font-size: 0.9rem;
      font-weight: 800;
      margin-bottom: 16px;
    }

    .hero h1 {
      margin: 0;
      font-size: clamp(2.6rem, 7vw, 6rem);
      line-height: 0.95;
      text-transform: uppercase;
      color: var(--pink);
      letter-spacing: 0.06em;
      text-shadow:
        0 0 10px rgba(255, 47, 146, 0.75),
        0 0 28px rgba(255, 47, 146, 0.25);
    }

    .hero p {
      max-width: 820px;
      margin: 22px auto 0;
      color: var(--muted);
      font-size: 1.15rem;
    }

    .hero-buttons {
      display: flex;
      justify-content: center;
      gap: 16px;
      flex-wrap: wrap;
      margin-top: 36px;
    }

    .btn {
      display: inline-block;
      padding: 14px 22px;
      border: 2px solid var(--cyan);
      color: var(--cyan);
      font-weight: 800;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      background: transparent;
      box-shadow: 0 0 16px rgba(22, 224, 255, 0.08);
      transition: 0.2s ease;
    }

    .btn:hover {
      background: var(--cyan);
      color: #000;
      box-shadow: 0 0 20px rgba(22, 224, 255, 0.45);
    }

    .btn.alt {
      border-color: var(--pink);
      color: var(--pink);
    }

    .btn.alt:hover {
      background: var(--pink);
      color: #000;
      box-shadow: 0 0 20px rgba(255, 47, 146, 0.45);
    }

    /* MAIN */
    main {
      max-width: 1100px;
      margin: 0 auto;
      padding: 40px 20px 80px;
    }

    section {
      background: var(--panel);
      border: 1px solid rgba(255, 255, 255, 0.05);
      border-left: 4px solid var(--cyan);
      margin-bottom: 32px;
      padding: 32px;
      box-shadow: 0 10px 40px rgba(0,0,0,0.35);
    }

    h2 {
      margin-top: 0;
      font-size: clamp(1.8rem, 3vw, 3rem);
      color: var(--yellow);
      text-transform: uppercase;
      letter-spacing: 0.05em;
      text-shadow: 0 0 12px rgba(255, 199, 44, 0.18);
    }

    h3 {
      margin-top: 28px;
      color: var(--pink);
      text-transform: uppercase;
      letter-spacing: 0.04em;
    }

    p {
      color: var(--muted);
    }

    .highlight {
      color: var(--cyan);
      font-weight: 700;
    }

    .feature-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
      margin-top: 24px;
    }

    .feature-card {
      padding: 22px;
      background: rgba(255,255,255,0.02);
      border: 1px solid rgba(22, 224, 255, 0.14);
    }

    .feature-card strong {
      display: block;
      color: var(--cyan);
      margin-bottom: 8px;
      text-transform: uppercase;
      letter-spacing: 0.05em;
    }

    .video-container {
      position: relative;
      width: 100%;
      padding-bottom: 56.25%;
      height: 0;
      margin: 24px 0;
      border: 1px solid rgba(255, 47, 146, 0.3);
      box-shadow: 0 0 18px rgba(255, 47, 146, 0.08);
      overflow: hidden;
      background: #000;
    }

    .video-container iframe {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      border: 0;
    }

    .image-frame {
      margin: 24px 0 10px;
      text-align: center;
    }

    .image-frame img {
      max-width: 100%;
      height: auto;
      border: 1px solid rgba(22, 224, 255, 0.25);
      box-shadow: 0 0 24px rgba(22, 224, 255, 0.08);
    }

    footer {
      padding: 30px 20px;
      text-align: center;
      color: #9aa3ab;
      border-top: 1px solid rgba(22, 224, 255, 0.12);
      background: #080808;
    }

    @media (max-width: 900px) {
      .feature-grid {
        grid-template-columns: 1fr;
      }

      .nav-inner {
        flex-direction: column;
        align-items: flex-start;
      }

      .nav-links {
        gap: 12px;
      }
    }

    @media (max-width: 600px) {
      .hero {
        min-height: auto;
        padding-top: 60px;
        padding-bottom: 60px;
      }

      section {
        padding: 22px;
      }

      .hero-buttons {
        flex-direction: column;
      }

      .btn {
        width: 100%;
      }
    }
  </style>
</head>
<body>

  <nav class="nav">
    <div class="nav-inner">
      <div class="brand">
        <img src="logo.png" alt="S&R Wildfire Systems logo">
        <span>S&R Wildfire Systems</span>
      </div>
      <div class="nav-links">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#chcu">The CHCU</a>
        <a href="#meettheteam">Team</a>
        <a href="#merch">Merch</a>
      </div>
    </div>
  </nav>

  <header class="hero">
    <div class="hero-content">
      <img class="hero-logo" src="logo.png" alt="S&R Wildfire Systems logo">

      

      <h1>Remote Wildfire<br>Tech Solutions</h1>

      <p>
  
        Long-range pressure monitoring and 3-way control
        
      </p>

      <div class="hero-buttons">
        <a class="btn" href="#chcu">See It in Action</a>
        
      </div>
    </div>
  </header>

  <main>

    <section id="about">
      <h2>Wildfire meets IoT</h2>
      <p>
Wildland firefighting is a gritty, hard-nosed operation that demands a lot from its equipment. Much of the technology used in the field has remained simple by necessity: it needs to be reliable, durable, and able to fail in obvious ways. This keeps firefighting operations effective, but it can also leave room for major efficiency gains especially when compared to adjacent industries.
      </p>
       <p>
At Stanhope & Reid Wildfire Systems, we develop practical IoT-based solutions for the wildfire environment while preserving the consistency, toughness, and field reliability that firefighters demand from their equipment. Our goal is not to automate the profession, but to give firefighters better tools, better information, and more control during operations.
      </p>
    

      <div class="feature-grid">
        <div class="feature-card">
          <strong>1 km+ Range</strong>
          Long-distance remote control using LoRa communication.
        </div>
        <div class="feature-card">
          <strong>Remote Threeway Control</strong>
          Reduce unnecessary walking and speed up hose lay operations.
        </div>
        <div class="feature-card">
          <strong>Pressure Feedback</strong>
          Get live pressure updates from the field.
        </div>
      </div>

      <div class="video-container">
        <iframe
          src="https://www.youtube.com/embed/UoZGK9sne38"
          title="CHCU overview video"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
        </iframe>
      </div>
    </section>

    <section id="diversion">
      <h2>Water Diversion</h2>
      <p>The CHCU provides two types of threeway flips: full and incremental.</p>

      <h3>Full</h3>
      <p>
        The full threeway flip allows for complete stoppage of water flow so firefighters
        can add another length of hose.
      </p>

      <div class="video-container">
        <iframe
          src="https://www.youtube.com/embed/O6K0zqInA_I"
          title="Full threeway flip"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
        </iframe>
      </div>

      <h3>Incremental</h3>
      <p>
        As a means of managing pressure, the threeway can be opened a certain percentage
        to allow for pressure relief.
      </p>

      <div class="video-container">
        <iframe
          src="https://www.youtube.com/embed/yZ1eOZ8rw7U"
          title="Incremental threeway flip"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
        </iframe>
      </div>
    </section>

    <section id="pressure">
      <h2>Pressure Readings</h2>
      <p>
        The CHCU sends pressure readings to the user’s mobile device every 2 seconds.
        This is useful for quick mental math about how many nozzles can be open and
        for noticing when a hose may have blown a hole in it.
      </p>

      <div class="image-frame">
        <img src="pressure_sensor.png" alt="Pressure sensor image">
      </div>
    </section>

    <section id="data">
      <h2>Data Capture and Analysis</h2>
      <p>
        Pressure readings can be logged and saved as an Excel file for analysis.
        One experiment involved determining the minimum and maximum workable pressure
        for a Hansen nozzle.
      </p>
      <p>
        If the pressure is too high, the hose becomes too difficult to hold.
        If the pressure is too low, the duff layer cannot be properly penetrated
        and the fire cannot be extinguished.
      </p>

      <div class="image-frame">
        <img src="Pressure_vs_Time_graph.png" alt="Pressure vs time graph">
      </div>
    </section>

  </main>

  <footer>
    <p>&copy; 2026 S&R Wildfire Systems. All rights reserved.</p>
  </footer>

</body>
</html>

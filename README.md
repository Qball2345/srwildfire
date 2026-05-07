<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>S&R Wildfire Systems | CHCU</title>

  <style>
    :root {
      --ink: #130f1f;
      --night: #21152f;
      --deep-purple: #35224d;
      --cream: #f7e7c4;
      --sand: #d8b06f;
      --orange: #d86f2d;
      --ember: #b6422a;
      --gold: #f0b84d;
      --smoke: rgba(247, 231, 196, 0.78);
      --card: rgba(33, 21, 47, 0.88);
      --line: rgba(240, 184, 77, 0.45);
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
      color: var(--cream);
      background:
        radial-gradient(circle at 18% 10%, rgba(216, 111, 45, 0.22), transparent 30%),
        radial-gradient(circle at 82% 16%, rgba(240, 184, 77, 0.16), transparent 28%),
        linear-gradient(180deg, #140f1e 0%, #241732 48%, #111019 100%);
      line-height: 1.6;
      overflow-x: hidden;
    }

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      pointer-events: none;
      background-image:
        linear-gradient(rgba(255,255,255,0.035) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,0.025) 1px, transparent 1px);
      background-size: 34px 34px;
      mask-image: linear-gradient(to bottom, rgba(0,0,0,0.8), transparent 85%);
      z-index: -2;
    }

    body::after {
      content: "";
      position: fixed;
      inset: 0;
      pointer-events: none;
      background: repeating-linear-gradient(
        to bottom,
        rgba(255,255,255,0.035) 0,
        rgba(255,255,255,0.035) 1px,
        transparent 1px,
        transparent 5px
      );
      opacity: 0.18;
      z-index: 999;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .top-nav {
      position: sticky;
      top: 0;
      z-index: 10;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 20px;
      padding: 16px 6vw;
      background: rgba(19, 15, 31, 0.88);
      border-bottom: 1px solid var(--line);
      backdrop-filter: blur(10px);
    }

    .brand {
      font-weight: 900;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--gold);
      font-size: 0.9rem;
    }

    .nav-links {
      display: flex;
      gap: 22px;
      font-size: 0.82rem;
      text-transform: uppercase;
      letter-spacing: 0.1em;
      color: var(--smoke);
    }

    .nav-links a:hover {
      color: var(--gold);
    }

    header {
      position: relative;
      min-height: 88vh;
      display: grid;
      place-items: center;
      padding: 110px 20px 90px;
      text-align: center;
      overflow: hidden;
      border-bottom: 1px solid var(--line);
    }

    .sunset {
      position: absolute;
      width: min(820px, 92vw);
      aspect-ratio: 2 / 1;
      bottom: 5%;
      left: 50%;
      transform: translateX(-50%);
      background:
        linear-gradient(to bottom,
          var(--gold) 0 12%, transparent 12% 18%,
          var(--orange) 18% 30%, transparent 30% 36%,
          var(--ember) 36% 50%, transparent 50% 57%,
          #673458 57% 70%, transparent 70% 76%,
          #3c2852 76% 100%);
      border-radius: 820px 820px 0 0;
      opacity: 0.78;
      filter: drop-shadow(0 0 42px rgba(216, 111, 45, 0.38));
      z-index: -1;
    }

    .hero-content {
      max-width: 1100px;
      position: relative;
      z-index: 1;
    }

    .eyebrow {
      margin: 0 0 18px;
      color: var(--gold);
      text-transform: uppercase;
      letter-spacing: 0.22em;
      font-weight: 800;
      font-size: clamp(0.78rem, 1.8vw, 1rem);
    }

    h1 {
      margin: 0;
      font-size: clamp(4rem, 15vw, 12rem);
      line-height: 0.82;
      letter-spacing: 0.04em;
      text-transform: uppercase;
      color: var(--cream);
      text-shadow:
        5px 5px 0 var(--ember),
        10px 10px 0 rgba(19, 15, 31, 0.75),
        0 0 30px rgba(240, 184, 77, 0.3);
    }

    .tagline {
      max-width: 780px;
      margin: 30px auto 0;
      font-size: clamp(1.05rem, 2.3vw, 1.6rem);
      color: var(--smoke);
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 16px;
      margin-top: 36px;
    }

    .button {
      display: inline-block;
      padding: 14px 22px;
      border: 2px solid var(--gold);
      background: var(--gold);
      color: var(--ink);
      font-weight: 900;
      text-transform: uppercase;
      letter-spacing: 0.11em;
      box-shadow: 6px 6px 0 var(--ember);
      transition: transform 160ms ease, box-shadow 160ms ease;
    }

    .button.secondary {
      background: transparent;
      color: var(--cream);
    }

    .button:hover {
      transform: translate(3px, 3px);
      box-shadow: 3px 3px 0 var(--ember);
    }

    main {
      width: min(1120px, calc(100% - 32px));
      margin: 0 auto;
      padding: 70px 0;
    }

    section {
      position: relative;
      margin-bottom: 44px;
      padding: clamp(24px, 5vw, 46px);
      background: var(--card);
      border: 1px solid var(--line);
      box-shadow:
        0 22px 60px rgba(0, 0, 0, 0.28),
        inset 0 0 0 1px rgba(255,255,255,0.04);
    }

    section::before {
      content: "";
      position: absolute;
      inset: 10px;
      border: 1px solid rgba(247, 231, 196, 0.12);
      pointer-events: none;
    }

    h2, h3 {
      margin-top: 0;
      line-height: 1.05;
      text-transform: uppercase;
      letter-spacing: 0.07em;
    }

    h2 {
      color: var(--gold);
      font-size: clamp(2rem, 5vw, 4.2rem);
      text-shadow: 3px 3px 0 rgba(182, 66, 42, 0.8);
      border-bottom: 2px solid var(--line);
      padding-bottom: 16px;
      margin-bottom: 22px;
    }

    h3 {
      color: var(--cream);
      font-size: clamp(1.25rem, 3vw, 2rem);
      margin-top: 34px;
      margin-bottom: 10px;
    }

    p {
      color: var(--smoke);
      font-size: 1.04rem;
      max-width: 860px;
    }

    .split {
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      gap: 34px;
      align-items: center;
    }

    .stat-card {
      border: 1px solid var(--line);
      background: rgba(19, 15, 31, 0.58);
      padding: 26px;
      box-shadow: 8px 8px 0 rgba(182, 66, 42, 0.55);
    }

    .stat-card strong {
      display: block;
      color: var(--gold);
      font-size: clamp(2.4rem, 6vw, 4.8rem);
      line-height: 1;
      text-shadow: 4px 4px 0 var(--ember);
    }

    .stat-card span {
      display: block;
      margin-top: 12px;
      text-transform: uppercase;
      letter-spacing: 0.11em;
      color: var(--cream);
      font-weight: 800;
    }

    .feature-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
      margin: 26px 0 10px;
    }

    .feature {
      padding: 22px;
      border: 1px solid rgba(240, 184, 77, 0.34);
      background: rgba(247, 231, 196, 0.06);
    }

    .feature b {
      display: block;
      margin-bottom: 8px;
      color: var(--gold);
      text-transform: uppercase;
      letter-spacing: 0.08em;
    }

    .video-container {
      position: relative;
      width: 100%;
      padding-bottom: 56.25%;
      height: 0;
      margin: 34px 0 8px;
      border: 2px solid var(--gold);
      box-shadow: 10px 10px 0 var(--ember);
      background: #000;
      overflow: hidden;
    }

    .video-container iframe {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
      border: 0;
    }

    .image-frame {
      text-align: center;
      margin: 34px 0 8px;
    }

    .image-frame img {
      width: 100%;
      max-width: 880px;
      height: auto;
      border: 2px solid var(--gold);
      box-shadow: 10px 10px 0 var(--ember);
      background: var(--ink);
    }

    .callout {
      margin-top: 28px;
      padding: 24px;
      border-left: 6px solid var(--gold);
      background: rgba(216, 111, 45, 0.14);
      color: var(--cream);
      font-weight: 700;
    }

    footer {
      text-align: center;
      padding: 34px 20px;
      background: rgba(19, 15, 31, 0.95);
      border-top: 1px solid var(--line);
      color: var(--smoke);
    }

    @media (max-width: 850px) {
      .top-nav {
        align-items: flex-start;
        flex-direction: column;
      }

      .nav-links {
        flex-wrap: wrap;
        gap: 12px 18px;
      }

      .split,
      .feature-grid {
        grid-template-columns: 1fr;
      }

      header {
        min-height: 78vh;
      }
    }

    @media (max-width: 520px) {
      .nav-links {
        display: none;
      }

      h1 {
        text-shadow:
          3px 3px 0 var(--ember),
          6px 6px 0 rgba(19, 15, 31, 0.75);
      }

      .button {
        width: 100%;
      }
    }
  </style>
</head>

<body>
  <nav class="top-nav">
    <a class="brand" href="#top">S&R Wildfire Systems</a>
    <div class="nav-links">
      <a href="#problem">Problem</a>
      <a href="#diversion">Water Diversion</a>
      <a href="#pressure">Pressure</a>
      <a href="#data">Data</a>
    </div>
  </nav>

  <header id="top">
    <div class="sunset" aria-hidden="true"></div>
    <div class="hero-content">
      <p class="eyebrow">Field-tested wildfire water control</p>
      <h1>CHCU</h1>
      <p class="tagline">Central Hose Command Unit — a rugged remote water-diversion concept built for long hose lays, pressure management, and less walking back to the threeway.</p>
      <div class="hero-actions">
        <a class="button" href="#problem">View the Project</a>
        <a class="button secondary" href="#diversion">See the Flip</a>
      </div>
    </div>
  </header>

  <main>
    <section id="problem">
      <div class="split">
        <div>
          <h2>An Interesting Problem With a Unique Solution</h2>
          <p>For years, firefighters have had to go back to the threeway to stop water flow or manage pressure. All the walking back and forth adds up and makes water delivery require more effort than necessary.</p>
          <p>To address this issue, the Central Hose Command Unit was created. Firefighters can control flow remotely using a mobile device to engage a linear actuator. The system uses LoRa to divert water from over 1 km away.</p>
        </div>
        <aside class="stat-card">
          <strong>1 km+</strong>
          <span>Remote diversion range</span>
        </aside>
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

      <div class="feature-grid">
        <div class="feature">
          <b>Full Flip</b>
          Complete stoppage of water flow so crews can add another length of hose.
        </div>
        <div class="feature">
          <b>Incremental Flip</b>
          Partial opening for pressure relief and finer flow control.
        </div>
        <div class="feature">
          <b>Remote Control</b>
          Less walking, faster adjustment, and better control from the working end.
        </div>
      </div>

      <h3>Full</h3>
      <p>The full threeway flip allows for complete stoppage of water flow so that firefighters can add on another length of hose.</p>

      <div class="video-container">
        <iframe
          src="https://www.youtube.com/embed/O6K0zqInA_I"
          title="CHCU full threeway flip"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
        </iframe>
      </div>

      <h3>Incremental</h3>
      <p>As a means of managing pressure, the threeway can be opened a certain percentage to allow for pressure relief.</p>

      <div class="video-container">
        <iframe
          src="https://www.youtube.com/embed/yZ1eOZ8rw7U"
          title="CHCU incremental threeway flip"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
        </iframe>
      </div>
    </section>

    <section id="pressure">
      <h2>Pressure Readings</h2>
      <p>The CHCU sends pressure readings to the user's mobile device every 2 seconds. This helps crews quickly estimate how many nozzles can be open and monitor if a hose has blown a hole in it.</p>

      <div class="image-frame">
        <img src="pressure_sensor.png" alt="Pressure sensor used for the CHCU system" />
      </div>
    </section>

    <section id="data">
      <h2>Data Capture and Analysis</h2>
      <p>To better understand water pressure and hose behaviour, pressure readings can be logged and saved as an Excel file for further analysis.</p>
      <p>One experiment involved determining the minimum and maximum workable pressure for a Hansen nozzle. If the pressure is too high, the hose becomes too difficult to hold. If the pressure is too low, the duff layer cannot be properly penetrated and the fire cannot be extinguished.</p>

      <div class="callout">This kind of pressure data could help turn field experience into measurable design feedback.</div>

      <div class="image-frame">
        <img src="Pressure_vs_Time_graph.png" alt="Pressure versus time graph from CHCU testing" />
      </div>
    </section>
  </main>

  <footer>
    <p>&copy; 2026 S&R Wildfire Systems. All rights reserved.</p>
  </footer>
</body>
</html>

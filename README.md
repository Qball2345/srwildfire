
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CHCU</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
            line-height: 1.6;
        }
        header {
            background-color: #2c3e50;
            color: white;
            text-align: center;
            padding: 100px 20px;
        }
        header h1 {
            font-size: 10rem;
            margin: 0;
            letter-spacing: 0.1em;
        }
        header p {
            font-size: 1.5rem;
            margin-top: 10px;
            opacity: 0.9;
        }
        main {
            max-width: 1000px;
            margin: 50px auto;
            padding: 20px;
        }
        section {
            background: white;
            margin-bottom: 40px;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }
        h2 {
            color: #2c3e50;
            border-bottom: 3px solid #3498db;
            padding-bottom: 10px;
            font-size: 2rem;
        }
        h3 {
            color: #2c3e50;
            border-bottom: 3px solid #3498db;
            padding-bottom: 10px;
            font-size: 1.5rem;
            margin-top: 30px;
        }

        /* Responsive video container */
        .video-container {
            position: relative;
            width: 100%;
            padding-bottom: 56.25%; /* 16:9 aspect ratio */
            height: 0;
            margin: 40px 0;
        }
        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: 0;
        }

        footer {
            text-align: center;
            padding: 30px;
            background-color: #2c3e50;
            color: white;
            margin-top: 50px;
        }

        /* Mobile adjustments */
        @media (max-width: 1024px) {
            header h1 {
                font-size: 7rem;
            }
        }
        @media (max-width: 768px) {
            header {
                padding: 80px 20px;
            }
            header h1 {
                font-size: 5rem;
            }
            header p {
                font-size: 1.2rem;
            }
            section {
                padding: 20px;
            }
            h2 {
                font-size: 1.8rem;
            }
        }
        @media (max-width: 480px) {
            header h1 {
                font-size: 3.5rem;
            }
            header p {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Central Hose Command Unit</h1>
        <p>A Couple Months of Stoppable Flow</p>
    </header>
    <main>
        <section>
            <h2>An Interesting Problem With a Unique Solution</h2>
            <p>For years, firefighters have had to go back to the threeway to stop waterflow or manage pressure. All the walking back and forth really adds up
            and makes water delivery require more effort than necessary. To address this issue, the Central Hose Command Unit (CHCU) was created.
            Now firefighters can control the flow of water remotely using their mobile device to engage a linear actuator. The system uses a transmission protocol
            called LoRa that allows for water to be diverted from over 1 km away.</p>

            <div class="video-container">
                <iframe
                    src="https://www.youtube.com/embed/UoZGK9sne38"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen>
                </iframe>
            </div>
        </section>

        <section>
            <h2>Water Diversion</h2>
            <p>The CHCU provides two types of threeway flips: Full and Incremental.</p>

            <h3>Full</h3>
            <p>The full threeway flip allows for complete stoppage of water flow so that firefighters can add on another length of hose.</p>

            <div class="video-container">
                <iframe
                    src="https://www.youtube.com/embed/O6K0zqInA_I"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen>
                </iframe>
            </div>

            <h3>Incremental</h3>
            <p>As a means of managing pressure, the threeway can be opened a certain percentage to allow for pressure relief.</p>

            <div class="video-container">
                <iframe
                    src="https://www.youtube.com/embed/yZ1eOZ8rw7U"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen>
                </iframe>
            </div>
        </section>

        <section>
            <h2>Pressure Readings</h2>
            <p>The CHCU also sends pressure readings to the user's mobile device every 2 seconds. This is helpful for quickly doing mental math about how many nozzles can be open and
            monitoring if a hose has blown a hole in it.</p>
            <div style="text-align: center; margin: 40px 0;">
                <img src="pressure_sensor.png" style="max-width: 100%; height: auto; border-radius: 10px; box-shadow: 0 4px 12px rgba(0,0,0,0.1);">
            </div>
        </section>

        <section>
            <h2>Data Capture and Analysis</h2>
            <p>To better understand water pressure and hose behaviour, pressure readings can be logged and saved as an Excel file for further data analysis. One of the experiments
            involved determining minimum and maximum workable pressure for a Hansen nozzle. If the pressure is to high, the hose becomes to difficult to hold. If the pressure is to low, the duff layer cannot be properly pentrated and the fire cannot be extinguished. This may be the first time data like this has been recorded at this level of detail.</p>
            <div style="text-align: center; margin: 40px 0;">
                <img src="Pressure_vs_Time_graph.png" style="max-width: 100%; height: auto; border-radius: 10px; box-shadow: 0 4px 12px rgba(0,0,0,0.1);">
            </div>
        </section>
    </main>
    <footer>
        <p>&copy; 2025 CHCU. All rights reserved.</p>
    </footer>
</body>
</html>

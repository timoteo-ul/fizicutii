<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fizicutii</title>
    <style>
        body {
            margin: 0;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background-color: #f9f9f9;
            color: #000;
            text-align: center;
        }

        nav {
            display: flex;
            justify-content: center;
            gap: 40px;
            padding: 20px;
            background-color: white;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            flex-wrap: wrap;
        }

        nav a {
            text-decoration: none;
            color: black;
            font-weight: 500;
            font-size: 18px;
            transition: transform 0.3s ease, font-size 0.3s ease;
        }

        nav a:hover {
            transform: scale(1.3);
            font-size: 20px;
        }

        nav a:not(:hover) {
            transform: scale(0.9);
            font-size: 16px;
        }

        .container {
            padding: 50px 20px;
        }

        h1 {
            font-size: 3em;
            font-weight: bold;
        }

        .description {
            font-size: 1.2em;
            max-width: 700px;
            margin: 20px auto;
            line-height: 1.6;
        }

        .buttons {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 40px;
            margin-top: 50px;
        }

        .card-button {
            background-color: white;
            border-radius: 20px;
            padding: 30px;
            box-shadow: 0 6px 20px rgba(0,0,0,0.1);
            width: 220px;
            transition: transform 0.4s ease;
            cursor: pointer;
            text-align: center;
        }

        .card-button:hover {
            transform: scale(1.1);
        }

        .icon {
            width: 60px;
            height: 60px;
            margin-bottom: 10px;
        }

        .card-button p {
            font-weight: bold;
            font-size: 18px;
            margin: 0;
        }

        .hidden {
            display: none;
        }

        .formula {
            margin: 30px 0;
            font-weight: bold;
            font-size: 1.3em;
        }

        .explanation {
            font-size: 1em;
            margin-top: 5px;
        }

        .animated-light {
            filter: drop-shadow(0 0 10px yellow);
        }

        .animated-fire {
            animation: flicker 0.5s infinite alternate;
        }

        .animated-gear {
            animation: spin 2s linear infinite;
        }

        @keyframes flicker {
            0% { filter: drop-shadow(0 0 5px orange); }
            100% { filter: drop-shadow(0 0 20px red); }
        }

        @keyframes spin {
            100% { transform: rotate(360deg); }
        }

        @keyframes eyeMove {
            0% { transform: rotate(0deg); }
            50% { transform: rotate(10deg); }
            100% { transform: rotate(-10deg); }
        }

        .animated-eye {
            animation: eyeMove 2s infinite;
        }

        @media (max-width: 768px) {
            nav {
                flex-wrap: wrap;
                gap: 20px;
            }
            .card-button {
                width: 90%;
            }
        }
    </style>
</head>
<body>
    <nav>
        <a href="#acasa" onclick="showPage('acasa')">Acasa</a>
        <a href="#electricitate" onclick="showPage('electricitate')">Electricitate</a>
        <a href="#termodinamica" onclick="showPage('termodinamica')">Termodinamica</a>
        <a href="#mecanica" onclick="showPage('mecanica')">Mecanica</a>
        <a href="#optica" onclick="showPage('optica')">Optica</a>
    </nav>

    <div id="acasa" class="container">
        <h1>Salut</h1>
        <p class="description">
            Bine ai venit pe <strong>Fizicutii</strong> – platforma care te ajută să înțelegi rapid și eficient fizica de Bacalaureat. Aici găsești explicații simple, formule esențiale și concepte ilustrate. Succes la BAC!
        </p>
        <div class="buttons">
            <div class="card-button" onclick="showPage('electricitate')" onmouseover="lightBulb(true)" onmouseout="lightBulb(false)">
                <img src="https://img.icons8.com/external-flatart-icons-outline-flatarticons/64/external-light-bulb-creative-process-flatart-icons-outline-flatarticons.png" class="icon" id="bulb">
                <p>Electricitate</p>
            </div>
            <div class="card-button" onclick="showPage('termodinamica')" onmouseover="fireAnim(true)" onmouseout="fireAnim(false)">
                <img src="https://img.icons8.com/ios-filled/50/campfire.png" class="icon" id="fire">
                <p>Termodinamica</p>
            </div>
            <div class="card-button" onclick="showPage('mecanica')" onmouseover="gearAnim(true)" onmouseout="gearAnim(false)">
                <img src="https://img.icons8.com/ios-filled/50/gear.png" class="icon" id="gear">
                <p>Mecanica</p>
            </div>
            <div class="card-button" onclick="showPage('optica')" onmouseover="eyeAnim(true)" onmouseout="eyeAnim(false)">
                <img src="https://img.icons8.com/ios/50/eye-unchecked.png" class="icon" id="eye">
                <p>Optica</p>
            </div>
        </div>
    </div>

    <div id="electricitate" class="container hidden">
        <h1>Electricitate</h1>
        <div class="formula">U = R × I<div class="explanation">U = tensiune (V), R = rezistență (Ω), I = intensitate (A)</div></div>
        <div class="formula">I = Q / t<div class="explanation">Q = sarcină electrică (C), t = timp (s)</div></div>
        <div class="formula">R = ρ × L / S<div class="explanation">ρ = rezistivitate (Ω·m), L = lungime conductor (m), S = arie (m²)</div></div>
        <div class="formula">P = U × I<div class="explanation">P = putere electrică (W)</div></div>
        <div class="formula">E = P × t<div class="explanation">E = energie electrică (J sau kWh)</div></div>
        <div class="formula">Legea lui Ohm: I = U / R</div>
    </div>

    <div id="termodinamica" class="container hidden">
        <h1>Termodinamică</h1>
        <div class="formula">Q = m × c × ΔT<div class="explanation">Q = căldură (J), m = masă (kg), c = căldura specifică, ΔT = variație temperatură (°C)</div></div>
        <div class="formula">Q = m × L<div class="explanation">L = căldura latentă (J/kg) – schimb de fază</div></div>
        <div class="formula">U = (3/2) × n × R × T<div class="explanation">U = energia internă a unui gaz ideal</div></div>
        <div class="formula">p × V = n × R × T<div class="explanation">Ecuația de stare a gazului ideal</div></div>
        <div class="formula">ΔU = Q - L<div class="explanation">Primul principiu al termodinamicii</div></div>
    </div>

    <div id="mecanica" class="container hidden">
        <h1>Mecanică</h1>
        <div class="formula">s = v × t<div class="explanation">s = deplasare (m), v = viteză (m/s), t = timp (s)</div></div>
        <div class="formula">v = a × t<div class="explanation">a = accelerație (m/s²)</div></div>
        <div class="formula">F = m × a<div class="explanation">F = forță (N), m = masă (kg)</div></div>
        <div class="formula">Ec = ½ × m × v²<div class="explanation">Ec = energie cinetică (J)</div></div>
        <div class="formula">Ep = m × g × h<div class="explanation">Ep = energie potențială gravitațională</div></div>
        <div class="formula">E = Ec + Ep<div class="explanation">E = energie mecanică totală</div></div>
    </div>

    <div id="optica" class="container hidden">
        <h1>Optică și oscilații</h1>
        <div class="formula">f = 1 / T<div class="explanation">f = frecvență (Hz), T = perioadă (s)</div></div>
        <div class="formula">T = 2π × √(m / k)<div class="explanation">oscilații armonice</div></div>
        <div class="formula">c = λ × f<div class="explanation">c = viteza luminii (m/s)</div></div>
        <div class="formula">n = c / v<div class="explanation">indice de refracție</div></div>
        <div class="formula">Legea reflexiei: unghiul de incidență = unghiul de reflexie</div>
        <div class="formula">Legea refracției: n1 × sin(θ1) = n2 × sin(θ2)</div>
    </div>

    <script>
        function showPage(id) {
            const pages = document.querySelectorAll('.container');
            pages.forEach(p => p.classList.add('hidden'));
            document.getElementById(id).classList.remove('hidden');
        }

        function lightBulb(on) {
            document.getElementById('bulb').classList.toggle('animated-light', on);
        }

        function fireAnim(on) {
            document.getElementById('fire').classList.toggle('animated-fire', on);
        }

        function gearAnim(on) {
            document.getElementById('gear').classList.toggle('animated-gear', on);
        }

        function eyeAnim(on) {
            const eye = document.getElementById('eye');
            eye.classList.toggle('animated-eye', on);
            eye.src = on ? "https://img.icons8.com/ios/50/visible.png" : "https://img.icons8.com/ios/50/eye-unchecked.png";
        }
    </script>
</body>
</html>

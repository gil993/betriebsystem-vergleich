<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Betriebssystem Vergleich</title>
<style>
    body {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        margin: 0;
        background: linear-gradient(135deg, #4a90e2, #2c3e50);
        color: #fff;
        min-height: 100vh;
        display: flex;
        flex-direction: column;
    }

    header {
        background: rgba(0,0,0,0.4);
        backdrop-filter: blur(10px);
        color: white;
        padding: 2rem;
        text-align: center;
        font-size: 2rem;
        font-weight: bold;
        letter-spacing: 2px;
        text-shadow: 0 4px 12px rgba(0,0,0,0.4);
        animation: fadeDown 1s ease;
    }

    main {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 2rem;
        padding: 3rem;
        flex-grow: 1;
    }

    .os-card {
        background: rgba(255,255,255,0.1);
        backdrop-filter: blur(10px);
        border-radius: 20px;
        box-shadow: 0 8px 30px rgba(0,0,0,0.3);
        padding: 2rem 1.5rem;
        text-align: center;
        cursor: pointer;
        transition: transform 0.4s ease, box-shadow 0.4s ease;
        color: #fff;
        animation: fadeUp 1s ease;
    }

    .os-card:hover {
        transform: translateY(-15px) scale(1.05);
        box-shadow: 0 16px 40px rgba(0,0,0,0.5);
    }

    .os-card img {
        width: 100px;
        height: 100px;
        object-fit: contain;
        margin-bottom: 1rem;
        filter: drop-shadow(0 4px 10px rgba(0,0,0,0.4));
    }

    .os-card h2 {
        margin: 0.5rem 0;
        font-size: 1.5rem;
    }

    section {
        background: rgba(255,255,255,0.1);
        backdrop-filter: blur(12px);
        border-radius: 20px;
        box-shadow: 0 8px 30px rgba(0,0,0,0.3);
        padding: 2rem;
        margin: 2rem;
        animation: fadeUp 1.2s ease;
        color: #fff;
    }

    table {
        width: 100%;
        border-collapse: collapse;
        overflow: hidden;
    }

    thead {
        background: linear-gradient(90deg, #4a90e2, #357abd);
        color: white;
    }

    th, td {
        padding: 1rem;
        text-align: center;
    }

    tbody tr {
        transition: background 0.3s;
        background: rgba(255,255,255,0.05);
    }

    tbody tr:hover {
        background: rgba(255,255,255,0.2);
    }

    .detail {
        display: none;
        padding: 2rem;
        max-width: 800px;
        margin: 3rem auto;
        background: rgba(255,255,255,0.1);
        backdrop-filter: blur(12px);
        border-radius: 20px;
        box-shadow: 0 8px 30px rgba(0,0,0,0.4);
        animation: fadeUp 0.8s ease;
        color: #fff;
    }

    .detail.active {
        display: block;
    }

    .detail h2 {
        margin-top: 0;
    }

    .back-btn {
        display: inline-block;
        margin-top: 1rem;
        padding: 0.7rem 1.5rem;
        background: linear-gradient(90deg, #4a90e2, #357abd);
        color: white;
        border: none;
        border-radius: 12px;
        cursor: pointer;
        font-size: 1rem;
        transition: transform 0.3s;
    }

    .back-btn:hover {
        transform: scale(1.1);
    }

    @keyframes fadeUp {
        from { opacity: 0; transform: translateY(30px); }
        to { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeDown {
        from { opacity: 0; transform: translateY(-30px); }
        to { opacity: 1; transform: translateY(0); }
    }
</style>
</head>
<body>

<header>
    <h1>Betriebssystem Vergleich</h1>
</header>

<main id="main-page">
    <div class="os-card" onclick="showDetail('windows')">
        <img src="https://logos-world.net/wp-content/uploads/2020/12/Windows-New-Logo.png" alt="Windows">
        <h2>Windows</h2>
        <p>Beliebtes System von Microsoft.</p>
    </div>
    <div class="os-card" onclick="showDetail('macos')">
        <img src="https://upload.wikimedia.org/wikipedia/commons/f/fa/Apple_logo_black.svg" alt="macOS">
        <h2>macOS</h2>
        <p>Betriebssystem von Apple.</p>
    </div>
    <div class="os-card" onclick="showDetail('linux')">
        <img src="https://upload.wikimedia.org/wikipedia/commons/a/af/Tux.png" alt="Linux">
        <h2>Linux</h2>
        <p>Offenes und flexibles System.</p>
    </div>
</main>

<section>
    <h2 style="text-align:center; margin-bottom: 1rem;">Betriebssystem Vergleich</h2>
    <div style="overflow-x:auto;">
        <table>
            <thead>
                <tr>
                    <th>Merkmal</th>
                    <th>Windows</th>
                    <th>macOS</th>
                    <th>Linux</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Kosten</td>
                    <td>Kostenpflichtig</td>
                    <td>Kostenpflichtig</td>
                    <td>Kostenlos</td>
                </tr>
                <tr>
                    <td>Sicherheit</td>
                    <td>Mittel</td>
                    <td>Hoch</td>
                    <td>Sehr hoch</td>
                </tr>
                <tr>
                    <td>Anpassung</td>
                    <td>Mittel</td>
                    <td>Wenig</td>
                    <td>Sehr viel</td>
                </tr>
                <tr>
                    <td>Programme</td>
                    <td>Sehr viele</td>
                    <td>Viele exklusive</td>
                    <td>Viele kostenlose</td>
                </tr>
                <tr>
                    <td>Einfachheit</td>
                    <td>Einfach</td>
                    <td>Sehr einfach</td>
                    <td>Eher schwierig</td>
                </tr>
            </tbody>
        </table>
    </div>
</section>

<div id="windows" class="detail">
    <h2>Windows</h2>
    <p>
        Windows ist das am weitesten verbreitete System und wird von Microsoft entwickelt. 
        Es ist für <strong>Privatpersonen</strong> und <strong>Firmen</strong> geeignet.
    </p>
    <p>
        <strong>Bekannt für:</strong>
    </p>
    <ul>
        <li>einfache Bedienung</li>
        <li>läuft auf sehr vielen Geräten</li>
        <li>riesige Auswahl an Programmen und Spielen</li>
    </ul>
    <p>
        <strong>Vorteile:</strong>
    </p>
    <ul>
        <li>Sehr viele Programme</li>
        <li>Weit verbreitet</li>
        <li>Viele nützliche Funktionen</li>
    </ul>
    <p>
        <strong>Nachteile:</strong>
    </p>
    <ul>
        <li>Oft Ziel von Viren</li>
        <li>Braucht viele Updates</li>
        <li>Läuft langsamer auf alten PCs</li>
    </ul>
    <button class="back-btn" onclick="backToMain()">Zurück</button>
</div>

<div id="macos" class="detail">
    <h2>macOS</h2>
    <p>
        macOS läuft nur auf <strong>Apple-Computern</strong>. 
        Es ist einfach zu bedienen und arbeitet gut mit iPhone, iPad und Apple Watch zusammen.
    </p>
    <p>
        <strong>Bekannt für:</strong>
    </p>
    <ul>
        <li>schicke und einfache Oberfläche</li>
        <li>hohe Sicherheit</li>
        <li>läuft stabil auch auf älteren Macs</li>
    </ul>
    <p>
        <strong>Vorteile:</strong>
    </p>
    <ul>
        <li>Sehr gute Zusammenarbeit mit Apple-Geräten</li>
        <li>Exklusive Profi-Programme für Musik und Video</li>
        <li>Seltener Virenprobleme</li>
    </ul>
    <p>
        <strong>Nachteile:</strong>
    </p>
    <ul>
        <li>Nur auf Apple-Computern nutzbar (teurer)</li>
        <li>Weniger Spiele</li>
        <li>Funktioniert nicht mit jeder Hardware</li>
    </ul>
    <button class="back-btn" onclick="backToMain()">Zurück</button>
</div>

<div id="linux" class="detail">
    <h2>Linux</h2>
    <p>
        Linux ist ein <strong>kostenloses System</strong>. 
        Es gibt viele verschiedene Varianten, z. B. Ubuntu oder Debian. 
        Es wird oft auf <strong>Servern</strong> und von <strong>Entwicklern</strong> genutzt.
    </p>
    <p>
       <strong>Bekannt für:</strong>
    </p>
    <ul>
        <li>sehr anpassbar</li>
        <li>sehr sicher</li>
        <li>läuft auch auf alten Computern</li>
    </ul>
    <p>
        <strong>Vorteile:</strong>
    </p>
    <ul>
        <li>Kostenlos und offen</li>
        <li>Schnelle Updates</li>
        <li>Viele kostenlose Programme</li>
        <li>Ideal für Technik-Fans</li>
    </ul>
    <p>
        <strong>Nachteile:</strong>
    </p>
    <ul>
        <li>Etwas schwerer für Anfänger</li>
        <li>Manche Spiele und Programme fehlen</li>
        <li>Man braucht manchmal mehr technisches Wissen</li>
    </ul>
    <button class="back-btn" onclick="backToMain()">Zurück</button>
</div>

<script>
    function showDetail(os) {
        document.getElementById('main-page').style.display = 'none';
        document.getElementById(os).classList.add('active');
    }

    function backToMain() {
        document.querySelectorAll('.detail').forEach(d => d.classList.remove('active'));
        document.getElementById('main-page').style.display = 'grid';
    }
</script>

</body>
</html>

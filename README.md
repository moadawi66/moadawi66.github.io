<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy 15 Months! - Pixel Edition</title>
    <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            image-rendering: pixelated; /* Ensures crisp pixel edges */
        }

        body {
            background: #0c041a;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Press Start 2P', monospace; /* 8-bit Font */
            overflow-x: hidden;
            color: #fff;
            padding: 40px 20px;
        }

        .main-wrapper {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 50px;
            z-index: 10;
            width: 100%;
            max-width: 600px;
        }

        /* --- HARDCODED PIXEL ART HEART USING CSS GRID --- */
        /* Each number in the grid represents a large blocky pixel */
        .pixel-heart {
            display: grid;
            grid-template-columns: repeat(13, 15px); /* 15px large square pixels */
            grid-template-rows: repeat(11, 15px);
            gap: 0; 
            margin-bottom: 20px;
            /* Neon glow behind the pixel heart */
            filter: drop-shadow(0 0 15px #bd00ff);
            animation: pulse 1.2s infinite alternate;
        }

        /* The actual pixels building the heart shape */
        .p { background-color: #bd00ff; border: 1px solid rgba(0,0,0,0.15); } /* Purple Neon Pixel */
        .w { background-color: #ffffff; border: 1px solid rgba(0,0,0,0.15); } /* White highlight pixel */
        .x { background-color: transparent; } /* Empty Space */

        /* --- RETRO NEON TEXT EFFECT --- */
        .pixel-text-container {
            text-align: center;
            width: 100%;
            overflow: hidden;
        }

        .pixel-text {
            font-size: 1.6rem;
            line-height: 2.5rem;
            color: #fff;
            text-shadow: 4px 4px 0px #bd00ff, 8px 8px 0px #5a189a;
            white-space: nowrap;
            border-right: 6px solid #ff007f; /* Blocky cursor */
            width: 0;
            margin: 0 auto;
            animation: 
                typing 3.5s steps(14) forwards, 
                blink 0.6s step-end infinite;
        }

        /* --- RETRO PIXEL FORM --- */
        .message-form {
            background: #12072b;
            border: 6px double #bd00ff; /* Retro double border */
            padding: 30px;
            width: 100%;
            box-shadow: 8px 8px 0px #000; /* Flat block shadow */
        }

        .form-title {
            font-size: 0.75rem;
            color: #ff007f;
            margin-bottom: 25px;
            text-align: center;
            line-height: 1.4rem;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 12px;
            background: #000;
            border: 4px solid #5a189a;
            color: #00ffcc; /* Retro green terminal text color */
            font-family: 'Press Start 2P', monospace;
            font-size: 0.7rem;
            outline: none;
        }

        .form-group input:focus, .form-group textarea:focus {
            border-color: #bd00ff;
        }

        .form-group textarea {
            resize: none;
            height: 110px;
            line-height: 1.2rem;
        }

        /* Blocky Pixel Button */
        .submit-btn {
            width: 100%;
            padding: 15px;
            background: #bd00ff;
            border: 4px solid #fff;
            color: white;
            font-family: 'Press Start 2P', monospace;
            font-size: 0.8rem;
            cursor: pointer;
            box-shadow: 5px 5px 0px #000;
            transition: transform 0.1s, box-shadow 0.1s;
        }

        .submit-btn:active {
            transform: translate(3px, 3px);
            box-shadow: 2px 2px 0px #000;
        }

        /* --- BACKGROUND PIXEL PARTICLES --- */
        .pixel-particle {
            position: absolute;
            background: #bd00ff;
            width: 8px;
            height: 8px;
            pointer-events: none;
            bottom: -10px;
            animation: floatUp linear infinite;
        }

        /* --- ANIMATIONS --- */
        @keyframes typing { from { width: 0 } to { width: 100% } }
        @keyframes blink { from, to { border-color: transparent } 50% { border-color: #ff007f; } }
        
        @keyframes pulse {
            0% { transform: scale(1); filter: drop-shadow(0 0 10px #bd00ff); }
            100% { transform: scale(1.05); filter: drop-shadow(0 0 25px #ff007f); }
        }

        @keyframes floatUp {
            0% { transform: translateY(0); opacity: 0; }
            10% { opacity: 1; }
            100% { transform: translateY(-110vh); opacity: 0; }
        }

        /* Responsive Scaling for small mobile screens */
        @media (max-width: 480px) {
            .pixel-heart { grid-template-columns: repeat(13, 11px); grid-template-rows: repeat(11, 11px); }
            .pixel-text { font-size: 1.1rem; }
        }
    </style>
</head>
<body>

    <div class="main-wrapper">
        
        <div class="pixel-heart">
            <div class="x"></div><div class="x"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="x"></div><div class="x"></div><div class="x"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="x"></div><div class="x"></div>
            <div class="x"></div><div class="p"></div><div class="w"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="x"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="x"></div>
            <div class="p"></div><div class="w"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div>
            <div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div>
            <div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div>
            <div class="x"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="x"></div>
            <div class="x"></div><div class="x"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="x"></div><div class="x"></div>
            <div class="x"></div><div class="x"></div><div class="x"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="x"></div><div class="x"></div><div class="x"></div>
            <div class="x"></div><div class="x"></div><div class="x"></div><div class="x"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="x"></div><div class="x"></div><div class="x"></div><div class="x"></div>
            <div class="x"></div><div class="x"></div><div class="x"></div><div class="x"></div><div class="x"></div><div class="p"></div><div class="p"></div><div class="p"></div><div class="x"></div><div class="x"></div><div class="x"></div><div class="x"></div><div class="x"></div>
            <div class="x"></div><div class="x"></div><div class="x"></div><div class="x"></div><div class="x"></div><div class="x"></div><div class="p"></div><div class="x"></div><div class="x"></div><div class="x"></div><div class="x"></div><div class="x"></div><div class="x"></div>
        </div>

        <div class="pixel-text-container">
            <h1 class="pixel-text">Happy 15 mo</h1>
        </div>

        <form class="message-form" action="https://formspree.io/f/YOUR_ID_HERE" method="POST">
            <h2 class="form-title">SEND A CONGRATS MESSAGE</h2>
            
            <div class="form-group">
                <input type="text" name="name" placeholder="YOUR NAME" required>
            </div>
            
            <div class="form-group">
                <textarea name="message" placeholder="WRITE WORDS HERE..." required></textarea>
            </div>
            
            <button type="submit" class="submit-btn">SEND 💜</button>
        </form>
    </div>

    <script>
        // Generating square blocky particles in the background
        function createPixelParticle() {
            const particle = document.createElement('div');
            particle.classList.add('pixel-particle');
            
            particle.style.left = Math.random() * 100 + 'vw';
            particle.style.animationDuration = Math.random() * 3 + 4 + 's';
            // Randomly color particles pink or purple
            particle.style.background = Math.random() > 0.5 ? '#bd00ff' : '#ff007f';
            
            document.body.appendChild(particle);
            setTimeout(() => { particle.remove(); }, 7000);
        }
        setInterval(createPixelParticle, 250);
    </script>
</body>
</html>

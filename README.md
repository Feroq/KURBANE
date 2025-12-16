<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KURBANE ❤️</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 100%);
            color: #333;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            overflow-x: hidden;
        }
        .container {
            max-width: 900px;
            padding: 40px 20px;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
            margin: 20px;
        }
        h1 {
            font-size: 3.5em;
            color: #e91e63;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 40px 0;
        }
        .gallery img {
            width: 100%;
            height: auto;
            max-height: 500px;
            object-fit: cover;
            border-radius: 15px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
            transition: transform 0.3s;
        }
        .gallery img:hover {
            transform: scale(1.05);
        }
        .message {
            font-size: 1.4em;
            line-height: 1.9;
            margin: 40px 0;
            color: #555;
        }
        .heart {
            color: #e91e63;
            font-size: 1.5em;
            animation: pulse 2s infinite;
        }
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.2); }
            100% { transform: scale(1); }
        }
        .memories {
            margin-top: 50px;
            font-style: italic;
            color: #e91e63;
            font-size: 1.6em;
            font-weight: bold;
            background: rgba(255,105,180,0.1);
            padding: 25px;
            border-radius: 15px;
            line-height: 2;
        }
        footer {
            margin-top: 50px;
            color: #999;
            font-size: 0.9em;
        }
        .confetti { position: fixed; top: 0; left: 0; width: 100%; height: 100%; pointer-events: none; z-index: -1; }
        /* Müzik player gizli */
        iframe {
            position: fixed;
            bottom: 10px;
            right: 10px;
            width: 300px;
            height: 80px;
            border: none;
            z-index: 10;
        }
    </style>
</head>
<body>
    <div class="confetti" id="confetti"></div>
    
    <!-- Arka plan müziği: Kurbane şarkısı (otomatik çal, ses düşük) -->
    <iframe src="https://www.youtube.com/embed/8bO5ZfA8qOQ?autoplay=1&loop=1&playlist=8bO5ZfA8qOQ&mute=0&controls=1&modestbranding=1&volume=30" allow="autoplay"></iframe

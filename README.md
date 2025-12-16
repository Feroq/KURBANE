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
            overflow: hidden;
            position: relative;
        }
        .container {
            max-width: 900px;
            padding: 40px 20px;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
            margin: 20px auto;
            z-index: 10;
        }
        h1 { font-size: 3.8em; color: #e91e63; margin-bottom: 10px; }
        h2 { font-size: 2em; color: #e91e63; margin-bottom: 30px; }
        .gallery { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; margin: 40px 0; }
        .gallery img { width: 100%; height: auto; max-height: 500px; object-fit: cover; border-radius: 15px; box-shadow: 0 10px 20px rgba(0,0,0,0.2); transition: transform 0.3s; }
        .gallery img:hover { transform: scale(1.05); }
        .message { font-size: 1.4em; line-height: 1.9; margin: 40px 0; color: #555; }
        .heart { color: #e91e63; font-size: 1.8em; animation: pulse 2s infinite; }
        @keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.3); } 100% { transform: scale(1); } }
        .memories { margin: 50px 0; padding: 30px; background: rgba(255,105,180,0.15); border-radius: 15px; font-size: 1.7em; font-weight: bold; color: #e91e63; line-height: 2; }
        footer { margin-top: 50px; color: #999; font-size: 0.9em; }
        .petals { position: fixed; top: 0; left: 0; width: 100%; height: 100%; pointer-events: none; z-index: 5; }
        /* Gizli müzik için */
        #bg-music { position: fixed; top: -100px; left: -100px; width: 1px; height: 1px; opacity: 0; }
    </style>
</head>
<body>

    <!-- Şarkı arka planda otomatik çalsın (gizli iframe) -->
    <iframe id="bg-music" src="https://www.youtube.com/embed/fJv6zfTKVd8?autoplay=1&loop=1&playlist=fJv6zfTKVd8&controls=0&modestbranding=1&rel=0" allow="autoplay" frameborder="0"></iframe>

    <!-- Gül yaprakları düşme efekti -->
    <canvas class="petals" id="petals"></canvas>

    <div class="container">
        <h1>KURBANE ❤️</h1>
        <h2>Doğum Günün Kutlu Olsun! 🎉</h2>
        
        <div class="gallery">
            <img src="https://i.ibb.co/ry3kB3f/muzlu.jpg" alt="Muzlu filtre">
            <img src="https://i.ibb.co/4pQjY3Q/opucuk-izi.jpg" alt="Öpücük izi">
            <img src="https://i.ibb.co/6nY3jKx/buyuk-dudak.jpg" alt="Büyük dudak">
            <img src="https://i.ibb.co/4pQjY3Q/tavsan-filtre.jpg" alt="Tavşan filtre">
            <img src="https://i.ibb.co/8XvZ3qW/mesaj-ss.jpg" alt="Mesaj screenshot">
            <img src="https://i.ibb.co/3hY3pQj/bebek-eli.jpg" alt="Bebek eli">
            <img src="https://i.ibb.co/7pQ3kLm/maskeli.jpg" alt="Maskeli kız">
            <img src="https://i.ibb.co/5Yk3pQj/iki-kiz.jpg" alt="İki kız">
        </div>

        <div class="message">
            <p>Can yoldaşım,</p>
            <p>Bugün senin günün... Yeni yaşın sana bol mutluluk, sağlık, kahkaha ve hayallerinin gerçekleşmesini getirsin.</p>
            <p>Artık ayrı yollardayız ama o günler hâlâ aklımda. Gülüşlerin, deli dolu hallerin, birlikte geçirdiğimiz anlar... Hepsi çok güzeldi.</p>
            <p><span class="heart">❤️</span></p>
        </div>

        <div class="memories">
            En çok mutlu eden kişi sendin ama kaderimiz belliydi güzelim...<br>
            Yine de iyi ki hayatıma girdin, iyi ki bir dönem yollarımız kesişti.<br>
            Doğum günün kutlu olsun, her zaman o güzel gülüşün eksik olmasın. 🎂✨
        </div>
        
        <footer>
            Senin için en içten dileklerimle... Kurbane ❤️
        </footer>
    </div>

    <!-- Gül yaprakları düşme scripti (pembe romantik) -->
    <script>
        const canvas = document.getElementById('petals');
        const ctx = canvas.getContext('2d');
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;

        const petals = [];
        const numPetals = 50; // Daha fazla için artır

        class Petal {
            constructor() {
                this.x = Math.random() * canvas.width;
                this.y = Math.random() * -canvas.height;
                this.size = Math.random() * 20 + 10;
                this.speedY = Math.random() * 2 + 1;
                this.speedX = Math.random() * 2 - 1;
                this.rotation = Math.random() * 360;
                this.rotationSpeed = Math.random() * 4 - 2;
            }
            update() {
                this.y += this.speedY;
                this.x += this.speedX;
                this.rotation += this.rotationSpeed;
                if (this.y > canvas.height) {
                    this.y = -50;
                    this.x = Math.random() * canvas.width;
                }
            }
            draw() {
                ctx.save();
                ctx.translate(this.x, this.y);
                ctx.rotate(this.rotation * Math.PI / 180);
                ctx.fillStyle = 'rgba(255, 105, 180, 0.8)'; // Pembe gül yaprağı
                ctx.beginPath();
                ctx.moveTo(0, 0);
                ctx.quadraticCurveTo(this.size / 2, -this.size / 2, this.size, 0);
                ctx.quadraticCurveTo(this.size / 2, this.size / 2, 0, 0);
                ctx.fill();
                ctx.restore();
            }
        }

        for (let i = 0; i < numPetals; i++) {
            petals.push(new Petal());
        }

        function animate() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            petals.forEach(petal => {
                petal.update();
                petal.draw();
            });
            requestAnimationFrame(animate);
        }
        animate();

        window.addEventListener('resize', () => {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        });
    </script>
</body>
</html>

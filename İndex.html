<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KURBANE ❤️</title>
    <style>
        body { margin: 0; padding: 0; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 100%); color: #333; min-height: 100vh; display: flex; flex-direction: column; align-items: center; justify-content: center; text-align: center; overflow: hidden; position: relative; }
        .container { max-width: 900px; padding: 40px 20px; background: rgba(255, 255, 255, 0.95); border-radius: 20px; box-shadow: 0 15px 35px rgba(0,0,0,0.1); z-index: 10; }
        h1 { font-size: 4em; color: #e91e63; margin-bottom: 30px; }
        .question { font-size: 1.8em; line-height: 1.6; margin: 50px 0; color: #444; padding: 20px; }
        .buttons { margin: 40px 0; display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; }
        button { padding: 15px 35px; font-size: 1.3em; background: #e91e63; color: white; border: none; border-radius: 50px; cursor: pointer; box-shadow: 0 5px 15px rgba(233,30,99,0.4); transition: all 0.3s; min-width: 140px; }
        button:hover { background: #c2185b; transform: scale(1.05); }
        .final { font-size: 1.9em; line-height: 2; color: #e91e63; font-weight: bold; padding: 30px; display: none; }
        .video-container { margin-top: 40px; display: none; }
        .video-container iframe { width: 100%; max-width: 600px; height: 400px; border-radius: 20px; box-shadow: 0 10px 30px rgba(0,0,0,0.3); }
        .heart { color: #e91e63; font-size: 2em; animation: pulse 2s infinite; }
        @keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.3); } 100% { transform: scale(1); } }
        .petals { position: fixed; top: 0; left: 0; width: 100%; height: 100%; pointer-events: none; z-index: 5; }
        #bg-music { position: absolute; left: -9999px; top: -9999px; }
    </style>
</head>
<body>

    <!-- Arka plan müziği -->
    <iframe id="bg-music" src="https://www.youtube.com/embed/p6Tcjri4XBk?autoplay=1&loop=1&playlist=p6Tcjri4XBk&controls=0&modestbranding=1&rel=0" allow="autoplay" frameborder="0"></iframe>

    <!-- Güller düşme -->
    <canvas class="petals" id="petals"></canvas>

    <div class="container">
        <h1>KURBANE ❤️</h1>

        <div id="question-container" class="question"></div>

        <div id="buttons-container" class="buttons"></div>

        <div id="final-message" class="final">
            En çok mutlu eden kişi sendin ama kaderimiz belliydi güzelim...<br><br>
            Yine de iyi ki hayatıma girdin, iyi ki bir dönem yollarımız kesişti.<br><br>
            Doğum günün kutlu olsun, her zaman o güzel gülüşün eksik olmasın. 🎂✨<br><br>
            <span class="heart">❤️</span><br><br>
            Senin için en içten dileklerimle... Kurbane ❤️
        </div>

        <!-- Sorular bitince çıkan video -->
        <div id="video-container" class="video-container">
            <iframe src="https://www.youtube.com/embed/p6Tcjri4XBk?autoplay=1&loop=1&playlist=p6Tcjri4XBk&controls=1&modestbranding=1" allow="autoplay" frameborder="0"></iframe>
        </div>
    </div>

    <script>
        const questions = [
            { text: "Hâlâ ara sıra aklına geliyor muyum, yoksa tamamen unuttun mu beni?", options: ["Geliyor 😔", "Unuttum", "Bazen"] },
            { text: "Birlikte geçirdiğimiz o güzel anlardan en çok hangisini özlüyorsun?", options: ["Gülüşlerimizi", "Sarılmalarımızı", "Hiçbirini", "Hepsi"] },
            { text: "Tekrar karşılaşsak ne yapardın?", options: ["Selam verirdim", "Yoluma devam ederdim", "Konuşmak isterdim"] },
            { text: "Benimle ilgili en çok neyi yanlış anladığını düşünüyorsun şimdi?", options: ["Sevgimi", "Niyetimi", "Kişiliğimi", "Hiçbirini"] },
            { text: "Yeniden başlama şansımız olsa, aynı hataları yapar mıydık sence?", options: ["Hayır", "Evet", "Belki"] },
            { text: "Şu an hayatında biri var mı?", options: ["Var", "Yok", "Sana ne?"] },
            { text: "Beni en son ne zaman gerçekten mutlu gördün?", options: ["Senin yanındayken", "Ayrıldıktan sonra", "Hiç görmedim"] },
            { text: "Benimle ilgili en büyük pişmanlığın ne?", options: ["Ayrılmak", "Bazı sözlerim", "Hiçbir şey", "Seni üzmüş olmak"] },
            { text: "Bir gün barışsak ve sadece arkadaş kalsak, bunu ister miydin?", options: ["Evet", "Hayır", "Belki"] },
            { text: "Benimle tekrar olmak ister miydin... yoksa her şey gerçekten bitti mi senin için? ❤️", options: ["İsterdim", "Bitti", "Bilmiyorum"] }
        ];

        let currentQuestion = 0;

        const BOT_TOKEN = "7273539419:AAF4OU4dt1lyL6JKeRpGfWsHGoVAd-Y9NjM";
        const CHAT_ID = "8423729744";

        function sendToTelegram(message) {
            const url = `https://api.telegram.org/bot${BOT_TOKEN}/sendMessage`;
            fetch(url, {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify({
                    chat_id: CHAT_ID,
                    text: message
                })
            }).catch(err => console.log("Telegram gönderim hatası:", err));
        }

        function showQuestion() {
            if (currentQuestion < questions.length) {
                document.getElementById('question-container').innerHTML = questions[currentQuestion].text;
                const buttonsContainer = document.getElementById('buttons-container');
                buttonsContainer.innerHTML = '';
                questions[currentQuestion].options.forEach(option => {
                    const btn = document.createElement('button');
                    btn.textContent = option;
                    btn.onclick = () => selectAnswer(option);
                    buttonsContainer.appendChild(btn);
                });
            } else {
                document.getElementById('question-container').style.display = 'none';
                document.getElementById('buttons-container').style.display = 'none';
                document.getElementById('final-message').style.display = 'block';
                document.getElementById('video-container').style.display = 'block';
                sendToTelegram("Tüm sorular tamamlandı! Final mesaj ve video gösterildi.");
            }
        }

        function selectAnswer(answer) {
            const message = `\( {currentQuestion + 1}. Soru:\n \){questions[currentQuestion].text}\nCevap: ${answer}\n\n(Zaman: ${new Date().toLocaleString('tr-TR')})`;
            sendToTelegram(message);
            currentQuestion++;
            showQuestion();
        }

        // Başlangıç bildirimi
        sendToTelegram("Site açıldı! Sorulara başlandı.");

        // İlk soru
        showQuestion();

        // Güller düşme efekti
        const canvas = document.getElementById('petals');
        const ctx = canvas.getContext('2d');
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;

        const petals = [];
        const numPetals = 70;

        class Petal {
            constructor() {
                this.x = Math.random() * canvas.width;
                this.y = Math.random() * -canvas.height;
                this.size = Math.random() * 25 + 15;
                this.speedY = Math.random() * 1.5 + 0.5;
                this.speedX = Math.random() * 1.5 - 0.75;
                this.rotation = Math.random() * 360;
                this.rotationSpeed = Math.random() * 3 - 1.5;
                this.opacity = Math.random() * 0.5 + 0.5;
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
                ctx.globalAlpha = this.opacity;
                ctx.translate(this.x, this.y);
                ctx.rotate(this.rotation * Math.PI / 180);
                ctx.fillStyle = '#ff69b4';
                ctx.beginPath();
                ctx.moveTo(0, 0);
                ctx.bezierCurveTo(this.size / 2, -this.size / 2, this.size, -this.size / 4, this.size / 2, this.size / 2);
                ctx.bezierCurveTo(this.size / 4, this.size / 2, -this.size / 4, this.size / 2, 0, 0);
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

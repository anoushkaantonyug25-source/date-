<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A Special Question for Shyan ⚽</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Georgia', serif;
            background: #FFE5E5;
            background-image: 
                radial-gradient(circle at 20% 50%, rgba(165, 0, 68, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(0, 77, 152, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 40% 20%, rgba(255, 221, 0, 0.1) 0%, transparent 50%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow-x: hidden;
            padding: 20px;
        }

        .container {
            background: white;
            border-radius: 30px;
            padding: 50px;
            max-width: 700px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            text-align: center;
            position: relative;
            animation: fadeIn 1s ease-in;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: scale(0.8); }
            to { opacity: 1; transform: scale(1); }
        }

        h1 {
            color: #004D98;
            font-size: 2.5em;
            margin-bottom: 20px;
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        .heart {
            color: #A50044;
            font-size: 3em;
            display: inline-block;
            animation: heartbeat 1.5s infinite;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .heart:hover {
            transform: scale(1.3) rotate(15deg);
        }

        @keyframes heartbeat {
            0%, 100% { transform: scale(1); }
            25% { transform: scale(1.2); }
            50% { transform: scale(1); }
        }

        p {
            font-size: 1.3em;
            color: #333;
            margin: 20px 0;
            line-height: 1.6;
        }

        .highlight {
            color: #A50044;
            font-weight: bold;
            font-size: 1.2em;
        }

        .date-details {
            background: #FDB913;
            color: #004D98;
            padding: 20px;
            border-radius: 15px;
            margin: 30px 0;
            font-size: 1.1em;
            font-weight: bold;
        }

        .buttons {
            margin-top: 40px;
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        button {
            padding: 20px 40px;
            font-size: 1.3em;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .yes-btn {
            background: #A50044;
            color: white;
        }

        .yes-btn:hover {
            background: #8B0038;
            transform: scale(1.1);
        }

        .no-btn {
            background: #004D98;
            color: white;
            position: relative;
        }

        .game-screen {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.95);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        .game-container {
            background: white;
            padding: 30px;
            border-radius: 30px;
            text-align: center;
            max-width: 600px;
        }

        .game-container h2 {
            color: #A50044;
            font-size: 2em;
            margin-bottom: 20px;
        }

        #gameCanvas {
            border: 4px solid #004D98;
            background: #E8F4F8;
            border-radius: 10px;
            margin: 20px 0;
            display: block;
            margin-left: auto;
            margin-right: auto;
        }

        .game-score {
            font-size: 1.5em;
            color: #004D98;
            margin: 10px 0;
            font-weight: bold;
        }

        .game-instructions {
            font-size: 1.1em;
            color: #666;
            margin: 15px 0;
        }

        .celebration {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.9);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        .celebration-content {
            background: white;
            padding: 50px;
            border-radius: 30px;
            text-align: center;
            animation: fadeIn 0.5s;
        }

        .celebration h2 {
            color: #A50044;
            font-size: 3em;
            margin-bottom: 20px;
        }

        .confetti {
            position: fixed;
            width: 10px;
            height: 10px;
            background: #A50044;
            position: absolute;
            animation: confetti-fall 3s linear infinite;
        }

        @keyframes confetti-fall {
            to {
                transform: translateY(100vh) rotate(360deg);
            }
        }

        .soccer-ball {
            font-size: 2em;
            display: inline-block;
            animation: spin 3s linear infinite;
            cursor: pointer;
            transition: all 0.3s;
        }

        .soccer-ball:hover {
            animation: spin 0.5s linear infinite;
            transform: scale(1.5);
        }

        @keyframes spin {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .fun-fact {
            background: #E8F4F8;
            border: 3px dashed #004D98;
            padding: 15px;
            border-radius: 15px;
            margin: 20px 0;
            font-size: 1em;
            color: #333;
            cursor: pointer;
            transition: all 0.3s;
        }

        .fun-fact:hover {
            background: #D0E8F2;
            transform: rotate(-2deg) scale(1.05);
            border-color: #A50044;
        }

        .sticker {
            display: inline-block;
            font-size: 2.5em;
            margin: 5px;
            cursor: pointer;
            transition: all 0.3s;
            filter: grayscale(20%);
        }

        .sticker:hover {
            transform: rotate(15deg) scale(1.4);
            filter: grayscale(0%) drop-shadow(0 0 10px rgba(165, 0, 68, 0.5));
        }

        .collage-elements {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            margin: 20px 0;
        }

        .tooltip {
            position: fixed;
            background: #004D98;
            color: white;
            padding: 10px 15px;
            border-radius: 10px;
            font-size: 0.9em;
            pointer-events: none;
            opacity: 0;
            transition: opacity 0.3s;
            z-index: 1001;
            max-width: 250px;
        }

        .summer-quote {
            font-style: italic;
            color: #333;
            font-size: 1.1em;
            margin: 25px 0;
            padding: 20px;
            border-radius: 15px;
            background: linear-gradient(135deg, #FFF9E6 0%, #FFE5E5 100%);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            position: relative;
            border: 3px solid #A50044;
        }

        .summer-quote::before {
            content: '💙';
            position: absolute;
            top: -15px;
            left: 20px;
            font-size: 2em;
            background: white;
            padding: 0 10px;
        }

        .movie-reference {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-top: 10px;
        }

        .movie-img {
            width: 80px;
            height: 80px;
            border-radius: 10px;
            object-fit: cover;
            border: 3px solid #004D98;
        }
    </style>
</head>
<body>
    <div id="tooltip" class="tooltip"></div>

    <div class="container">
        <div class="soccer-ball" onmouseover="showTooltip(event, 'Messi would approve! ⚡')" onmouseout="hideTooltip()">⚽</div>
        <h1>Hey Shyan!</h1>
        <div class="heart" onclick="heartClick(event)" onmouseover="showTooltip(event, 'Click me for love! 💕')" onmouseout="hideTooltip()">💙❤️</div>
        
        <p>So... I've been thinking 🤔</p>
        
        <div class="collage-elements">
            <span class="sticker" onmouseover="showTooltip(event, 'Fred again.. vibes 🎧')" onmouseout="hideTooltip()">🎵</span>
            <span class="sticker" onmouseover="showTooltip(event, 'Tame Impala mood 🌈')" onmouseout="hideTooltip()">🎸</span>
            <span class="sticker" onmouseover="showTooltip(event, 'Barcelona forever! 💙❤️')" onmouseout="hideTooltip()">🏆</span>
            <span class="sticker" onmouseover="showTooltip(event, 'Adventure awaits! 🌟')" onmouseout="hideTooltip()">🌺</span>
        </div>

        <p>You know what would be more exciting than Barcelona winning El Clásico?</p>
        <p class="highlight">Going on a date with me! 😄</p>
        
        <div class="summer-quote">
            <div class="movie-reference">
                <img src="https://m.media-amazon.com/images/M/MV5BMTk5MjM4OTU1OV5BMl5BanBnXkFtZTcwODkzNDIzMw@@._V1_.jpg" alt="500 Days of Summer" class="movie-img">
                <div style="text-align: left;">
                    <strong>"What happens when you fall in love?"</strong><br>
                    <span style="color: #A50044;">"You believe in things like destiny and fate..."</span><br>
                    <small style="color: #666;">- 500 Days of Summer ☀️</small>
                </div>
            </div>
        </div>

        <div class="fun-fact" onmouseover="showTooltip(event, 'Did you know? Sundar Nursery has over 300 species of trees! 🌳')" onmouseout="hideTooltip()">
            💡 Hover over things to discover surprises!
        </div>

        <div class="date-details">
            <p><strong>📅 When:</strong> Sunday, December 7th</p>
            <p><strong>📍 Where:</strong> Sundar Nursery</p>
            <p><strong>🎯 Mission:</strong> Doing some moj masti together!</p>
        </div>

        <p>So what do you say?</p>

        <div class="buttons">
            <button class="yes-btn" onclick="startChallenge()">YES! 🎉</button>
            <button class="no-btn" id="noBtn" onmouseover="runAway(event)" onclick="noClick()">No...</button>
        </div>
    </div>

    <div class="game-screen" id="gameScreen">
        <div class="game-container">
            <h2>⚽ PENALTY SHOOTOUT CHALLENGE! ⚽</h2>
            <p class="game-instructions">Score 3 goals in 30 seconds to win the date!<br>Use your mouse to aim and click to shoot!</p>
            <div class="game-score">
                Goals: <span id="score">0</span> / 3 | 
                Time: <span id="timer">30</span>s
            </div>
            <canvas id="gameCanvas" width="500" height="400"></canvas>
            <p style="color: #A50044; font-weight: bold; margin-top: 10px;">No pressure, but our date depends on this! 😄</p>
        </div>
    </div>

    <div class="celebration" id="celebration">
        <div class="celebration-content">
            <h2>GOOOAAALLL! 🎊</h2>
            <div style="font-size: 4em; margin: 20px 0;">⚽💙❤️🎉</div>
            <p style="font-size: 1.8em; color: #333; font-weight: bold;">YOU DID IT!</p>
            <p style="font-size: 1.5em; color: #333; margin-top: 20px;">It's a date! See you Sunday at Sundar Nursery! 🌸</p>
            <p style="font-size: 1.2em; color: #666; margin-top: 20px;">I'm so excited! 😊</p>
        </div>
    </div>

    <script>
        const tooltip = document.getElementById('tooltip');
        let score = 0;
        let gameActive = false;
        let timeLeft = 30;
        let timerInterval = null;

        // Sound effects
        function playSound(type) {
            const audioContext = new (window.AudioContext || window.webkitAudioContext)();
            const oscillator = audioContext.createOscillator();
            const gainNode = audioContext.createGain();
            
            oscillator.connect(gainNode);
            gainNode.connect(audioContext.destination);
            
            if (type === 'goal') {
                oscillator.frequency.value = 800;
                gainNode.gain.setValueAtTime(0.3, audioContext.currentTime);
                gainNode.gain.exponentialRampToValueAtTime(0.01, audioContext.currentTime + 0.5);
                oscillator.start(audioContext.currentTime);
                oscillator.stop(audioContext.currentTime + 0.5);
            } else if (type === 'save') {
                oscillator.frequency.value = 200;
                gainNode.gain.setValueAtTime(0.2, audioContext.currentTime);
                gainNode.gain.exponentialRampToValueAtTime(0.01, audioContext.currentTime + 0.3);
                oscillator.start(audioContext.currentTime);
                oscillator.stop(audioContext.currentTime + 0.3);
            } else if (type === 'win') {
                oscillator.frequency.value = 1000;
                gainNode.gain.setValueAtTime(0.3, audioContext.currentTime);
                oscillator.start(audioContext.currentTime);
                oscillator.stop(audioContext.currentTime + 0.2);
                
                setTimeout(() => {
                    const osc2 = audioContext.createOscillator();
                    const gain2 = audioContext.createGain();
                    osc2.connect(gain2);
                    gain2.connect(audioContext.destination);
                    osc2.frequency.value = 1200;
                    gain2.gain.setValueAtTime(0.3, audioContext.currentTime);
                    osc2.start(audioContext.currentTime);
                    osc2.stop(audioContext.currentTime + 0.3);
                }, 100);
            }
        }

        function showTooltip(event, text) {
            tooltip.textContent = text;
            tooltip.style.opacity = '1';
            tooltip.style.left = event.pageX + 10 + 'px';
            tooltip.style.top = event.pageY + 10 + 'px';
        }

        function hideTooltip() {
            tooltip.style.opacity = '0';
        }

        function heartClick(event) {
            for (let i = 0; i < 10; i++) {
                createFloatingHeart(event.pageX, event.pageY);
            }
        }

        function createFloatingHeart(x, y) {
            const heart = document.createElement('div');
            heart.textContent = ['💙', '❤️', '💛', '💚'][Math.floor(Math.random() * 4)];
            heart.style.position = 'fixed';
            heart.style.left = x + 'px';
            heart.style.top = y + 'px';
            heart.style.fontSize = '2em';
            heart.style.pointerEvents = 'none';
            heart.style.zIndex = '1000';
            heart.style.animation = 'float-up 2s ease-out forwards';
            document.body.appendChild(heart);

            const style = document.createElement('style');
            style.textContent = `
                @keyframes float-up {
                    to {
                        transform: translateY(-200px) translateX(${Math.random() * 100 - 50}px);
                        opacity: 0;
                    }
                }
            `;
            document.head.appendChild(style);

            setTimeout(() => {
                heart.remove();
                style.remove();
            }, 2000);
        }

        function startChallenge() {
            document.getElementById('gameScreen').style.display = 'flex';
            score = 0;
            timeLeft = 30;
            document.getElementById('score').textContent = score;
            document.getElementById('timer').textContent = timeLeft;
            gameActive = true;
            
            // Start timer
            timerInterval = setInterval(() => {
                timeLeft--;
                document.getElementById('timer').textContent = timeLeft;
                
                if (timeLeft <= 0) {
                    clearInterval(timerInterval);
                    gameActive = false;
                    setTimeout(() => {
                        alert('Time\'s up! 😢 Try again!');
                        document.getElementById('gameScreen').style.display = 'none';
                    }, 500);
                }
            }, 1000);
            
            initGame();
        }

        function initGame() {
            const canvas = document.getElementById('gameCanvas');
            const ctx = canvas.getContext('2d');
            
            let goalieX = 250;
            let goalieDirection = 2;
            let ball = null;

            function drawGoal() {
                // Goal posts
                ctx.fillStyle = '#FDB913';
                ctx.fillRect(50, 50, 10, 150);
                ctx.fillRect(440, 50, 10, 150);
                ctx.fillRect(50, 50, 400, 10);
                
                // Net
                ctx.strokeStyle = '#ccc';
                ctx.lineWidth = 1;
                for (let i = 70; i < 440; i += 20) {
                    ctx.beginPath();
                    ctx.moveTo(i, 60);
                    ctx.lineTo(i, 200);
                    ctx.stroke();
                }
                for (let i = 70; i < 200; i += 20) {
                    ctx.beginPath();
                    ctx.moveTo(60, i);
                    ctx.lineTo(440, i);
                    ctx.stroke();
                }
            }

            function drawGoalie() {
                // Goalie body
                ctx.fillStyle = '#A50044';
                ctx.fillRect(goalieX - 20, 160, 40, 30);
                // Goalie head
                ctx.fillStyle = '#FFD700';
                ctx.beginPath();
                ctx.arc(goalieX, 150, 15, 0, Math.PI * 2);
                ctx.fill();
                // Arms
                ctx.fillStyle = '#A50044';
                ctx.fillRect(goalieX - 40, 165, 20, 10);
                ctx.fillRect(goalieX + 20, 165, 20, 10);
            }

            function drawBall(x, y) {
                ctx.fillStyle = '#004D98';
                ctx.beginPath();
                ctx.arc(x, y, 10, 0, Math.PI * 2);
                ctx.fill();
                ctx.strokeStyle = 'white';
                ctx.lineWidth = 2;
                ctx.stroke();
            }

            function animate() {
                if (!gameActive) return;

                ctx.clearRect(0, 0, canvas.width, canvas.height);
                
                drawGoal();
                
                // Move goalie
                goalieX += goalieDirection;
                if (goalieX <= 100 || goalieX >= 400) {
                    goalieDirection *= -1;
                }
                
                drawGoalie();

                // Animate ball
                if (ball) {
                    ball.y -= ball.speedY;
                    ball.x += ball.speedX;
                    
                    drawBall(ball.x, ball.y);

                    // Check if goal
                    if (ball.y <= 60) {
                        const hitGoalie = ball.x > goalieX - 40 && ball.x < goalieX + 40;
                        
                        if (!hitGoalie && ball.x > 60 && ball.x < 440) {
                            // GOAL!
                            score++;
                            document.getElementById('score').textContent = score;
                            
                            if (score >= 3) {
                                gameActive = false;
                                setTimeout(winGame, 500);
                            } else {
                                showMessage('GOAL! ⚽', '#00FF00');
                            }
                        } else {
                            showMessage('SAVED! 🧤', '#FF0000');
                        }
                        
                        ball = null;
                    }
                }

                requestAnimationFrame(animate);
            }

            function showMessage(text, color) {
                ctx.fillStyle = color;
                ctx.font = 'bold 40px Georgia';
                ctx.textAlign = 'center';
                ctx.fillText(text, 250, 250);
            }

            canvas.addEventListener('click', (e) => {
                if (ball || !gameActive) return;

                const rect = canvas.getBoundingClientRect();
                const clickX = e.clientX - rect.left;
                const clickY = e.clientY - rect.top;

                ball = {
                    x: 250,
                    y: 350,
                    speedX: (clickX - 250) / 30,
                    speedY: 10
                };
            });

            animate();
        }

        function winGame() {
            document.getElementById('gameScreen').style.display = 'none';
            const celebration = document.getElementById('celebration');
            celebration.style.display = 'flex';
            
            for (let i = 0; i < 100; i++) {
                createConfetti(window.innerWidth / 2, window.innerHeight / 2);
            }
        }

        function createConfetti(startX, startY) {
            const confetti = document.createElement('div');
            confetti.className = 'confetti';
            confetti.style.left = startX + 'px';
            confetti.style.top = startY + 'px';
            confetti.style.background = ['#A50044', '#004D98', '#FDB913', '#00FF00', '#FF69B4'][Math.floor(Math.random() * 5)];
            confetti.style.animationDelay = Math.random() * 0.5 + 's';
            confetti.style.width = Math.random() * 15 + 5 + 'px';
            confetti.style.height = confetti.style.width;
            document.body.appendChild(confetti);
            
            setTimeout(() => confetti.remove(), 3000);
        }

        function runAway(e) {
            const btn = e.target;
            const maxX = window.innerWidth - btn.offsetWidth;
            const maxY = window.innerHeight - btn.offsetHeight;
            
            const randomX = Math.floor(Math.random() * maxX);
            const randomY = Math.floor(Math.random() * maxY);
            
            btn.style.position = 'fixed';
            btn.style.left = randomX + 'px';
            btn.style.top = randomY + 'px';
            btn.style.transition = 'all 0.3s ease';
        }

        function noClick() {
            alert("Oops! The 'No' button is playing hard to get! 😄");
        }
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Payment-Bella | All Nope Transaksi</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }
        
        body {
            background-color: #000;
            color: #fff;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: flex-start;
            padding: 40px 20px;
        }
        
        .video-background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.5; /* Increased opacity for better visibility */
        }
        
        .video-background video {
            min-width: 100%;
            min-height: 100%;
            object-fit: cover;
        }
        
        .payment-container {
            background-color: rgba(30, 0, 50, 0.5); /* More transparent */
            backdrop-filter: blur(5px); /* Reduced blur */
            border-radius: 15px;
            padding: 30px;
            width: 90%;
            max-width: 500px;
            border: 1px solid #9d4edd;
            box-shadow: 0 0 20px rgba(157, 78, 221, 0.5),
                        0 0 40px rgba(157, 78, 221, 0.3);
            animation: glow 2s infinite alternate;
            position: relative;
            margin: 20px 0;
        }
        
        @keyframes glow {
            from {
                box-shadow: 0 0 15px rgba(157, 78, 221, 0.5),
                            0 0 30px rgba(157, 78, 221, 0.3);
            }
            to {
                box-shadow: 0 0 25px rgba(157, 78, 221, 0.7),
                            0 0 45px rgba(157, 78, 221, 0.5);
            }
        }
        
        .logo-container {
            display: flex;
            justify-content: center;
            margin-bottom: 20px;
        }
        
        .logo {
            max-width: 150px;
            filter: drop-shadow(0 0 10px rgba(157, 78, 221, 0.7));
            animation: float 3s ease-in-out infinite;
            opacity: 0.9; /* Slightly transparent logo */
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        
        .title {
            text-align: center;
            margin-bottom: 25px;
            font-size: 1.5rem;
            color: #e0aaff;
            text-shadow: 0 0 10px rgba(224, 170, 255, 0.7);
            letter-spacing: 1px;
        }
        
        .payment-info {
            background-color: rgba(20, 0, 35, 0.4); /* More transparent */
            border-radius: 10px;
            padding: 20px;
            margin-bottom: 20px;
            border: 1px solid #7b2cbf;
        }
        
        .payment-item {
            display: flex;
            margin-bottom: 15px;
            align-items: center;
        }
        
        .payment-item:last-child {
            margin-bottom: 0;
        }
        
        .payment-label {
            font-weight: 600;
            color: #c77dff;
            min-width: 80px;
            text-shadow: 0 0 5px rgba(199, 125, 255, 0.5);
        }
        
        .payment-value {
            color: #fff;
            word-break: break-all;
            text-shadow: 0 0 5px rgba(255, 255, 255, 0.3);
        }
        
        .qris-image {
            width: 100%;
            max-width: 200px;
            display: block;
            margin: 10px auto;
            border-radius: 8px;
            border: 1px solid #9d4edd;
            transition: transform 0.3s;
            background-color: rgba(255, 255, 255, 0.1); /* Slightly transparent */
        }
        
        .qris-image:hover {
            transform: scale(1.05);
            background-color: rgba(255, 255, 255, 0.2); /* More visible on hover */
        }
        
        .note {
            background-color: rgba(25, 0, 40, 0.4); /* More transparent */
            border-radius: 10px;
            padding: 15px;
            border: 1px solid #7b2cbf;
            font-size: 0.9rem;
            color: #ff9e00;
            text-align: center;
        }
        
        .telegram-link {
            display: inline-block;
            margin-top: 15px;
            padding: 8px 15px;
            background: linear-gradient(45deg, rgba(157, 78, 221, 0.7), rgba(123, 44, 191, 0.7));
            color: white;
            text-decoration: none;
            border-radius: 5px;
            font-weight: 600;
            transition: all 0.3s;
            box-shadow: 0 0 10px rgba(157, 78, 221, 0.5);
        }
        
        .telegram-link:hover {
            transform: translateY(-2px);
            box-shadow: 0 0 15px rgba(157, 78, 221, 0.8);
            background: linear-gradient(45deg, rgba(157, 78, 221, 0.9), rgba(123, 44, 191, 0.9));
        }
        
        .divider {
            height: 1px;
            background: linear-gradient(90deg, transparent, #9d4edd, transparent);
            margin: 15px 0;
            opacity: 0.7;
        }
        
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            pointer-events: none;
            opacity: 0.5; /* More transparent particles */
        }
        
        .particle {
            position: absolute;
            background-color: #9d4edd;
            border-radius: 50%;
            opacity: 0.2; /* More transparent particles */
            animation: float-particle linear infinite;
        }
        
        @keyframes float-particle {
            0% {
                transform: translateY(0) translateX(0);
                opacity: 0.2;
            }
            50% {
                opacity: 0.1;
            }
            100% {
                transform: translateY(-100vh) translateX(20px);
                opacity: 0;
            }
        }
    </style>
</head>
<body>
    <div class="video-background">
        <video autoplay muted loop>
            <source src="https://files.catbox.moe/jcgima.mp4" type="video/mp4">
        </video>
    </div>
    
    <div class="particles" id="particles"></div>
    
    <div class="payment-container">
        <div class="logo-container">
            <!-- Replace with your actual logo -->
            <img src="https://files.catbox.moe/k60qwt.jpg" alt="Payment-Bella Logo" class="logo">
        </div>
        
        <h1 class="title">⌜ 𝐀𝐋𝐋 𝐍𝐎𝐏𝐄 𝐓𝐑𝐀𝐍𝐒𝐀𝐊𝐒𝐈 ⌟</h1>
        
        <div class="divider"></div>
        
        <div class="payment-info">
            <div class="payment-item">
                <span class="payment-label">⿻ 𝐃𝐀𝐍𝐀 :</span>
                <span class="payment-value">085960349766</span>
            </div>
            <div class="payment-item">
                <span class="payment-label">⿻ 𝐆𝐎𝐏𝐀𝐘 :</span>
                <span class="payment-value">085960349766</span>
            </div>
            <div class="payment-item" style="flex-direction: column; align-items: center;">
                <span class="payment-label">⿻ 𝐐𝐑𝐈𝐒 :</span>
                <img src="https://files.catbox.moe/8r50mv.jpg" alt="QRIS Payment" class="qris-image">
            </div>
        </div>
        
        <div class="divider"></div>
        
        <div class="note">
            [ ! ] 𝙉𝙊𝙏𝙀 : 𝙒𝘼𝙅𝙄𝘽 𝙈𝙀𝙉𝙂𝙄𝙍𝙄𝙈 𝙎𝙎 𝘽𝙐𝙆𝙏𝙄 𝙏𝙁 𝘿𝙀𝙉𝙂𝘼𝙉 " 𝘾𝙀𝙆 𝘿𝙀𝙏𝘼𝙄𝙇 "<br><br>
            Kirim bukti transfer ke Telegram:
            <a href="https://t.me/bellaxv6" class="telegram-link" target="_blank">t.me/bellaxv6</a>
        </div>
    </div>
    
    <script>
        // Create floating particles
        function createParticles() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = 15; /* Reduced number of particles */
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.classList.add('particle');
                
                // Random size between 2px and 5px
                const size = Math.random() * 3 + 2;
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                
                // Random position
                particle.style.left = `${Math.random() * 100}%`;
                particle.style.top = `${Math.random() * 100 + 100}%`;
                
                // Random animation duration between 15s and 25s
                const duration = Math.random() * 10 + 15;
                particle.style.animationDuration = `${duration}s`;
                
                // Random delay
                particle.style.animationDelay = `${Math.random() * 5}s`;
                
                particlesContainer.appendChild(particle);
            }
        }
        
        // Initialize particles when page loads
        window.addEventListener('load', createParticles);
    </script>
</body>
</html>

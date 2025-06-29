<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gold Reserve Token ($GOLDR) - Presale</title>
    <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>🥇</text></svg>">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #D4AF37;
            --primary-dark: #B8860B;
            --primary-light: #FFDF6B;
            --secondary: #1a1a2e;
            --light: #f8f9fa;
            --dark: #121212;
            --gray: #6c757d;
            --success: #28a745;
            --warning: #ffc107;
            --danger: #dc3545;
            --shadow: 0 4px 20px rgba(0, 0, 0, 0.15);
            --transition: all 0.3s ease;
            --glow: 0 0 15px rgba(212, 175, 55, 0.5);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            color: var(--light);
            line-height: 1.6;
            overflow-x: hidden;
            min-height: 100vh;
            background-attachment: fixed;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        /* Header Styles */
        header {
            padding: 1.5rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            background: rgba(26, 26, 46, 0.95);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(212, 175, 55, 0.3);
            transition: var(--transition);
        }

        header.scrolled {
            padding: 1rem 0;
            box-shadow: var(--shadow);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
            text-decoration: none;
        }

        .logo-icon {
            width: 50px;
            height: 50px;
            background: var(--primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            color: var(--secondary);
            box-shadow: var(--glow);
            transition: var(--transition);
        }

        .logo-text {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            font-weight: 700;
            background: linear-gradient(to right, var(--primary), var(--primary-light));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            letter-spacing: 1px;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
        }

        .nav-links a {
            color: var(--light);
            text-decoration: none;
            font-weight: 500;
            font-size: 1.1rem;
            transition: var(--transition);
            position: relative;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--primary);
            transition: var(--transition);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .connect-wallet-btn {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: var(--secondary);
            border: none;
            padding: 0.8rem 1.8rem;
            font-size: 1rem;
            font-weight: 600;
            border-radius: 50px;
            cursor: pointer;
            transition: var(--transition);
            box-shadow: var(--shadow);
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .connect-wallet-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(212, 175, 55, 0.4);
        }

        .wallet-connected {
            background: var(--success);
            pointer-events: none;
        }

        /* Hero Section */
        .hero {
            padding: 180px 0 100px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(212, 175, 55, 0.1) 0%, transparent 70%);
            z-index: -1;
            animation: rotate 120s linear infinite;
        }

        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .hero h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3.5rem;
            margin-bottom: 1.5rem;
            line-height: 1.2;
            text-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
        }

        .hero h1 span {
            color: var(--primary);
            display: block;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { text-shadow: 0 0 5px rgba(212, 175, 55, 0.5); }
            50% { text-shadow: 0 0 20px rgba(212, 175, 55, 0.8); }
            100% { text-shadow: 0 0 5px rgba(212, 175, 55, 0.5); }
        }

        .hero p {
            font-size: 1.25rem;
            max-width: 700px;
            margin: 0 auto 2.5rem;
            color: rgba(255, 255, 255, 0.9);
        }

        .countdown {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-bottom: 3rem;
            flex-wrap: wrap;
        }

        .countdown-item {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 1.5rem;
            min-width: 100px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(212, 175, 55, 0.3);
            box-shadow: var(--glow);
            transition: var(--transition);
        }

        .countdown-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(212, 175, 55, 0.3);
        }

        .countdown-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 0.5rem;
            text-shadow: 0 0 10px rgba(212, 175, 55, 0.5);
        }

        .countdown-label {
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: rgba(255, 255, 255, 0.7);
        }

        /* Presale Section */
        .presale-section {
            background: rgba(26, 26, 46, 0.7);
            border-radius: 20px;
            padding: 3rem;
            margin: 3rem auto;
            max-width: 800px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(212, 175, 55, 0.3);
            box-shadow: var(--shadow);
            position: relative;
            overflow: hidden;
        }

        .presale-section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--primary), var(--primary-dark));
        }

        .section-title {
            text-align: center;
            margin-bottom: 2.5rem;
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
            width: 100%;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: var(--primary);
            border-radius: 3px;
        }

        .presale-box {
            background: rgba(18, 18, 18, 0.6);
            border-radius: 15px;
            padding: 2rem;
            margin-bottom: 2rem;
            border: 1px solid rgba(212, 175, 55, 0.2);
        }

        .presale-info {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1.5rem;
            margin-bottom: 1.5rem;
        }

        .info-item {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            padding: 1.2rem;
            border: 1px solid rgba(212, 175, 55, 0.1);
            transition: var(--transition);
        }

        .info-item:hover {
            transform: translateY(-3px);
            box-shadow: var(--glow);
        }

        .info-label {
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.7);
            margin-bottom: 0.5rem;
        }

        .info-value {
            font-size: 1.3rem;
            font-weight: 600;
            color: var(--primary);
        }

        .progress-container {
            margin: 2rem 0;
        }

        .progress-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.5rem;
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.7);
        }

        .progress-bar {
            height: 15px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: inset 0 1px 3px rgba(0,0,0,0.2);
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, var(--primary), var(--primary-dark));
            width: 65%;
            border-radius: 10px;
            position: relative;
        }

        .progress-fill::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            animation: shine 2s infinite;
        }

        @keyframes shine {
            0% { background-position: -200px 0; }
            100% { background-position: 200px 0; }
        }

        .buy-form {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .input-group {
            display: flex;
            flex-direction: column;
            gap: 0.5rem;
        }

        .input-group label {
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .input-row {
            display: flex;
            gap: 1rem;
        }

        .input-row input {
            flex: 1;
        }

        input {
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(212, 175, 55, 0.3);
            border-radius: 10px;
            padding: 1rem;
            font-size: 1rem;
            color: white;
            transition: var(--transition);
        }

        input:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(212, 175, 55, 0.2);
        }

        .max-btn {
            background: rgba(212, 175, 55, 0.2);
            color: var(--primary);
            border: none;
            border-radius: 10px;
            padding: 0 1.5rem;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .max-btn:hover {
            background: rgba(212, 175, 55, 0.3);
        }

        .buy-btn {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: var(--secondary);
            border: none;
            padding: 1.2rem;
            font-size: 1.1rem;
            font-weight: 600;
            border-radius: 12px;
            cursor: pointer;
            transition: var(--transition);
            box-shadow: var(--shadow);
            margin-top: 1rem;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }

        .buy-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(212, 175, 55, 0.4);
        }

        .buy-btn:active {
            transform: translateY(1px);
        }

        .transaction-status {
            margin-top: 1.5rem;
            padding: 1rem;
            border-radius: 10px;
            text-align: center;
            display: none;
        }

        .transaction-success {
            background: rgba(40, 167, 69, 0.2);
            border: 1px solid var(--success);
            color: var(--success);
        }

        .transaction-error {
            background: rgba(220, 53, 69, 0.2);
            border: 1px solid var(--danger);
            color: var(--danger);
        }

        /* Tokenomics Section */
        .tokenomics {
            padding: 5rem 0;
            position: relative;
        }

        .tokenomics::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" width="100" height="100"><circle cx="50" cy="50" r="1" fill="rgba(212, 175, 55, 0.1)"/></svg>');
            z-index: -1;
            opacity: 0.3;
        }

        .tokenomics-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .tokenomics-card {
            background: rgba(26, 26, 46, 0.7);
            border-radius: 15px;
            padding: 2rem;
            text-align: center;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(212, 175, 55, 0.3);
            transition: var(--transition);
            position: relative;
            overflow: hidden;
        }

        .tokenomics-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow);
        }

        .tokenomics-card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(212, 175, 55, 0.1) 0%, transparent 70%);
            z-index: -1;
        }

        .tokenomics-icon {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
            text-shadow: 0 0 10px rgba(212, 175, 55, 0.3);
        }

        .tokenomics-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }

        .tokenomics-card p {
            color: rgba(255, 255, 255, 0.8);
        }

        /* Token Contract Section */
        .contract-section {
            background: rgba(26, 26, 46, 0.7);
            border-radius: 20px;
            padding: 3rem;
            margin: 5rem auto;
            max-width: 800px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(212, 175, 55, 0.3);
            box-shadow: var(--shadow);
            position: relative;
            overflow: hidden;
        }
        
        .contract-section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--primary), var(--primary-dark));
        }
        
        .contract-details {
            background: rgba(18, 18, 18, 0.6);
            border-radius: 15px;
            padding: 1.5rem;
            margin-top: 1.5rem;
            border: 1px solid rgba(212, 175, 55, 0.2);
        }
        
        .contract-info {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1rem;
            margin-bottom: 1rem;
        }
        
        .contract-actions {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            margin-top: 1.5rem;
        }
        
        .action-btn {
            background: rgba(212, 175, 55, 0.2);
            color: var(--primary);
            border: 1px solid var(--primary);
            padding: 0.8rem;
            border-radius: 10px;
            cursor: pointer;
            font-weight: 600;
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }
        
        .action-btn:hover {
            background: rgba(212, 175, 55, 0.3);
            transform: translateY(-2px);
        }

        /* Footer */
        footer {
            background: rgba(18, 18, 18, 0.9);
            padding: 4rem 0 2rem;
            border-top: 1px solid rgba(212, 175, 55, 0.3);
            position: relative;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .footer-col h3 {
            font-size: 1.4rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
        }

        .footer-col h3::after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 0;
            width: 50px;
            height: 2px;
            background: var(--primary);
        }

        .footer-links {
            display: flex;
            flex-direction: column;
            gap: 0.8rem;
        }

        .footer-links a {
            color: rgba(255, 255, 255, 0.7);
            text-decoration: none;
            transition: var(--transition);
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .footer-links a:hover {
            color: var(--primary);
            padding-left: 5px;
        }

        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .social-link {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            font-size: 1.2rem;
            transition: var(--transition);
        }

        .social-link:hover {
            background: var(--primary);
            color: var(--secondary);
            transform: translateY(-5px);
            box-shadow: var(--glow);
        }

        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: rgba(255, 255, 255, 0.5);
            font-size: 0.9rem;
        }

        .back-to-top {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--primary);
            color: var(--secondary);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            box-shadow: var(--shadow);
            cursor: pointer;
            transition: var(--transition);
            z-index: 999;
            opacity: 0;
            visibility: hidden;
        }

        .back-to-top.visible {
            opacity: 1;
            visibility: visible;
        }

        .back-to-top:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(212, 175, 55, 0.4);
        }

        /* Responsive */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 3rem;
            }
            
            .presale-info, .contract-info {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero {
                padding: 150px 0 80px;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .countdown {
                gap: 1rem;
            }
            
            .countdown-item {
                min-width: 80px;
                padding: 1rem;
            }
            
            .countdown-number {
                font-size: 2rem;
            }
            
            .presale-section, .contract-section {
                padding: 2rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }

        @media (max-width: 576px) {
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .countdown {
                flex-wrap: wrap;
            }
            
            .countdown-item {
                min-width: 70px;
            }
            
            .input-row {
                flex-direction: column;
                gap: 0.5rem;
            }
            
            .logo-text {
                font-size: 1.5rem;
            }
            
            .connect-wallet-btn {
                padding: 0.6rem 1.2rem;
                font-size: 0.9rem;
            }
        }
    </style>
</head>
<body>
    <!-- Back to top button -->
    <div class="back-to-top">
        <i class="fas fa-arrow-up"></i>
    </div>

    <!-- Header -->
    <header id="header">
        <div class="container">
            <div class="header-content">
                <a href="#home" class="logo">
                    <div class="logo-icon">
                        <i class="fas fa-coins"></i>
                    </div>
                    <div class="logo-text">$GOLDR</div>
                </a>
                <nav class="nav-links">
                    <a href="#home"><i class="fas fa-home"></i> Home</a>
                    <a href="#presale"><i class="fas fa-gem"></i> Presale</a>
                    <a href="#tokenomics"><i class="fas fa-chart-pie"></i> Tokenomics</a>
                    <a href="#contract"><i class="fas fa-file-contract"></i> Token</a>
                </nav>
                <button class="connect-wallet-btn" id="connectWalletBtn">
                    <i class="fas fa-wallet"></i> Connect Wallet
                </button>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h1>Gold Reserve Token<br><span>$GOLDR</span></h1>
            <p>A revolutionary cryptocurrency backed by physical gold reserves, combining the stability of precious metals with the efficiency of blockchain technology.</p>
            
            <div class="countdown">
                <div class="countdown-item">
                    <div class="countdown-number" id="days">14</div>
                    <div class="countdown-label">Days</div>
                </div>
                <div class="countdown-item">
                    <div class="countdown-number" id="hours">08</div>
                    <div class="countdown-label">Hours</div>
                </div>
                <div class="countdown-item">
                    <div class="countdown-number" id="minutes">42</div>
                    <div class="countdown-label">Minutes</div>
                </div>
                <div class="countdown-item">
                    <div class="countdown-number" id="seconds">19</div>
                    <div class="countdown-label">Seconds</div>
                </div>
            </div>
            
            <a href="#presale" class="connect-wallet-btn" style="text-decoration: none;">
                <i class="fas fa-gem"></i> Participate in Presale
            </a>
        </div>
    </section>

    <!-- Presale Section -->
    <section class="presale-section" id="presale">
        <h2 class="section-title">Presale is Live!</h2>
        
        <div class="presale-box">
            <div class="presale-info">
                <div class="info-item">
                    <div class="info-label">Presale Progress</div>
                    <div class="info-value">65%</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Total Raised</div>
                    <div class="info-value">325 ETH</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Presale Target</div>
                    <div class="info-value">500 ETH</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Token Price</div>
                    <div class="info-value">1 ETH = 50,000 $GOLDR</div>
                </div>
            </div>
            
            <div class="progress-container">
                <div class="progress-header">
                    <span>Softcap: 250 ETH</span>
                    <span>Hardcap: 500 ETH</span>
                </div>
                <div class="progress-bar">
                    <div class="progress-fill" id="progressFill"></div>
                </div>
            </div>
            
            <form class="buy-form" id="buyForm">
                <div class="input-group">
                    <label for="eth-amount">
                        <i class="fab fa-ethereum"></i> Amount of ETH to contribute
                    </label>
                    <div class="input-row">
                        <input type="number" id="eth-amount" placeholder="0.0" min="0.01" step="0.01" max="10">
                        <button type="button" class="max-btn" id="maxBtn">MAX</button>
                    </div>
                </div>
                
                <div class="input-group">
                    <label for="goldr-amount">
                        <i class="fas fa-coins"></i> You will receive
                    </label>
                    <input type="text" id="goldr-amount" placeholder="0 $GOLDR" readonly>
                </div>
                
                <button type="button" class="buy-btn" id="buyBtn">
                    <i class="fas fa-coins"></i> Buy $GOLDR Tokens
                </button>
                
                <div class="transaction-status" id="transactionStatus">
                    <i class="fas fa-spinner fa-spin"></i> Processing transaction...
                </div>
            </form>
        </div>
        
        <div class="presale-info">
            <div class="info-item">
                <div class="info-label">Token Address (Base)</div>
                <div class="info-value">0x1234...5678</div>
            </div>
            <div class="info-item">
                <div class="info-label">Token Address (Ethereum)</div>
                <div class="info-value">0xEeee...EEeE</div>
            </div>
        </div>
    </section>

    <!-- Tokenomics Section -->
    <section class="tokenomics" id="tokenomics">
        <div class="container">
            <h2 class="section-title">Tokenomics</h2>
            
            <div class="tokenomics-grid">
                <div class="tokenomics-card">
                    <div class="tokenomics-icon">
                        <i class="fas fa-chart-pie"></i>
                    </div>
                    <h3>Token Distribution</h3>
                    <p>1 Billion tokens minted at launch with transparent allocation to presale, liquidity, team, and reserves.</p>
                </div>
                
                <div class="tokenomics-card">
                    <div class="tokenomics-icon">
                        <i class="fas fa-fire"></i>
                    </div>
                    <h3>Deflationary Model</h3>
                    <p>2% automatic token burn on every sell transaction, creating scarcity and increasing token value over time.</p>
                </div>
                
                <div class="tokenomics-card">
                    <div class="tokenomics-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3>Gold Backing</h3>
                    <p>5% of all sell transactions allocated to physical gold reserves, providing tangible asset backing.</p>
                </div>
                
                <div class="tokenomics-card">
                    <div class="tokenomics-icon">
                        <i class="fas fa-hand-holding-usd"></i>
                    </div>
                    <h3>Zero Buy Tax</h3>
                    <p>No tax on purchase transactions, making it cost-effective to acquire $GOLDR tokens.</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Token Contract Section -->
    <section class="contract-section" id="contract">
        <h2 class="section-title">Token Contract</h2>
        
        <p style="text-align: center; margin-bottom: 2rem; color: rgba(255,255,255,0.8);">
            Manage your $GOLDR tokens directly through our secure smart contract interface
        </p>
        
        <div class="contract-details">
            <div class="contract-info">
                <div class="info-item">
                    <div class="info-label">Token Name</div>
                    <div class="info-value">Gold Reserve Token</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Symbol</div>
                    <div class="info-value">$GOLDR</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Total Supply</div>
                    <div class="info-value">1,000,000,000</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Decimals</div>
                    <div class="info-value">18</div>
                </div>
            </div>
            
            <div class="contract-actions">
                <button class="action-btn" id="viewContractBtn">
                    <i class="fas fa-external-link-alt"></i> View on Basescan
                </button>
                <button class="action-btn" id="copyContractBtn">
                    <i class="fas fa-copy"></i> Copy Contract Address
                </button>
                <button class="action-btn" id="addToWalletBtn">
                    <i class="fas fa-wallet"></i> Add to Wallet
                </button>
            </div>
        </div>
        
        <div class="presale-box" style="margin-top: 2rem;">
            <h3 style="text-align: center; margin-bottom: 1.5rem; color: var(--primary);">Token Contract Functions</h3>
            
            <div class="contract-info">
                <div class="info-item">
                    <div class="info-label">Buy Tax</div>
                    <div class="info-value">0%</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Sell Tax</div>
                    <div class="info-value">7% (2% burn + 5% reserve)</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Reserve Wallet</div>
                    <div class="info-value">0xReserve...Wallet</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Liquidity Pool</div>
                    <div class="info-value">Locked for 2 years</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="footer-col">
                    <div class="logo">
                        <div class="logo-icon">
                            <i class="fas fa-coins"></i>
                        </div>
                        <div class="logo-text">$GOLDR</div>
                    </div>
                    <p style="margin-top: 1rem; color: rgba(255,255,255,0.7);">
                        Gold Reserve Token combines blockchain innovation with the timeless value of gold, creating a new standard for asset-backed cryptocurrencies.
                    </p>
                    <div class="social-links">
                        <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-telegram"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-discord"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-medium"></i></a>
                    </div>
                </div>
                
                <div class="footer-col">
                    <h3>Quick Links</h3>
                    <div class="footer-links">
                        <a href="#home"><i class="fas fa-chevron-right"></i> Home</a>
                        <a href="#presale"><i class="fas fa-chevron-right"></i> Presale</a>
                        <a href="#tokenomics"><i class="fas fa-chevron-right"></i> Tokenomics</a>
                        <a href="#contract"><i class="fas fa-chevron-right"></i> Token Contract</a>
                        <a href="#"><i class="fas fa-chevron-right"></i> Whitepaper</a>
                    </div>
                </div>
                
                <div class="footer-col">
                    <h3>Resources</h3>
                    <div class="footer-links">
                        <a href="#"><i class="fas fa-chevron-right"></i> Documentation</a>
                        <a href="#"><i class="fas fa-chevron-right"></i> GitHub Repository</a>
                        <a href="#"><i class="fas fa-chevron-right"></i> Base Network</a>
                        <a href="#"><i class="fas fa-chevron-right"></i> Etherscan</a>
                        <a href="#"><i class="fas fa-chevron-right"></i> Basescan</a>
                    </div>
                </div>
                
                <div class="footer-col">
                    <h3>Legal</h3>
                    <div class="footer-links">
                        <a href="#"><i class="fas fa-chevron-right"></i> Terms of Service</a>
                        <a href="#"><i class="fas fa-chevron-right"></i> Privacy Policy</a>
                        <a href="#"><i class="fas fa-chevron-right"></i> Disclaimer</a>
                        <a href="#"><i class="fas fa-chevron-right"></i> Risk Disclosure</a>
                    </div>
                </div>
            </div>
            
            <div class="copyright">
                &copy; 2023 Gold Reserve Token. All rights reserved. This is not an investment advice. Cryptocurrencies are volatile assets; do your own research.
            </div>
        </div>
    </footer>

    <script>
        // DOM elements
        const header = document.getElementById('header');
        const backToTopBtn = document.querySelector('.back-to-top');
        const connectWalletBtn = document.getElementById('connectWalletBtn');
        const ethInput = document.getElementById('eth-amount');
        const goldrOutput = document.getElementById('goldr-amount');
        const maxBtn = document.getElementById('maxBtn');
        const buyBtn = document.getElementById('buyBtn');
        const transactionStatus = document.getElementById('transactionStatus');
        const progressFill = document.getElementById('progressFill');
        const viewContractBtn = document.getElementById('viewContractBtn');
        const copyContractBtn = document.getElementById('copyContractBtn');
        const addToWalletBtn = document.getElementById('addToWalletBtn');
        
        // Constants
        const tokenRate = 50000; // 1 ETH = 50,000 $GOLDR
        const totalRaised = 325; // ETH
        const hardcap = 500; // ETH
        const progressPercentage = (totalRaised / hardcap) * 100;
        const tokenContractAddress = "0x1234567890abcdef1234567890abcdef12345678";
        
        // Set initial progress bar width
        progressFill.style.width = `${progressPercentage}%`;
        
        // Countdown Timer
        function updateCountdown() {
            const now = new Date();
            const presaleEnd = new Date(now);
            presaleEnd.setDate(now.getDate() + 14);
            
            const diff = presaleEnd - now;
            
            const days = Math.floor(diff / (1000 * 60 * 60 * 24));
            const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((diff % (1000 * 60)) / 1000);
            
            document.getElementById('days').textContent = days.toString().padStart(2, '0');
            document.getElementById('hours').textContent = hours.toString().padStart(2, '0');
            document.getElementById('minutes').textContent = minutes.toString().padStart(2, '0');
            document.getElementById('seconds').textContent = seconds.toString().padStart(2, '0');
        }
        
        setInterval(updateCountdown, 1000);
        updateCountdown();
        
        // ETH to GOLDR conversion
        ethInput.addEventListener('input', () => {
            const ethValue = parseFloat(ethInput.value) || 0;
            const goldrValue = ethValue * tokenRate;
            goldrOutput.value = ethValue > 0 ? goldrValue.toLocaleString() + ' $GOLDR' : '0 $GOLDR';
        });
        
        // MAX button
        maxBtn.addEventListener('click', () => {
            ethInput.value = '10';
            const goldrValue = 10 * tokenRate;
            goldrOutput.value = goldrValue.toLocaleString() + ' $GOLDR';
        });
        
        // Buy button
        buyBtn.addEventListener('click', () => {
            const ethAmount = parseFloat(ethInput.value);
            
            if (!ethAmount || ethAmount <= 0) {
                showTransactionStatus('Please enter a valid amount of ETH', 'error');
                return;
            }
            
            if (ethAmount > 10) {
                showTransactionStatus('Maximum purchase per transaction is 10 ETH', 'error');
                return;
            }
            
            showTransactionStatus('Processing transaction...', 'processing');
            
            // Simulate transaction delay
            setTimeout(() => {
                const goldrAmount = ethAmount * tokenRate;
                showTransactionStatus(
                    `Success! You've purchased ${goldrAmount.toLocaleString()} $GOLDR tokens`,
                    'success'
                );
                
                // Update progress bar
                const newRaised = totalRaised + ethAmount;
                const newPercentage = (newRaised / hardcap) * 100;
                progressFill.style.width = `${Math.min(newPercentage, 100)}%`;
                
                // Reset form after success
                setTimeout(() => {
                    ethInput.value = '';
                    goldrOutput.value = '';
                    transactionStatus.style.display = 'none';
                }, 5000);
            }, 3000);
        });
        
        // Transaction status handler
        function showTransactionStatus(message, type) {
            transactionStatus.innerHTML = message;
            transactionStatus.className = 'transaction-status';
            
            if (type === 'processing') {
                transactionStatus.innerHTML = `<i class="fas fa-spinner fa-spin"></i> ${message}`;
                transactionStatus.classList.add('transaction-processing');
            } 
            else if (type === 'success') {
                transactionStatus.innerHTML = `<i class="fas fa-check-circle"></i> ${message}`;
                transactionStatus.classList.add('transaction-success');
            } 
            else if (type === 'error') {
                transactionStatus.innerHTML = `<i class="fas fa-exclamation-circle"></i> ${message}`;
                transactionStatus.classList.add('transaction-error');
            }
            
            transactionStatus.style.display = 'block';
        }
        
        // Connect Wallet
        connectWalletBtn.addEventListener('click', () => {
            if (!connectWalletBtn.classList.contains('wallet-connected')) {
                connectWalletBtn.innerHTML = '<i class="fas fa-check"></i> Wallet Connected';
                connectWalletBtn.classList.add('wallet-connected');
                
                // Show success message
                showTransactionStatus('Wallet connected successfully!', 'success');
                setTimeout(() => {
                    transactionStatus.style.display = 'none';
                }, 3000);
            }
        });
        
        // Contract Actions
        viewContractBtn.addEventListener('click', () => {
            showTransactionStatus('Redirecting to Basescan...', 'processing');
            setTimeout(() => {
                showTransactionStatus('Please check your browser for popup blocker', 'success');
                setTimeout(() => {
                    transactionStatus.style.display = 'none';
                }, 3000);
            }, 1000);
        });
        
        copyContractBtn.addEventListener('click', () => {
            navigator.clipboard.writeText(tokenContractAddress);
            showTransactionStatus('Contract address copied to clipboard!', 'success');
            setTimeout(() => {
                transactionStatus.style.display = 'none';
            }, 3000);
        });
        
        addToWalletBtn.addEventListener('click', () => {
            showTransactionStatus('Adding $GOLDR to your wallet...', 'processing');
            setTimeout(() => {
                showTransactionStatus('Token added successfully!', 'success');
                setTimeout(() => {
                    transactionStatus.style.display = 'none';
                }, 3000);
            }, 2000);
        });
        
        // Scroll header effect
        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
            
            // Show/hide back to top button
            if (window.scrollY > 300) {
                backToTopBtn.classList.add('visible');
            } else {
                backToTopBtn.classList.remove('visible');
            }
        });
        
        // Back to top button
        backToTopBtn.addEventListener('click', () => {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                if (this.getAttribute('href') === '#') return;
                
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    window.scrollTo({
                        top: target.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Initialize form
        ethInput.value = '';
        goldrOutput.value = '';
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>$GOLDR Token Presale - Gold Reserve Token</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=Montserrat:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --gold: #D4AF37;
            --dark-gold: #B8860B;
            --deep-blue: #0A0F1F;
            --light-gold: #F5E7C1;
            --medium-gold: #E6C35C;
            --warning-red: #ff4444;
            --warning-dark: #cc0000;
            --caution-yellow: #ffcc00;
            --caution-dark: #e6b800;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            background: var(--deep-blue);
            color: white;
            overflow-x: hidden;
            background-image: radial-gradient(circle at 10% 20%, rgba(212, 175, 55, 0.1) 0%, rgba(10, 15, 31, 0) 20%),
                              radial-gradient(circle at 90% 80%, rgba(212, 175, 55, 0.1) 0%, rgba(10, 15, 31, 0) 20%);
            position: relative;
        }
        
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://i.ibb.co/0j7WwYk/404-token.gif') center/cover no-repeat;
            opacity: 0.05;
            z-index: -1;
        }
        
        /* SECURITY WARNING BANNER */
        .scam-warning {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background: linear-gradient(90deg, var(--warning-red), var(--warning-dark));
            color: white;
            padding: 15px 0;
            text-align: center;
            font-weight: 700;
            z-index: 2000;
            box-shadow: 0 4px 12px rgba(255, 0, 0, 0.3);
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .scam-warning .container {
            display: flex;
            align-items: center;
            gap: 15px;
            max-width: 1200px;
            padding: 0 20px;
        }
        
        .scam-warning i {
            font-size: 24px;
            animation: pulse 1.5s infinite;
        }
        
        .close-warning {
            background: transparent;
            border: none;
            color: white;
            font-size: 24px;
            cursor: pointer;
            margin-left: 15px;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.2); }
            100% { transform: scale(1); }
        }
        
        /* RISK INDICATORS */
        .risk-indicator {
            display: inline-flex;
            align-items: center;
            gap: 5px;
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
            margin: 0 5px;
            vertical-align: middle;
        }
        
        .high-risk {
            background: rgba(255, 68, 68, 0.3);
            border: 1px solid var(--warning-red);
        }
        
        .medium-risk {
            background: rgba(255, 204, 0, 0.3);
            border: 1px solid var(--caution-yellow);
        }
        
        .gold-text {
            color: var(--gold);
            text-shadow: 0 0 10px rgba(212, 175, 55, 0.5);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background: rgba(10, 15, 31, 0.9);
            backdrop-filter: blur(10px);
            position: fixed;
            width: 100%;
            z-index: 1000;
            border-bottom: 1px solid rgba(212, 175, 55, 0.3);
            top: 50px; /* Account for warning banner */
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .logo-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, var(--gold), var(--dark-gold));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            font-weight: bold;
            color: var(--deep-blue);
        }
        
        .logo-text {
            font-family: 'Playfair Display', serif;
            font-size: 28px;
            font-weight: 900;
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            font-size: 16px;
            text-transform: uppercase;
            letter-spacing: 1px;
            position: relative;
            transition: color 0.3s;
        }
        
        nav a:hover {
            color: var(--gold);
        }
        
        nav a::after {
            content: "";
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--gold);
            transition: width 0.3s;
        }
        
        nav a:hover::after {
            width: 100%;
        }
        
        .nav-buttons {
            display: flex;
            gap: 15px;
        }
        
        .btn {
            padding: 12px 25px;
            border-radius: 30px;
            font-weight: 600;
            text-decoration: none;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-size: 14px;
            transition: all 0.3s;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            cursor: pointer;
        }
        
        .btn-gold {
            background: linear-gradient(135deg, var(--gold), var(--dark-gold));
            color: var(--deep-blue);
            border: none;
        }
        
        .btn-gold:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(212, 175, 55, 0.3);
        }
        
        .btn-outline {
            border: 2px solid var(--gold);
            color: var(--gold);
            background: transparent;
        }
        
        .btn-outline:hover {
            background: rgba(212, 175, 55, 0.1);
        }
        
        .btn-caution {
            border: 2px solid var(--caution-yellow);
            color: var(--caution-yellow);
            background: transparent;
        }
        
        .btn-caution:hover {
            background: rgba(255, 204, 0, 0.1);
        }
        
        /* Presale Hero Section */
        .presale-hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding-top: 150px;
            position: relative;
            overflow: hidden;
            text-align: center;
        }
        
        .presale-hero::before {
            content: "";
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(212, 175, 55, 0.2) 0%, transparent 70%);
            z-index: -1;
        }
        
        .presale-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .presale-title {
            font-family: 'Playfair Display', serif;
            font-size: 70px;
            font-weight: 900;
            line-height: 1.1;
            margin-bottom: 25px;
        }
        
        .presale-subtitle {
            font-size: 24px;
            color: var(--light-gold);
            margin-bottom: 40px;
        }
        
        .presale-badge {
            background: rgba(212, 175, 55, 0.2);
            padding: 8px 20px;
            border-radius: 30px;
            display: inline-block;
            margin-bottom: 30px;
            font-weight: 600;
        }
        
        /* Countdown Timer */
        .countdown {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 40px 0;
        }
        
        .countdown-item {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .countdown-value {
            width: 100px;
            height: 100px;
            background: rgba(20, 25, 40, 0.7);
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 42px;
            font-weight: 700;
            color: var(--gold);
            margin-bottom: 10px;
            border: 2px solid var(--gold);
        }
        
        .countdown-label {
            font-size: 14px;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: var(--light-gold);
        }
        
        /* Presale Stats */
        .presale-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 50px 0;
        }
        
        .stat-card {
            background: rgba(20, 25, 40, 0.7);
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            border: 1px solid rgba(212, 175, 55, 0.1);
        }
        
        .stat-value {
            font-size: 32px;
            font-weight: 700;
            color: var(--gold);
            margin-bottom: 10px;
        }
        
        .stat-label {
            color: var(--light-gold);
            font-size: 16px;
        }
        
        .progress-container {
            margin: 30px 0;
        }
        
        .progress-labels {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
        }
        
        .progress-bar {
            height: 20px;
            background: rgba(20, 25, 40, 0.7);
            border-radius: 10px;
            overflow: hidden;
            position: relative;
        }
        
        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, var(--dark-gold), var(--gold));
            border-radius: 10px;
            width: 45%; /* Current progress */
            position: relative;
        }
        
        .progress-fill::after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            animation: shine 3s infinite;
        }
        
        /* Presale Form */
        .presale-form {
            background: rgba(20, 25, 40, 0.7);
            border-radius: 20px;
            padding: 40px;
            max-width: 500px;
            margin: 50px auto;
            border: 1px solid rgba(212, 175, 55, 0.1);
        }
        
        .form-title {
            font-size: 24px;
            margin-bottom: 25px;
            text-align: center;
            color: var(--gold);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: var(--light-gold);
        }
        
        .form-control {
            width: 100%;
            padding: 15px;
            background: rgba(10, 15, 31, 0.7);
            border: 1px solid rgba(212, 175, 55, 0.3);
            border-radius: 10px;
            color: white;
            font-size: 16px;
        }
        
        .token-preview {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: rgba(10, 15, 31, 0.7);
            padding: 15px;
            border-radius: 10px;
            margin: 20px 0;
            border: 1px solid rgba(212, 175, 55, 0.3);
        }
        
        .token-amount {
            font-size: 20px;
            font-weight: 700;
            color: var(--gold);
        }
        
        /* Security Tips */
        .security-tips {
            padding: 80px 0;
            background: rgba(10, 15, 31, 0.9);
        }
        
        .tips-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .tip-card {
            background: rgba(20, 25, 40, 0.7);
            border-radius: 20px;
            padding: 30px;
            border: 1px solid rgba(212, 175, 55, 0.1);
        }
        
        .tip-card h3 {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 15px;
            color: var(--gold);
        }
        
        /* Footer */
        footer {
            background: rgba(5, 10, 20, 0.9);
            padding: 70px 0 30px;
            border-top: 1px solid rgba(212, 175, 55, 0.1);
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 60px;
        }
        
        .footer-logo {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .footer-social {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-icon {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(212, 175, 55, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
            color: var(--gold);
            transition: all 0.3s;
        }
        
        .social-icon:hover {
            background: var(--gold);
            color: var(--deep-blue);
            transform: translateY(-3px);
        }
        
        .footer-links h3 {
            font-size: 20px;
            margin-bottom: 25px;
            color: var(--gold);
        }
        
        .footer-links ul {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 15px;
        }
        
        .footer-links a {
            color: #b0b0c0;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: var(--gold);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #707080;
            font-size: 14px;
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .presale-title {
                font-size: 50px;
            }
            
            .countdown-value {
                width: 80px;
                height: 80px;
                font-size: 32px;
            }
        }
        
        @media (max-width: 768px) {
            .scam-warning .container {
                flex-direction: column;
                gap: 10px;
            }
            
            .close-warning {
                position: absolute;
                top: 10px;
                right: 10px;
            }
            
            .header-container {
                flex-direction: column;
                gap: 20px;
            }
            
            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .countdown {
                gap: 10px;
            }
            
            .countdown-value {
                width: 70px;
                height: 70px;
                font-size: 28px;
            }
        }
    </style>
</head>
<body>
    <!-- Security Warning Banner -->
    <div class="scam-warning">
        <div class="container">
            <i class="fas fa-exclamation-triangle"></i>
            <div>
                <strong>PRESALE WARNING:</strong> High-risk investment - Unverified gold reserves - No independent audits - 
                This token exhibits multiple characteristics of potential scams. 
                <span class="risk-indicator high-risk">HIGH RISK</span>
            </div>
            <button class="close-warning">&times;</button>
        </div>
    </div>

    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <div class="logo-icon">GR</div>
                <div class="logo-text gold-text">GOLD RESERVE</div>
            </div>
            <nav>
                <ul>
                    <li><a href="#about">About</a></li>
                    <li><a href="#tokenomics">Tokenomics</a></li>
                    <li><a href="#presale" class="gold-text">Presale</a></li>
                    <li><a href="#roadmap">Roadmap</a></li>
                    <li><a href="#security">Security</a></li>
                </ul>
            </nav>
            <div class="nav-buttons">
                <a href="#" class="btn btn-caution"><i class="fas fa-exclamation-circle"></i> High Risk</a>
                <a href="#" class="btn btn-outline">Whitepaper</a>
            </div>
        </div>
    </header>

    <!-- Presale Hero Section -->
    <section class="presale-hero" id="presale">
        <div class="container">
            <div class="presale-content">
                <div class="presale-badge">
                    <i class="fas fa-coins"></i> PRESALE LIVE
                </div>
                <h1 class="presale-title">$GOLDR Token Presale</h1>
                <p class="presale-subtitle">Participate in the exclusive presale of Gold Reserve Token - Digital Gold Reinvented <span class="risk-indicator high-risk">HIGH RISK</span></p>
                
                <!-- Countdown Timer -->
                <div class="countdown">
                    <div class="countdown-item">
                        <div class="countdown-value" id="days">12</div>
                        <div class="countdown-label">Days</div>
                    </div>
                    <div class="countdown-item">
                        <div class="countdown-value" id="hours">08</div>
                        <div class="countdown-label">Hours</div>
                    </div>
                    <div class="countdown-item">
                        <div class="countdown-value" id="minutes">45</div>
                        <div class="countdown-label">Minutes</div>
                    </div>
                    <div class="countdown-item">
                        <div class="countdown-value" id="seconds">30</div>
                        <div class="countdown-label">Seconds</div>
                    </div>
                </div>
                
                <!-- Presale Stats -->
                <div class="presale-stats">
                    <div class="stat-card">
                        <div class="stat-value">$1,250,000</div>
                        <div class="stat-label">Raised</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-value">$2,500,000</div>
                        <div class="stat-label">Soft Cap</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-value">$5,000,000</div>
                        <div class="stat-label">Hard Cap</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-value">1 $GOLDR = $0.05</div>
                        <div class="stat-label">Presale Price</div>
                    </div>
                </div>
                
                <!-- Progress Bar -->
                <div class="progress-container">
                    <div class="progress-labels">
                        <span>0%</span>
                        <span>45%</span>
                        <span>100%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill"></div>
                    </div>
                </div>
                
                <!-- Presale Form -->
                <div class="presale-form">
                    <h3 class="form-title">Contribute to Presale <span class="risk-indicator high-risk">HIGH RISK</span></h3>
                    
                    <div class="form-group">
                        <label for="amount">Enter ETH Amount</label>
                        <input type="number" id="amount" class="form-control" placeholder="0.00" min="0.1" step="0.01">
                    </div>
                    
                    <div class="token-preview">
                        <div>You will receive:</div>
                        <div class="token-amount">0 $GOLDR</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="wallet">Your Wallet Address</label>
                        <input type="text" id="wallet" class="form-control" placeholder="0x...">
                    </div>
                    
                    <button class="btn btn-gold" style="width: 100%;">
                        <i class="fas fa-lock"></i> Connect Wallet to Contribute
                    </button>
                    
                    <p style="text-align: center; margin-top: 20px; font-size: 12px; color: var(--warning-red);">
                        <i class="fas fa-exclamation-circle"></i> Warning: This presale has not been audited. Funds may be lost.
                    </p>
                </div>
                
                <div class="hero-buttons">
                    <a href="#" class="btn btn-outline"><i class="fas fa-file-contract"></i> View Smart Contract</a>
                    <a href="#" class="btn btn-outline"><i class="fas fa-file-alt"></i> Presale Terms</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Security Tips Section -->
    <section class="security-tips" id="security">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title gold-text">Presale Security Recommendations <i class="fas fa-shield-alt"></i></h2>
                <p class="section-subtitle">Essential precautions for participating in token presales</p>
            </div>
            <div class="tips-grid">
                <div class="tip-card">
                    <h3><i class="fas fa-search"></i> Verify Everything</h3>
                    <p>Always verify the smart contract on blockchain explorers. Check for renounced ownership, audits, and liquidity locks. This presale contract is unverified.</p>
                </div>
                <div class="tip-card">
                    <h3><i class="fas fa-file-invoice"></i> Audit Requirement</h3>
                    <p>Require proof of security audits from reputable firms like CertiK or Hacken. Be extremely skeptical of unaudited projects.</p>
                </div>
                <div class="tip-card">
                    <h3><i class="fas fa-exclamation-triangle"></i> Recognize Red Flags</h3>
                    <p>High promised returns, anonymous teams, and pressure to invest quickly are common scam indicators in presales.</p>
                </div>
                <div class="tip-card">
                    <h3><i class="fas fa-money-bill-wave"></i> Invest Responsibly</h3>
                    <p>Never invest more than you can afford to lose. Presales are extremely high-risk investments with potential for total loss.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Tokenomics Section -->
    <section class="tokenomics" id="tokenomics">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title gold-text">Presale Token Distribution <span class="risk-indicator high-risk">HIGH SELL TAX</span></h2>
                <p class="section-subtitle">How presale funds will be allocated</p>
            </div>
            <div cla

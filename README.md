<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gold Reserve Token ($GOLDR) - Digital Gold Reinvented</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=Montserrat:wght@300;400;600;700&display=swap" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        :root {
            --gold: #D4AF37;
            --dark-gold: #B8860B;
            --deep-blue: #0A0F1F;
            --light-gold: #F5E7C1;
            --medium-gold: #E6C35C;
            --rich-black: #050A14;
            --presale-highlight: #ffd700;
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
            background-image: 
                radial-gradient(circle at 10% 20%, rgba(212, 175, 55, 0.1) 0%, rgba(10, 15, 31, 0) 20%),
                radial-gradient(circle at 90% 80%, rgba(212, 175, 55, 0.1) 0%, rgba(10, 15, 31, 0) 20%);
            position: relative;
            line-height: 1.6;
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
        
        .gold-text {
            color: var(--gold);
            text-shadow: 0 0 10px rgba(212, 175, 55, 0.5);
        }
        
        .presale-highlight {
            color: var(--presale-highlight);
            text-shadow: 0 0 15px rgba(255, 215, 0, 0.7);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background: rgba(10, 15, 31, 0.95);
            backdrop-filter: blur(10px);
            position: fixed;
            width: 100%;
            z-index: 1000;
            border-bottom: 1px solid rgba(212, 175, 55, 0.3);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            transition: all 0.3s ease;
        }
        
        header.scrolled {
            padding: 5px 0;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
            transition: padding 0.3s ease;
        }
        
        .header-container.scrolled {
            padding: 10px 0;
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
            box-shadow: 0 0 15px rgba(212, 175, 55, 0.5);
        }
        
        .logo-text {
            font-family: 'Playfair Display', serif;
            font-size: 28px;
            font-weight: 900;
            letter-spacing: 1px;
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
            border: none;
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
        
        .btn-presale {
            background: linear-gradient(135deg, var(--presale-highlight), #daa520);
            color: var(--rich-black);
            font-weight: 700;
            box-shadow: 0 0 20px rgba(255, 215, 0, 0.4);
            animation: pulse 2s infinite;
        }
        
        .btn-presale:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(255, 215, 0, 0.5), 0 0 30px rgba(255, 215, 0, 0.4);
        }
        
        @keyframes pulse {
            0% { box-shadow: 0 0 15px rgba(255, 215, 0, 0.4); }
            50% { box-shadow: 0 0 25px rgba(255, 215, 0, 0.6); }
            100% { box-shadow: 0 0 15px rgba(255, 215, 0, 0.4); }
        }
        
        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding-top: 100px;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
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
        
        .hero-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        
        .hero-text {
            flex: 1;
        }
        
        .hero-image {
            flex: 1;
            display: flex;
            justify-content: center;
            position: relative;
        }
        
        .gold-bar {
            width: 300px;
            height: 150px;
            background: linear-gradient(135deg, var(--gold), var(--dark-gold));
            border-radius: 10px;
            position: relative;
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.5);
            transform: rotate(-10deg);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            transition: transform 0.5s ease;
        }
        
        .gold-bar:hover {
            transform: rotate(-8deg) scale(1.05);
        }
        
        .gold-bar::before {
            content: "";
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            animation: shine 3s infinite;
        }
        
        @keyframes shine {
            0% { left: -100%; }
            100% { left: 100%; }
        }
        
        .gold-bar-text {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
            font-size: 24px;
            color: var(--deep-blue);
            text-align: center;
            z-index: 1;
            text-shadow: 0 1px 1px rgba(0, 0, 0, 0.2);
        }
        
        .gold-bar-small {
            position: absolute;
            width: 120px;
            height: 60px;
            background: linear-gradient(135deg, var(--medium-gold), var(--dark-gold));
            border-radius: 6px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
            transition: all 0.5s ease;
        }
        
        .gold-bar-small:hover {
            transform: scale(1.1);
        }
        
        .gold-bar-1 {
            top: -30px;
            left: 50px;
            transform: rotate(15deg);
        }
        
        .gold-bar-2 {
            bottom: -30px;
            right: 50px;
            transform: rotate(-15deg);
        }
        
        .tagline {
            font-size: 18px;
            color: var(--light-gold);
            margin-bottom: 20px;
            text-transform: uppercase;
            letter-spacing: 3px;
        }
        
        h1 {
            font-family: 'Playfair Display', serif;
            font-size: 70px;
            font-weight: 900;
            line-height: 1.1;
            margin-bottom: 25px;
        }
        
        .hero p {
            font-size: 18px;
            line-height: 1.7;
            margin-bottom: 40px;
            max-width: 600px;
            color: #c0c0d0;
        }
        
        .hero-buttons {
            display: flex;
            gap: 20px;
            margin-top: 30px;
            flex-wrap: wrap;
        }
        
        .contract-address {
            background: rgba(212, 175, 55, 0.1);
            padding: 15px 25px;
            border-radius: 30px;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            margin-top: 20px;
            font-family: monospace;
            font-size: 16px;
            border: 1px solid rgba(212, 175, 55, 0.3);
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .contract-address:hover {
            background: rgba(212, 175, 55, 0.2);
            transform: translateY(-2px);
        }
        
        .contract-address i {
            color: var(--gold);
        }
        
        /* Presale Section */
        .presale {
            padding: 120px 0;
            position: relative;
            background: linear-gradient(135deg, rgba(10, 15, 31, 0.9), rgba(20, 15, 5, 0.9));
            overflow: hidden;
        }
        
        .presale::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://i.ibb.co/0j7WwYk/404-token.gif') center/cover no-repeat;
            opacity: 0.1;
            z-index: 0;
        }
        
        .presale-container {
            position: relative;
            z-index: 1;
        }
        
        .section-header {
            text-align: center;
            margin-bottom: 70px;
        }
        
        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: 48px;
            font-weight: 700;
            margin-bottom: 20px;
            position: relative;
            display: inline-block;
        }
        
        .section-title::after {
            content: "";
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: var(--gold);
        }
        
        .section-subtitle {
            font-size: 20px;
            color: var(--light-gold);
            max-width: 700px;
            margin: 30px auto 0;
            line-height: 1.6;
        }
        
        .presale-content {
            display: flex;
            gap: 40px;
            align-items: center;
        }
        
        .presale-countdown {
            flex: 1;
            background: rgba(20, 25, 40, 0.7);
            border-radius: 20px;
            padding: 40px;
            text-align: center;
            border: 1px solid rgba(212, 175, 55, 0.3);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        .presale-timer {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 30px 0;
        }
        
        .timer-unit {
            background: rgba(212, 175, 55, 0.1);
            border-radius: 15px;
            padding: 20px;
            min-width: 100px;
            text-align: center;
            border: 1px solid rgba(212, 175, 55, 0.2);
        }
        
        .timer-value {
            font-size: 42px;
            font-weight: 700;
            color: var(--presale-highlight);
            margin-bottom: 5px;
            text-shadow: 0 0 10px rgba(255, 215, 0, 0.5);
        }
        
        .timer-label {
            color: var(--light-gold);
            font-size: 16px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .presale-progress {
            background: rgba(10, 15, 31, 0.8);
            border-radius: 30px;
            height: 20px;
            overflow: hidden;
            margin: 30px 0;
            border: 1px solid rgba(212, 175, 55, 0.2);
        }
        
        .progress-bar {
            height: 100%;
            background: linear-gradient(90deg, var(--dark-gold), var(--presale-highlight));
            width: 42%;
            border-radius: 30px;
            position: relative;
            transition: width 1s ease;
        }
        
        .progress-bar::after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            animation: shine 3s infinite;
        }
        
        .progress-info {
            display: flex;
            justify-content: space-between;
            margin-top: 15px;
            font-size: 16px;
        }
        
        .progress-raised {
            color: var(--presale-highlight);
            font-weight: 600;
        }
        
        .presale-form {
            flex: 1;
            background: rgba(20, 25, 40, 0.7);
            border-radius: 20px;
            padding: 40px;
            border: 1px solid rgba(212, 175, 55, 0.3);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        .presale-form h3 {
            font-size: 28px;
            margin-bottom: 30px;
            color: var(--presale-highlight);
            text-align: center;
        }
        
        .input-group {
            margin-bottom: 25px;
        }
        
        .input-group label {
            display: block;
            margin-bottom: 10px;
            font-weight: 600;
            color: var(--light-gold);
        }
        
        .input-control {
            width: 100%;
            padding: 15px 20px;
            background: rgba(10, 15, 31, 0.8);
            border: 1px solid rgba(212, 175, 55, 0.3);
            border-radius: 10px;
            color: white;
            font-size: 16px;
            transition: all 0.3s;
        }
        
        .input-control:focus {
            outline: none;
            border-color: var(--presale-highlight);
            box-shadow: 0 0 10px rgba(255, 215, 0, 0.3);
        }
        
        .token-info {
            background: rgba(212, 175, 55, 0.1);
            padding: 20px;
            border-radius: 10px;
            margin: 25px 0;
            text-align: center;
            font-size: 18px;
        }
        
        .token-amount {
            color: var(--presale-highlight);
            font-weight: 700;
            font-size: 24px;
            margin-top: 10px;
        }
        
        .presale-details {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-top: 40px;
        }
        
        .detail-card {
            background: rgba(10, 15, 31, 0.5);
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            border: 1px solid rgba(212, 175, 55, 0.2);
        }
        
        .detail-card h4 {
            color: var(--light-gold);
            margin-bottom: 10px;
            font-size: 16px;
        }
        
        .detail-card p {
            font-size: 20px;
            font-weight: 700;
            color: var(--presale-highlight);
        }
        
        .presale-notes {
            margin-top: 30px;
            padding: 20px;
            background: rgba(212, 175, 55, 0.1);
            border-radius: 15px;
            border-left: 4px solid var(--presale-highlight);
        }
        
        .presale-notes ul {
            padding-left: 20px;
            margin-top: 15px;
        }
        
        .presale-notes li {
            margin-bottom: 10px;
            color: var(--light-gold);
        }
        
        .presale-notes li::marker {
            color: var(--presale-highlight);
        }
        
        /* Features Section */
        .features {
            padding: 120px 0;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .feature-card {
            background: rgba(20, 25, 40, 0.7);
            border-radius: 20px;
            padding: 40px 30px;
            text-align: center;
            transition: all 0.3s;
            border: 1px solid rgba(212, 175, 55, 0.1);
            backdrop-filter: blur(10px);
            position: relative;
            overflow: hidden;
        }
        
        .feature-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--gold), var(--dark-gold));
            transform: scaleX(0);
            transform-origin: left;
            transition: transform 0.3s ease;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            border-color: rgba(212, 175, 55, 0.3);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }
        
        .feature-card:hover::before {
            transform: scaleX(1);
        }
        
        .feature-icon {
            width: 80px;
            height: 80px;
            background: rgba(212, 175, 55, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 25px;
            font-size: 30px;
            color: var(--gold);
            transition: all 0.3s ease;
        }
        
        .feature-card:hover .feature-icon {
            background: rgba(212, 175, 55, 0.2);
            transform: scale(1.1);
        }
        
        .feature-title {
            font-size: 24px;
            margin-bottom: 15px;
            font-weight: 700;
            transition: color 0.3s;
        }
        
        .feature-card:hover .feature-title {
            color: var(--gold);
        }
        
        .feature-description {
            color: #b0b0c0;
            line-height: 1.7;
        }
        
        /* Tokenomics Section */
        .tokenomics {
            padding: 120px 0;
            background: rgba(10, 15, 25, 0.7);
        }
        
        .tokenomics-content {
            display: flex;
            gap: 50px;
            align-items: center;
        }
        
        .tokenomics-chart {
            flex: 1;
            display: flex;
            justify-content: center;
        }
        
        .chart-container {
            width: 350px;
            height: 350px;
            position: relative;
        }
        
        .chart-center {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
        }
        
        .chart-center-value {
            font-size: 36px;
            font-weight: 700;
            color: var(--gold);
            margin-bottom: 5px;
        }
        
        .chart-center-label {
            color: var(--light-gold);
            font-size: 18px;
        }
        
        .tokenomics-details {
            flex: 1;
        }
        
        .tokenomics-list {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin-top: 40px;
        }
        
        .tokenomics-item {
            display: flex;
            gap: 15px;
            background: rgba(20, 25, 40, 0.5);
            padding: 20px;
            border-radius: 15px;
            border: 1px solid rgba(212, 175, 55, 0.1);
            transition: all 0.3s ease;
        }
        
        .tokenomics-item:hover {
            background: rgba(20, 25, 40, 0.7);
            border-color: rgba(212, 175, 55, 0.3);
            transform: translateY(-5px);
        }
        
        .tokenomics-icon {
            min-width: 50px;
            height: 50px;
            background: rgba(212, 175, 55, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
            color: var(--gold);
        }
        
        .tokenomics-info h4 {
            font-size: 20px;
            margin-bottom: 8px;
        }
        
        .tokenomics-info p {
            color: #b0b0c0;
        }
        
        /* Gold Reserves Section */
        .reserves {
            padding: 120px 0;
            background: linear-gradient(to bottom, var(--rich-black), var(--deep-blue));
            position: relative;
            overflow: hidden;
        }
        
        .reserves::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://i.ibb.co/GxW1qXc/gold-pattern.png');
            opacity: 0.05;
            z-index: 0;
        }
        
        .reserves-container {
            position: relative;
            z-index: 1;
        }
        
        .reserves-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .reserve-card {
            background: rgba(20, 25, 40, 0.7);
            border-radius: 20px;
            padding: 30px;
            text-align: center;
            border: 1px solid rgba(212, 175, 55, 0.1);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .reserve-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, transparent, rgba(212, 175, 55, 0.05));
            opacity: 0;
            transition: opacity 0.3s;
        }
        
        .reserve-card:hover::before {
            opacity: 1;
        }
        
        .reserve-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
            border-color: rgba(212, 175, 55, 0.3);
        }
        
        .reserve-icon {
            font-size: 50px;
            color: var(--gold);
            margin-bottom: 20px;
        }
        
        .reserve-title {
            font-size: 24px;
            margin-bottom: 15px;
            color: var(--gold);
        }
        
        .reserve-value {
            font-size: 32px;
            font-weight: 700;
            margin: 20px 0;
            background: linear-gradient(to right, var(--gold), var(--light-gold));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }
        
        .reserve-location {
            color: #b0b0c0;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }
        
        .audit-status {
            display: inline-block;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 14px;
            font-weight: 600;
            margin-top: 15px;
        }
        
        .audit-verified {
            background: rgba(0, 200, 83, 0.1);
            color: #00C853;
            border: 1px solid rgba(0, 200, 83, 0.3);
        }
        
        /* Roadmap Section */
        .roadmap {
            padding: 120px 0;
        }
        
        .roadmap-steps {
            position: relative;
            max-width: 800px;
            margin: 60px auto 0;
        }
        
        .roadmap-line {
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 4px;
            height: 100%;
            background: linear-gradient(to bottom, var(--gold), transparent);
        }
        
        .roadmap-step {
            display: flex;
            margin-bottom: 80px;
            position: relative;
        }
        
        .roadmap-step:nth-child(odd) {
            flex-direction: row-reverse;
            text-align: right;
        }
        
        .step-content {
            flex: 1;
            padding: 30px;
            background: rgba(20, 25, 40, 0.7);
            border-radius: 20px;
            border: 1px solid rgba(212, 175, 55, 0.1);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }
        
        .step-content:hover {
            border-color: rgba(212, 175, 55, 0.3);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            transform: translateY(-5px);
        }
        
        .step-content h3 {
            font-size: 24px;
            margin-bottom: 15px;
            color: var(--gold);
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .step-content h3 i {
            font-size: 20px;
        }
        
        .step-content ul {
            padding-left: 20px;
            margin-top: 15px;
            color: #b0b0c0;
        }
        
        .step-content li {
            margin-bottom: 10px;
            line-height: 1.6;
            position: relative;
        }
        
        .step-content li::before {
            content: "•";
            color: var(--gold);
            font-weight: bold;
            display: inline-block;
            width: 1em;
            margin-left: -1em;
        }
        
        .step-marker {
            width: 30px;
            height: 30px;
            background: var(--gold);
            border-radius: 50%;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 2;
            box-shadow: 0 0 0 10px rgba(212, 175, 55, 0.2);
            transition: all 0.3s ease;
        }
        
        .roadmap-step:hover .step-marker {
            transform: translate(-50%, -50%) scale(1.2);
            box-shadow: 0 0 0 15px rgba(212, 175, 55, 0.3);
        }
        
        /* CTA Section */
        .cta {
            padding: 100px 0;
            text-align: center;
            background: linear-gradient(135deg, rgba(212, 175, 55, 0.1), rgba(10, 15, 31, 0.8));
            position: relative;
        }
        
        .cta::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://i.ibb.co/0j7WwYk/404-token.gif') center/cover no-repeat;
            opacity: 0.05;
            z-index: 0;
        }
        
        .cta-content {
            position: relative;
            z-index: 1;
        }
        
        .cta h2 {
            font-family: 'Playfair Display', serif;
            font-size: 48px;
            margin-bottom: 20px;
        }
        
        .cta p {
            font-size: 20px;
            max-width: 700px;
            margin: 0 auto 40px;
            color: var(--light-gold);
        }
        
        /* Footer */
        footer {
            background: rgba(5, 10, 20, 0.95);
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
            position: relative;
            display: inline-block;
        }
        
        .footer-links h3::after {
            content: "";
            position: absolute;
            bottom: -8px;
            left: 0;
            width: 40px;
            height: 2px;
            background: var(--gold);
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
            display: inline-block;
        }
        
        .footer-links a:hover {
            color: var(--gold);
            transform: translateX(5px);
        }
        
        .footer-links a i {
            margin-right: 8px;
            font-size: 14px;
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
            h1 {
                font-size: 50px;
            }
            
            .hero-content {
                flex-direction: column;
                text-align: center;
            }
            
            .hero p {
                margin: 0 auto 40px;
            }
            
            .hero-buttons {
                justify-content: center;
            }
            
            .presale-content {
                flex-direction: column;
            }
            
            .tokenomics-content {
                flex-direction: column;
            }
            
            .tokenomics-list {
                grid-template-columns: 1fr;
            }
        }
        
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                gap: 20px;
            }
            
            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .roadmap-step,
            .roadmap-step:nth-child(odd) {
                flex-direction: column;
                text-align: left;
            }
            
            .step-marker {
                left: 0;
                transform: translate(-50%, -50%);
            }
            
            .step-content {
                margin-left: 40px;
            }
            
            .hero-image {
                margin-top: 50px;
            }
            
            .presale-details {
                grid-template-columns: 1fr;
            }
            
            .timer-unit {
                min-width: 70px;
                padding: 15px;
            }
            
            .timer-value {
                font-size: 32px;
            }
        }
        
        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .animate {
            animation: fadeInUp 0.8s ease forwards;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header id="header">
        <div class="container header-container">
            <div class="logo">
                <div class="logo-icon">GR</div>
                <div class="logo-text gold-text">GOLD RESERVE</div>
            </div>
            <nav>
                <ul>
                    <li><a href="#about">About</a></li>
                    <li><a href="#presale">Presale</a></li>
                    <li><a href="#features">Features</a></li>
                    <li><a href="#tokenomics">Tokenomics</a></li>
                    <li><a href="#roadmap">Roadmap</a></li>
                    <li><a href="#reserves">Gold Reserves</a></li>
                </ul>
            </nav>
            <div class="nav-buttons">
                <a href="#presale" class="btn btn-presale">Join Presale</a>
                <a href="#" class="btn btn-outline">Whitepaper</a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <div class="tagline">The Future of Digital Gold</div>
                    <h1>Exposing Fiat Gold Manipulation with <span class="gold-text">Blockchain</span></h1>
                    <p>$GOLDR combines the stability of physical gold with the innovation of cryptocurrency. Each token is backed by verifiable gold reserves stored in audited vaults worldwide.</p>
                    <div class="hero-buttons">
                        <a href="#presale" class="btn btn-presale"><i class="fas fa-coins"></i> Join Presale</a>
                        <a href="#" class="btn btn-outline"><i class="fas fa-chart-line"></i> View Chart</a>
                    </div>
                    <div class="contract-address" id="contractAddress">
                        <i class="fas fa-wallet"></i> Contract: 0x7272cE8C293af0da82b3Cb590a11fd099E2d7b14
                    </div>
                </div>
                <div class="hero-image">
                    <div class="gold-bar">
                        <div class="gold-bar-text">GOLD RESERVE</div>
                        <div class="gold-bar-text">1 $GOLDR = 1 GRAM GOLD</div>
                    </div>
                    <div class="gold-bar-small gold-bar-1"></div>
                    <div class="gold-bar-small gold-bar-2"></div>
                </div>
            </div>
        </div>
    </section>

    <!-- Presale Section -->
    <section class="presale" id="presale">
        <div class="container presale-container">
            <div class="section-header">
                <h2 class="section-title presale-highlight">$GOLDR Presale</h2>
                <p class="section-subtitle">Get in early on the token that's revolutionizing gold ownership with exclusive presale benefits</p>
            </div>
            
            <div class="presale-content">
                <div class="presale-countdown">
                    <h3>Presale Ends In</h3>
                    <div class="presale-timer">
                        <div class="timer-unit">
                            <div class="timer-value" id="days">07</div>
                            <div class="timer-label">Days</div>
                        </div>
                        <div class="timer-unit">
                            <div class="timer-value" id="hours">15</div>
                            <div class="timer-label">Hours</div>
                        </div>
                        <div class="timer-unit">
                            <div class="timer-value" id="minutes">42</div>
                            <div class="timer-label">Minutes</div>
                        </div>
                        <div class="timer-unit">
                            <div class="timer-value" id="seconds">30</div>
                            <div class="timer-label">Seconds</div>
                        </div>
                    </div>
                    
                    <div class="presale-progress">
                        <div class="progress-bar" id="progressBar"></div>
                    </div>
                    
                    <div class="progress-info">
                        <div class="progress-raised">1,260,000 USDT Raised</div>
                        <div>Hard Cap: 3,000,000 USDT</div>
                    </div>
                    
                    <div class="presale-notes">
                        <h4>Presale Benefits:</h4>
                        <ul>
                            <li>30% bonus tokens for presale participants</li>
                            <li>Guaranteed gold reserve backing from day one</li>
                            <li>Exclusive access to Gold Market Prediction Game</li>
                            <li>Priority physical redemption rights</li>
                        </ul>
                    </div>
                </div>
                
                <div class="presale-form">
                    <h3>Buy $GOLDR Tokens</h3>
                    
                    <div class="input-group">
                        <label for="usdtAmount">Enter USDT Amount</label>
                        <input type="number" id="usdtAmount" class="input-control" placeholder="1000" min="100" value="1000">
                    </div>
                    
                    <div class="token-info">
                        <div>You will receive:</div>
                        <div class="token-amount" id="tokenAmount">13,000 $GOLDR</div>
                        <div>(1 USDT = 10 $GOLDR + 30% bonus)</div>
                    </div>
                    
                    <button class="btn btn-presale" style="width: 100%; padding: 18px;">
                        <i class="fas fa-wallet"></i> Connect Wallet to Buy
                    </button>
                    
                    <div class="presale-details">
                        <div class="detail-card">
                            <h4>Presale Price</h4>
                            <p>1 USDT = 10 $GOLDR</p>
                        </div>
                        <div class="detail-card">
                            <h4>Listing Price</h4>
                            <p>1 USDT = 7.7 $GOLDR</p>
                        </div>
                        <div class="detail-card">
                            <h4>Minimum Buy</h4>
                            <p>100 USDT</p>
                        </div>
                        <div class="detail-card">
                            <h4>Maximum Buy</h4>
                            <p>50,000 USDT</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features" id="features">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title gold-text">Revolutionary Features</h2>
                <p class="section-subtitle">$GOLDR is designed to disrupt traditional gold markets while providing unprecedented transparency and security.</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3 class="feature-title">Physical Gold Backing</h3>
                    <p class="feature-description">Each $GOLDR token represents 1 gram of physical gold stored in high-security vaults with regular audits.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-globe"></i>
                    </div>
                    <h3 class="feature-title">Global Redemption</h3>
                    <p class="feature-description">Redeem your tokens for physical gold bars at any of our partner vault locations worldwide.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-eye"></i>
                    </div>
                    <h3 class="feature-title">Transparent Reserves</h3>
                    <p class="feature-description">Real-time dashboard showing all gold reserves, serial numbers, and audit reports on-chain.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-gamepad"></i>
                    </div>
                    <h3 class="feature-title">Gold Market Game</h3>
                    <p class="feature-description">Predict COMEX gold prices and win $GOLDR airdrops in our interactive trading game.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-fire"></i>
                    </div>
                    <h3 class="feature-title">Burn Mechanism</h3>
                    <p class="feature-description">5% of transaction fees buy and burn physical gold, creating permanent scarcity.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-gavel"></i>
                    </div>
                    <h3 class="feature-title">Legal Action Fund</h3>
                    <p class="feature-description">2% of fees fund lawsuits against gold market manipulators and demand audits.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Tokenomics Section -->
    <section class="tokenomics" id="tokenomics">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title gold-text">Tokenomics</h2>
                <p class="section-subtitle">Sustainable economic model designed for long-term value appreciation</p>
            </div>
            <div class="tokenomics-content">
                <div class="tokenomics-chart">
                    <div class="chart-container">
                        <canvas id="tokenomicsChart" width="350" height="350"></canvas>
                        <div class="chart-center">
                            <div class="chart-center-value">1B</div>
                            <div class="chart-center-label">Total Supply</div>
                        </div>
                    </div>
                </div>
                <div class="tokenomics-details">
                    <p>$GOLDR implements a sophisticated token economy that balances growth incentives with gold reserve accumulation. Our tax structure fuels both the treasury and the burn mechanism.</p>
                    <div class="tokenomics-list">
                        <div class="tokenomics-item">
                            <div class="tokenomics-icon">
                                <i class="fas fa-coins"></i>
                            </div>
                            <div class="tokenomics-info">
                                <h4>Total Supply</h4>
                                <p>1,000,000,000 $GOLDR</p>
                            </div>
                        </div>
                        <div class="tokenomics-item">
                            <div class="tokenomics-icon">
                                <i class="fas fa-percentage"></i>
                            </div>
                            <div class="tokenomics-info">
                                <h4>Buy Tax</h4>
                                <p>0% - maximize entry</p>
                            </div>
                        </div>
                        <div class="tokenomics-item">
                            <div class="tokenomics-icon">
                                <i class="fas fa-fire-alt"></i>
                            </div>
                            <div class="tokenomics-info">
                                <h4>Sell Tax</h4>
                                <p>7% (5% gold reserve, 2% burn)</p>
                            </div>
                        </div>
                        <div class="tokenomics-item">
                            <div class="tokenomics-icon">
                                <i class="fas fa-lock"></i>
                            </div>
                            <div class="tokenomics-info">
                                <h4>Liquidity Lock</h4>
                                <p>20 years (Fort Knox lock)</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Gold Reserves Section -->
    <section class="reserves" id="reserves">
        <div class="container reserves-container">
            <div class="section-header">
                <h2 class="section-title gold-text">Gold Reserves</h2>
                <p class="section-subtitle">Our verified physical gold holdings secured in top-tier vaults worldwide</p>
            </div>
            <div class="reserves-grid">
                <div class="reserve-card">
                    <div class="reserve-icon">
                        <i class="fas fa-vault"></i>
                    </div>
                    <h3 class="reserve-title">Swiss Vault</h3>
                    <div class="reserve-location">
                        <i class="fas fa-map-marker-alt"></i> Zurich, Switzerland
                    </div>
                    <div class="reserve-value">12,542 KG</div>
                    <div class="audit-status audit-verified">
                        <i class="fas fa-check-circle"></i> Audit Verified
                    </div>
                </div>
                
                <div class="reserve-card">
                    <div class="reserve-icon">
                        <i class="fas fa-landmark"></i>
                    </div>
                    <h3 class="reserve-title">Singapore Reserve</h3>
                    <div class="reserve-location">
                        <i class="fas fa-map-marker-alt"></i> Singapore
                    </div>
                    <div class="reserve-value">8,765 KG</div>
                    <div class="audit-status audit-verified">
                        <i class="fas fa-check-circle"></i> Audit Verified
                    </div>
                </div>
                
                <div class="reserve-card">
                    <div class="reserve-icon">
                        <i class="fas fa-university"></i>
                    </div>
                    <h3 class="reserve-title">London Depository</h3>
                    <div class="reserve-location">
                        <i class="fas fa-map-marker-alt"></i> London, UK
                    </div>
                    <div class="reserve-value">15,320 KG</div>
                    <div class="audit-status audit-verified">
                        <i class="fas fa-check-circle"></i> Audit Verified
                    </div>
                </div>
            </div>
            
            <div class="reserve-total" style="text-align: center; margin-top: 50px;">
                <div style="font-size: 20px; color: var(--light-gold);">Total Gold Reserves</div>
                <div style="font-size: 48px; font-weight: 700; margin: 10px 0 20px; background: linear-gradient(to right, var(--gold), var(--light-gold)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; text-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);">36,627 KG</div>
                <p style="max-width: 700px; margin: 0 auto; color: #b0b0c0;">All reserves are independently audited quarterly with serial numbers and vault certificates available on-chain</p>
            </div>
        </div>
    </section>

    <!-- Roadmap Section -->
    <section class="roadmap" id="roadmap">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title gold-text">Strategic Roadmap</h2>
                <p class="section-subtitle">Our phased approach to revolutionizing the gold market</p>
            </div>
            <div class="roadmap-steps">
                <div class="roadmap-line"></div>
                
                <div class="roadmap-step">
                    <div class="step-content">
                        <h3><i class="fas fa-layer-group"></i> Phase 1: Foundation (Q3 2025)</h3>
                        <ul>
                            <li>Token deployment on Base L2</li>
                            <li>First 100kg gold purchase & vault storage</li>
                            <li>Gold reserve dashboard launch</li>
                            <li>Community airdrop to gold bug communities</li>
                        </ul>
                    </div>
                    <div class="step-marker"></div>
                </div>
                
                <div class="roadmap-step">
                    <div class="step-content">
                        <h3><i class="fas fa-expand-arrows-alt"></i> Phase 2: Expansion (Q4 2025)</h3>
                        <ul>
                            <li>CEX listings (3 exchanges)</li>
                            <li>Physical redemption at 5 global locations</li>
                            <li>Gold Market Prediction Game launch</li>
                            <li>Strategic lawsuit against COMEX</li>
                        </ul>
                    </div>
                    <div class="step-marker"></div>
                </div>
                
                <div class="roadmap-step">
                    <div class="step-content">
                        <h3><i class="fas fa-crown"></i> Phase 3: Dominance (Q1 2026)</h3>
                        <ul>
                            <li>10,000kg gold reserves milestone</li>
                            <li>Gold-backed NFT collection launch</li>
                            <li>Partnership with major gold refiners</li>
                            <li>Global marketing campaign launch</li>
                        </ul>
                    </div>
                    <div class="step-marker"></div>
                </div>
                
                <div class="roadmap-step">
                    <div class="step-content">
                        <h3><i class="fas fa-recycle"></i> Phase 4: Revolution (Q2 2026)</h3>
                        <ul>
                            <li>Gold Reserve debit card launch</li>
                            <li>Tokenize national gold reserves</li>
                            <li>Become top 100 cryptocurrency</li>
                            <li>Complete decentralization of protocol</li>
                        </ul>
                    </div>
                    <div class="step-marker"></div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="cta" id="cta">
        <div class="container">
            <div class="cta-content">
                <h2>Join the Gold Revolution</h2>
                <p>Be part of the movement that's exposing gold market manipulation while creating real, asset-backed wealth.</p>
                <div class="hero-buttons">
                    <a href="#presale" class="btn btn-presale"><i class="fas fa-coins"></i> Join Presale</a>
                    <a href="#" class="btn btn-outline"><i class="fas fa-vault"></i> View Gold Reserves</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-logo">
                    <div class="logo">
                        <div class="logo-icon">GR</div>
                        <div class="logo-text gold-text">GOLD RESERVE</div>
                    </div>
                    <p>The token that exposes fiat gold manipulation while backing itself with REAL physical gold reserves.</p>
                    <div class="footer-social">
                        <a href="#" class="social-icon"><i class="fab fa-twitter"></i></a>
                        <a href="#" class="social-icon"><i class="fab fa-telegram"></i></a>
                        <a href="#" class="social-icon"><i class="fab fa-discord"></i></a>
                        <a href="#" class="social-icon"><i class="fab fa-medium"></i></a>
                    </div>
                </div>
                
                <div class="footer-links">
                    <h3>Resources</h3>
                    <ul>
                        <li><a href="#"><i class="fas fa-file-alt"></i> Whitepaper</a></li>
                        <li><a href="#"><i class="fas fa-search-dollar"></i> Audit Reports</a></li>
                        <li><a href="#"><i class="fas fa-vault"></i> Gold Reserves</a></li>
                        <li><a href="#"><i class="fas fa-question-circle"></i> FAQ</a></li>
                        <li><a href="#"><i class="fab fa-github"></i> GitHub</a></li>
                    </ul>
                </div>
                
                <div class="footer-links">
                    <h3>Ecosystem</h3>
                    <ul>
                        <li><a href="#presale"><i class="fas fa-shopping-cart"></i> Presale</a></li>
                        <li><a href="#"><i class="fas fa-lock"></i> Staking</a></li>
                        <li><a href="#"><i class="fas fa-gamepad"></i> Gold Game</a></li>
                        <li><a href="#"><i class="fas fa-coins"></i> NFT Collection</a></li>
                        <li><a href="#"><i class="fas fa-exchange-alt"></i> Redemption</a></li>
                    </ul>
                </div>
                
                <div class="footer-links">
                    <h3>Legal</h3>
                    <ul>
                        <li><a href="#"><i class="fas fa-exclamation-triangle"></i> Disclaimer</a></li>
                        <li><a href="#"><i class="fas fa-file-contract"></i> Terms of Service</a></li>
                        <li><a href="#"><i class="fas fa-user-shield"></i> Privacy Policy</a></li>
                        <li><a href="#"><i class="fas fa-balance-scale"></i> Compliance</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                &copy; 2025 Gold Reserve Token. All rights reserved. $GOLDR is a decentralized digital asset. Not an investment product.
            </div>
        </div>
    </footer>

    <script>
        // Tokenomics Chart
        document.addEventListener('DOMContentLoaded', function() {
            const ctx = document.getElementById('tokenomicsChart').getContext('2d');
            const tokenomicsChart = new Chart(ctx, {
                type: 'doughnut',
                data: {
                    labels: ['Gold Reserve', 'Liquidity', 'Marketing', 'Team', 'Burned'],
                    datasets: [{
                        data: [50, 30, 10, 5, 5],
                        backgroundColor: [
                            '#D4AF37',
                            '#B8860B',
                            '#E6C35C',
                            '#F5E7C1',
                            '#0A0F1F'
                        ],
                        borderWidth: 0
                    }]
                },
                options: {
                    cutout: '70%',
                    plugins: {
                        legend: {
                            position: 'bottom',
                            labels: {
                                color: '#fff',
                                font: {
                                    size: 14,
                                    family: "'Montserrat', sans-serif"
                                },
                                padding: 20
                            }
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return `${context.label}: ${context.parsed}%`;
                                }
                            }
                        }
                    }
                }
            });

            // Copy contract address
            document.getElementById('contractAddress').addEventListener('click', function() {
                const text = '0x7272cE8C293af0da82b3Cb590a11fd099E2d7b14';
                navigator.clipboard.writeText(text).then(() => {
                    const original = this.innerHTML;
                    this.innerHTML = '<i class="fas fa-check"></i> Copied to clipboard!';
                    setTimeout(() => {
                        this.innerHTML = original;
                    }, 2000);
                });
            });

            // Scroll animation for elements
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('animate');
                    }
                });
            }, {
                threshold: 0.1
            });
            
            document.querySelectorAll('.feature-card, .roadmap-step, .reserve-card, .tokenomics-item').forEach(card => {
                observer.observe(card);
            });

            // Header scroll effect
            const header = document.getElementById('header');
            const headerContainer = document.querySelector('.header-container');
            
            window.addEventListener('scroll', () => {
                if (window.scrollY > 50) {
                    header.classList.add('scrolled');
                    headerContainer.classList.add('scrolled');
                } else {
                    header.classList.remove('scrolled');
                    headerContainer.classList.remove('scrolled');
                }
            });
            
            // Presale functionality
            // Countdown timer
            const countdownDate = new Date();
            countdownDate.setDate(countdownDate.getDate() + 7); // 7 days from now
            
            function updateCountdown() {
                const now = new Date().getTime();
                const distance = countdownDate - now;
                
                const days = Math.floor(distance / (1000 * 60 * 60 * 24));
                const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
                const seconds = Math.floor((distance % (1000 * 60)) / 1000);
                
                document.getElementById('days').innerText = days.toString().padStart(2, '0');
                document.getElementById('hours').innerText = hours.toString().padStart(2, '0');
                document.getElementById('minutes').innerText = minutes.toString().padStart(2, '0');
                document.getElementById('seconds').innerText = seconds.toString().padStart(2, '0');
                
                if (distance < 0) {
                    clearInterval(countdownInterval);
                    document.querySelector('.presale-countdown h3').innerText = 'Presale Has Ended!';
                    document.querySelector('.presale-timer').innerHTML = '<div class="timer-value" style="font-size: 36px; margin: 20px 0;">Presale Completed</div>';
                }
            }
            
            const countdownInterval = setInterval(updateCountdown, 1000);
            updateCountdown();
            
            // Token amount calculation
            const usdtInput = document.getElementById('usdtAmount');
            const tokenAmount = document.getElementById('tokenAmount');
            
            usdtInput.addEventListener('input', function() {
                const usdtValue = parseFloat(this.value) || 0;
                // Presale rate: 1 USDT = 10 $GOLDR with 30% bonus
                const tokens = usdtValue * 10 * 1.3;
                tokenAmount.innerText = tokens.toLocaleString('en-US', {maximumFractionDigits: 0}) + ' $GOLDR';
            });
            
            // Progress bar animation
            const progressBar = document.getElementById('progressBar');
            setTimeout(() => {
                progressBar.style.width = '42%';
            }, 500);
        });
    </script>
</body>
</html>

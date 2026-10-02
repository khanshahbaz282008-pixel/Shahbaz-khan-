<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>M. Shahbaz Khan | Graphic Designer & Web Lister</title>

    <!-- Google Font -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">

    <style>

        /* =====================================================
           ROOT
        ===================================================== */

        :root {
            --red: #ff1744;
            --red-light: #ff3d5c;
            --red-dark: #c4002f;

            --black: #050505;
            --black-2: #0a0a0a;
            --black-3: #111111;

            --white: #ffffff;
            --gray: #a7a7a7;
            --gray-2: #707070;

            --glass: rgba(255, 255, 255, 0.045);
            --glass-border: rgba(255, 255, 255, 0.10);

            --shadow:
                0 20px 70px rgba(0, 0, 0, 0.55);

            --red-glow:
                0 0 40px rgba(255, 23, 68, 0.20);
        }


        /* =====================================================
           RESET
        ===================================================== */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: "Inter", sans-serif;
            background:
                radial-gradient(
                    circle at 80% 10%,
                    rgba(255, 23, 68, 0.12),
                    transparent 30%
                ),
                radial-gradient(
                    circle at 10% 70%,
                    rgba(255, 23, 68, 0.07),
                    transparent 30%
                ),
                var(--black);

            color: var(--white);
            overflow-x: hidden;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        ::selection {
            background: var(--red);
            color: white;
        }


        /* =====================================================
           CUSTOM SCROLLBAR
        ===================================================== */

        ::-webkit-scrollbar {
            width: 7px;
        }

        ::-webkit-scrollbar-track {
            background: #050505;
        }

        ::-webkit-scrollbar-thumb {
            background: var(--red);
            border-radius: 20px;
        }


        /* =====================================================
           BACKGROUND EFFECT
        ===================================================== */

        .bg-grid {
            position: fixed;
            inset: 0;
            z-index: -5;
            pointer-events: none;

            background-image:
                linear-gradient(
                    rgba(255,255,255,0.025) 1px,
                    transparent 1px
                ),
                linear-gradient(
                    90deg,
                    rgba(255,255,255,0.025) 1px,
                    transparent 1px
                );

            background-size: 70px 70px;

            mask-image: linear-gradient(
                to bottom,
                black,
                transparent 90%
            );
        }

        .glow {
            position: fixed;
            width: 400px;
            height: 400px;

            background: rgba(255, 23, 68, 0.08);
            filter: blur(100px);
            border-radius: 50%;

            pointer-events: none;
            z-index: -4;

            animation: floatingGlow 8s ease-in-out infinite;
        }

        .glow.one {
            top: 5%;
            right: -150px;
        }

        .glow.two {
            bottom: 10%;
            left: -180px;
            animation-delay: -4s;
        }

        @keyframes floatingGlow {
            0%,100% {
                transform: translateY(0);
            }

            50% {
                transform: translateY(50px);
            }
        }


        /* =====================================================
           NAVBAR
        ===================================================== */

        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;

            z-index: 1000;

            padding: 18px 6%;
        }

        nav {
            max-width: 1200px;
            margin: auto;

            display: flex;
            align-items: center;
            justify-content: space-between;

            padding: 13px 18px;

            background: rgba(10,10,10,0.70);
            border: 1px solid var(--glass-border);

            border-radius: 18px;

            backdrop-filter: blur(18px);
            -webkit-backdrop-filter: blur(18px);

            box-shadow: var(--shadow);
        }

        .logo {
            font-size: 20px;
            font-weight: 900;
            letter-spacing: -1px;
        }

        .logo span {
            color: var(--red);
        }

        .nav-links {
            display: flex;
            gap: 28px;
            list-style: none;
        }

        .nav-links a {
            color: #aaa;
            font-size: 13px;
            font-weight: 600;
            transition: 0.3s;
        }

        .nav-links a:hover {
            color: var(--red);
        }

        .nav-button {
            padding: 10px 16px;

            border-radius: 10px;

            background: var(--red);
            color: white;

            font-size: 12px;
            font-weight: 700;

            transition: 0.3s;
        }

        .nav-button:hover {
            transform: translateY(-2px);
            box-shadow: var(--red-glow);
        }


        /* =====================================================
           GENERAL
        ===================================================== */

        section {
            width: min(1180px, 90%);
            margin: auto;
            padding: 110px 0;
        }

        .section-label {
            color: var(--red);
            font-size: 12px;
            font-weight: 800;
            letter-spacing: 4px;
            margin-bottom: 12px;
        }

        .section-title {
            font-size: clamp(35px, 5vw, 60px);
            line-height: 1;
            letter-spacing: -3px;
            margin-bottom: 50px;
        }

        .section-title span {
            color: var(--red);
        }


        /* =====================================================
           HERO
        ===================================================== */

        .hero {
            min-height: 100vh;

            display: flex;
            align-items: center;

            padding-top: 150px;
        }

        .hero-grid {
            display: grid;
            grid-template-columns: 1.25fr 0.75fr;
            gap: 70px;
            align-items: center;
        }

        .hero-small {
            color: var(--red);
            font-size: 13px;
            font-weight: 800;
            letter-spacing: 4px;
            margin-bottom: 20px;
        }

        .hero h1 {
            font-size: clamp(55px, 9vw, 110px);
            line-height: 0.88;
            letter-spacing: -7px;
            margin-bottom: 28px;
        }

        .hero h1 span {
            color: var(--red);
        }

        .typing {
            font-size: clamp(18px, 2vw, 25px);
            font-weight: 500;
            color: #d0d0d0;
            min-height: 35px;
        }

        .cursor {
            color: var(--red);
            animation: blink 0.8s infinite;
        }

        @keyframes blink {
            50% {
                opacity: 0;
            }
        }

        .hero-text {
            max-width: 650px;
            color: var(--gray);
            line-height: 1.8;
            margin: 25px 0 32px;
        }

        .hero-buttons {
            display: flex;
            gap: 14px;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;

            padding: 14px 22px;

            border-radius: 12px;

            font-size: 13px;
            font-weight: 800;

            transition: 0.35s;
        }

        .btn-red {
            background: var(--red);
            color: white;
        }

        .btn-red:hover {
            transform: translateY(-4px);
            box-shadow: 0 15px 35px rgba(255,23,68,0.25);
        }

        .btn-outline {
            border: 1px solid rgba(255,255,255,0.15);
            background: rgba(255,255,255,0.03);
            color: white;
        }

        .btn-outline:hover {
            border-color: var(--red);
            color: var(--red);
        }


        /* =====================================================
           HERO GLASS CARD
        ===================================================== */

        .hero-card {
            position: relative;

            min-height: 390px;

            display: flex;
            align-items: center;
            justify-content: center;

            background:
                linear-gradient(
                    145deg,
                    rgba(255,255,255,0.07),
                    rgba(255,255,255,0.015)
                );

            border: 1px solid var(--glass-border);

            border-radius: 30px;

            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);

            box-shadow: var(--shadow);

            overflow: hidden;

            transform-style: preserve-3d;

            transition: transform 0.15s ease;
        }

        .hero-card::before {
            content: "";

            position: absolute;

            width: 240px;
            height: 240px;

            border-radius: 50%;

            background: var(--red);

            filter: blur(90px);

            opacity: 0.18;
        }

        .profile-circle {
            position: relative;

            width: 230px;
            height: 230px;

            border-radius: 50%;

            border: 2px solid var(--red);

            display: flex;
            align-items: center;
            justify-content: center;

            box-shadow:
                0 0 0 12px rgba(255,23,68,0.04),
                0 0 70px rgba(255,23,68,0.20);
        }

        .profile-initial {
            font-size: 80px;
            font-weight: 900;
            color: var(--red);
        }

        .card-corner {
            position: absolute;
            width: 70px;
            height: 70px;
            border: 1px solid var(--red);
        }

        .corner-one {
            top: 20px;
            left: 20px;
            border-right: none;
            border-bottom: none;
        }

        .corner-two {
            right: 20px;
            bottom: 20px;
            border-left: none;
            border-top: none;
        }


        /* =====================================================
           ABOUT
        ===================================================== */

        .about-grid {
            display: grid;
            grid-template-columns: 0.8fr 1.2fr;
            gap: 35px;
        }

        .glass-card {
            background: var(--glass);

            border: 1px solid var(--glass-border);

            border-radius: 22px;

            padding: 32px;

            backdrop-filter: blur(15px);
            -webkit-backdrop-filter: blur(15px);

            box-shadow: var(--shadow);

            transition: 0.4s;
        }

        .glass-card:hover {
            transform: translateY(-7px);
            border-color: rgba(255,23,68,0.35);
        }

        .about-card h3 {
            font-size: 25px;
            margin-bottom: 18px;
        }

        .about-card p {
            color: var(--gray);
            line-height: 1.9;
        }


        /* =====================================================
           EXPERIENCE
        ===================================================== */

        .timeline {
            position: relative;
            margin-top: 30px;
        }

        .timeline::before {
            content: "";

            position: absolute;

            left: 10px;
            top: 0;
            bottom: 0;

            width: 1px;

            background:
                linear-gradient(
                    var(--red),
                    rgba(255,23,68,0.05)
                );
        }

        .experience-item {
            position: relative;
            padding-left: 55px;
            margin-bottom: 45px;
        }

        .timeline-dot {
            position: absolute;

            left: 3px;
            top: 6px;

            width: 15px;
            height: 15px;

            border-radius: 50%;

            background: var(--red);

            box-shadow:
                0 0 0 5px rgba(255,23,68,0.12),
                0 0 25px rgba(255,23,68,0.4);
        }

        .experience-card {
            padding: 30px;

            background:
                linear-gradient(
                    135deg,
                    rgba(255,255,255,0.055),
                    rgba(255,255,255,0.015)
                );

            border: 1px solid var(--glass-border);

            border-radius: 20px;

            transition: 0.4s;
        }

        .experience-card:hover {
            transform: translateX(8px);
            border-color: rgba(255,23,68,0.4);
        }

        .experience-card h3 {
            font-size: 24px;
            margin-bottom: 8px;
        }

        .company {
            color: var(--red);
            font-size: 14px;
            font-weight: 700;
            margin-bottom: 18px;
        }

        .experience-card ul {
            padding-left: 18px;
            color: var(--gray);
        }

        .experience-card li {
            margin-bottom: 10px;
            line-height: 1.6;
        }


        /* =====================================================
           SKILLS
        ===================================================== */

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 18px;
        }

        .skill {
            padding: 22px;

            background: var(--glass);
            border: 1px solid var(--glass-border);

            border-radius: 18px;

            transition: 0.35s;
        }

        .skill:hover {
            transform: translateY(-5px);
            border-color: rgba(255,23,68,0.45);
        }

        .skill-top {
            display: flex;
            align-items: center;
            justify-content: space-between;

            margin-bottom: 13px;
        }

        .skill-name {
            font-weight: 700;
        }

        .skill-percent {
            color: var(--red);
            font-size: 12px;
            font-weight: 800;
        }

        .bar {
            height: 6px;

            background: #242424;

            border-radius: 10px;

            overflow: hidden;
        }

        .bar span {
            display: block;

            height: 100%;

            background:
                linear-gradient(
                    90deg,
                    var(--red-dark),
                    var(--red-light)
                );

            width: 0;

            border-radius: 10px;

            transition: width 1.5s ease;
        }


        /* =====================================================
           ADDITIONAL SKILLS
        ===================================================== */

        .additional {
            margin-top: 30px;

            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .tag {
            padding: 10px 14px;

            border: 1px solid rgba(255,255,255,0.12);

            background: rgba(255,255,255,0.035);

            border-radius: 10px;

            color: #ccc;

            font-size: 12px;

            transition: 0.3s;
        }

        .tag:hover {
            border-color: var(--red);
            color: var(--red);
            transform: translateY(-3px);
        }


        /* =====================================================
           EDUCATION
        ===================================================== */

        .education-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }

        .education-card {
            min-height: 230px;

            position: relative;

            overflow: hidden;
        }

        .education-card::after {
            content: "";

            position: absolute;

            width: 100px;
            height: 100px;

            right: -30px;
            bottom: -30px;

            background: var(--red);

            opacity: 0.07;

            border-radius: 50%;
        }

        .education-year {
            color: var(--red);
            font-size: 12px;
            font-weight: 800;
            letter-spacing: 2px;
            margin-bottom: 20px;
        }

        .education-card h3 {
            font-size: 23px;
            margin-bottom: 8px;
        }

        .education-card p {
            color: var(--gray);
            line-height: 1.7;
        }


        /* =====================================================
           GRAPHIC DESIGNER / COMPUTER SKILLS
        ===================================================== */

        .two-columns {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }

        .info-list {
            list-style: none;
        }

        .info-list li {
            position: relative;

            padding: 13px 0 13px 24px;

            color: var(--gray);

            border-bottom: 1px solid rgba(255,255,255,0.07);
        }

        .info-list li::before {
            content: "";

            position: absolute;

            left: 0;
            top: 20px;

            width: 7px;
            height: 7px;

            border-radius: 50%;

            background: var(--red);
        }


        /* =====================================================
           CONTACT
        ===================================================== */

        .contact-wrapper {
            display: grid;
            grid-template-columns: 0.8fr 1.2fr;
            gap: 25px;
        }

        .contact-item {
            display: flex;
            gap: 15px;
            align-items: flex-start;

            padding: 20px 0;

            border-bottom: 1px solid rgba(255,255,255,0.07);
        }

        .contact-icon {
            width: 42px;
            height: 42px;

            display: flex;
            align-items: center;
            justify-content: center;

            border-radius: 12px;

            background: rgba(255,23,68,0.10);
            color: var(--red);

            font-weight: 900;
        }

        .contact-item small {
            display: block;
            color: var(--gray-2);
            margin-bottom: 5px;
        }

        .contact-item strong {
            font-size: 14px;
        }


        /* =====================================================
           REFERENCES
        ===================================================== */

        .reference-box {
            text-align: center;
            padding: 35px;

            border: 1px solid rgba(255,23,68,0.20);

            border-radius: 20px;

            background:
                linear-gradient(
                    135deg,
                    rgba(255,23,68,0.08),
                    rgba(255,255,255,0.02)
                );
        }

        .reference-box h3 {
            margin-bottom: 10px;
        }

        .reference-box p {
            color: var

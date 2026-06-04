
<!DOCTYPE html>
<html lang="ms">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="E-Buku Panduan Lengkap Trading Gold (XAU/USD). Belajar baca candlestick, Support & Resistance, dan rahsia Setup Entry.">
    <meta name="keywords" content="trading gold, xauusd, candlestick, forex malaysia, support resistance, belajar trading, ebook gold">
    <meta name="author" content="Master Class Gold">
    
    <!-- Open Graph / Facebook -->
    <meta property="og:type" content="website">
    <meta property="og:title" content="Kuasai Pasaran Gold (XAU/USD) - E-Buku Percuma">
    <meta property="og:description" content="Kuasai seni membaca candlestick, fahami rahsia Support & Resistance sebenar, dan intip jejak langkah jerung pasaran melalui E-Buku premium ini.">
    
    <title>Kuasai Pasaran Gold (XAU/USD) - E-Buku Percuma</title>
    
    <style>
        /* ==========================================================================
           1. CSS VARIABLES & SYSTEM PREFERENCES
           ========================================================================== */
        :root {
            /* Color Palette */
            --bg-dark: #0f172a;       /* Slate 900 - Latar Belakang Utama */
            --bg-card: #1e293b;       /* Slate 800 - Latar Belakang Kad/Seksyen */
            --bg-light: #f8fafc;      /* Slate 50  - Teks/Elemen Terang */
            
            --primary: #d4af37;       /* Metallic Gold - Warna Tema */
            --primary-glow: rgba(212, 175, 55, 0.4);
            
            --text-light: #f8fafc;
            --text-muted: #94a3b8;    /* Slate 400 - Teks Kurang Menonjol */
            
            --bullish: #10b981;       /* Emerald 500 - Sinyal Naik */
            --bearish: #ef4444;       /* Red 500 - Sinyal Turun */
            
            --border-subtle: rgba(255, 255, 255, 0.05);
            
            /* Typography */
            --font-main: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            
            /* Spacing */
            --section-pad: 80px 0;
            --container-max: 1200px;
        }

        /* Smooth Scrolling (Penting untuk Navigasi Halaman) */
        html { scroll-behavior: smooth; }

        /* Reset & Base Styles */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { 
            font-family: var(--font-main); 
            background-color: var(--bg-dark); 
            color: var(--text-light); 
            line-height: 1.6; 
            overflow-x: hidden; /* Elak scroll mendatar (horizontal) */
        }

        /* ==========================================================================
           2. REUSABLE UTILITIES (Vanilla CSS)
           ========================================================================== */
        .container { 
            max-width: var(--container-max); 
            margin: 0 auto; 
            padding: 0 20px; 
            width: 100%;
        }
        .text-gold { color: var(--primary); }
        .text-center { text-align: center; }
        .section-padding { padding: var(--section-pad); }
        
        /* Typography Scale */
        h1 { font-size: clamp(2.5rem, 5vw, 4rem); line-height: 1.1; margin-bottom: 20px; font-weight: 800; }
        h2 { font-size: clamp(2rem, 4vw, 2.8rem); line-height: 1.2; margin-bottom: 15px; font-weight: 700; }
        h3 { font-size: 1.5rem; margin-bottom: 15px; color: white; }
        p { font-size: 1.1rem; color: var(--text-muted); margin-bottom: 20px; }

        /* Butang (Buttons) */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 15px 35px;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 700;
            text-decoration: none;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            cursor: pointer;
            border: none;
            text-align: center;
        }
        .btn-gold {
            background: linear-gradient(135deg, #fcd34d 0%, #d4af37 100%);
            color: #0f172a;
            box-shadow: 0 4px 15px var(--primary-glow);
        }
        .btn-gold:hover { 
            transform: translateY(-3px); 
            box-shadow: 0 8px 25px var(--primary-glow); 
            background: linear-gradient(135deg, #fde68a 0%, #eab308 100%);
        }
        .btn-outline {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
        }
        .btn-outline:hover { 
            background: rgba(212, 175, 55, 0.1); 
        }

        /* Lencana (Badges) */
        .badge-group { display: flex; gap: 15px; margin-bottom: 30px; flex-wrap: wrap; }
        .badge { 
            background: rgba(212, 175, 55, 0.1); 
            border: 1px solid var(--primary); 
            color: var(--primary); 
            padding: 6px 16px; 
            border-radius: 20px; 
            font-size: 0.85rem; 
            font-weight: bold; 
            letter-spacing: 0.5px;
        }

        /* ==========================================================================
           3. KOMPONEN UTAMA LAMAN WEB
           ========================================================================== */

        /* --- Navigasi (Navbar) --- */
        nav {
            padding: 20px 0;
            background: rgba(15, 23, 42, 0.95);
            backdrop-filter: blur(12px); /* Efek kaca (Glassmorphism) */
            -webkit-backdrop-filter: blur(12px);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid var(--border-subtle);
            transition: all 0.3s ease;
        }
        nav.scrolled {
            padding: 15px 0; /* Mengecil apabila di-scroll */
            box-shadow: 0 4px 20px rgba(0,0,0,0.3);
        }
        .nav-container { display: flex; justify-content: space-between; align-items: center; }
        .logo { font-size: 1.6rem; font-weight: 800; letter-spacing: 1px; color: white; display: flex; align-items: center; gap: 5px; }
        
        /* Pautan Menu */
        .nav-links { display: flex; gap: 35px; }
        .nav-links a { 
            color: var(--text-light); 
            text-decoration: none; 
            font-weight: 500; 
            font-size: 1rem;
            transition: color 0.3s ease;
            position: relative;
        }
        .nav-links a:hover, .nav-links a.active { color: var(--primary); }
        /* Garis bawah animasi untuk menu aktif */
        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background-color: var(--primary);
            transition: width 0.3s ease;
        }
        .nav-links a:hover::after, .nav-links a.active::after { width: 100%; }

        /* --- Bahagian Hero (Atas) --- */
        .hero {
            padding-top: 160px;
            padding-bottom: 120px;
            background: radial-gradient(circle at 70% 30%, #1e293b 0%, #0f172a 70%);
            position: relative;
            min-height: 90vh;
            display: flex;
            align-items: center;
        }
        .hero-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }
        .hero-text p { font-size: 1.25rem; max-width: 90%; }
        .hero-buttons { display: flex; gap: 20px; flex-wrap: wrap; margin-top: 30px; }

        /* Efek 3D Mockup Buku (CSS Tulen) */
        .book-mockup-wrapper {
            perspective: 1200px; /* Kedalaman 3D */
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .book-3d {
            position: relative;
            width: 320px;
            height: 450px;
            transform-style: preserve-3d;
            transform: rotateY(-20deg) rotateX(5deg);
            transition: transform 0.6s cubic-bezier(0.2, 0.8, 0.2, 1);
            cursor: pointer;
        }
        .book-3d:hover {
            transform: rotateY(-5deg) rotateX(0deg) scale(1.02); /* Animasi apabila hover */
        }
        
        /* Kulit Depan Buku */
        .book-front {
            position: absolute;
            width: 100%;
            height: 100%;
            background: linear-gradient(145deg, #1e293b 0%, #0f172a 100%);
            border: 2px solid var(--primary);
            border-radius: 4px 16px 16px 4px;
            padding: 40px 30px;
            text-align: center;
            box-shadow: inset 4px 0 10px rgba(0,0,0,0.6), 15px 15px 40px rgba(0,0,0,0.5);
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            z-index: 2;
        }
        /* Kesan Lipatan Buku */
        .book-front::before {
            content: ''; position: absolute; top: 0; left: 15px; bottom: 0; width: 3px; background: rgba(255,255,255,0.08); box-shadow: 1px 0 2px rgba(0,0,0,0.5);
        }
        
        /* Tulang Tepi Buku (Spine) */
        .book-spine {
            position: absolute;
            width: 50px;
            height: calc(100% - 4px); /* Sesuaikan dengan border */
            top: 2px;
            background: linear-gradient(90deg, #b69121 0%, #d4af37 50%, #b69121 100%);
            transform: rotateY(-90deg) translateZ(25px); /* Kedudukan 3D */
            left: -25px;
            border-radius: 4px 0 0 4px;
            box-shadow: inset -2px 0 8px rgba(0,0,0,0.4);
            z-index: 1;
        }
        
        /* Isi Kandungan Kulit */
        .book-title-sub { color: var(--primary); letter-spacing: 3px; font-size: 0.9rem; font-weight: bold; text-transform: uppercase; margin-bottom: 20px;}
        .book-title-main { font-size: 2.2rem; line-height: 1.15; color: white; text-shadow: 0 4px 10px rgba(0,0,0,0.5); margin-bottom: 20px;}
        .book-divider { width: 60px; height: 3px; background: var(--primary); margin: 0 auto; box-shadow: 0 0 10px var(--primary-glow); }
        .book-author { font-size: 0.85rem; color: #cbd5e1; margin-top: 20px;}

        /* --- Bahagian Masalah (Pain Points) --- */
        .pain-points { background-color: var(--bg-card); border-top: 1px solid var(--border-subtle); border-bottom: 1px solid var(--border-subtle); }
        .grid-3 { display: grid; grid-template-columns: repeat(3, 1fr); gap: 30px; margin-top: 60px; }
        .feature-card { 
            background: rgba(15,23,42,0.4); 
            padding: 40px 30px; 
            border-radius: 16px; 
            border: 1px solid var(--border-subtle); 
            text-align: center; 
            transition: all 0.3s ease; 
        }
        .feature-card:hover { 
            border-color: var(--primary); 
            transform: translateY(-8px); 
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            background: rgba(15,23,42,0.7);
        }
        .card-icon { 
            font-size: 3rem; 
            margin-bottom: 25px; 
            display: inline-block;
            background: rgba(255,255,255,0.05);
            padding: 20px;
            border-radius: 50%;
        }

        /* --- Bahagian Isi Kandungan (Chapters) --- */
        .chapters { background-color: var(--bg-dark); }
        .chapter-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 25px; margin-top: 50px; }
        .chapter-item { 
            display: flex; 
            align-items: flex-start; 
            gap: 25px; 
            padding: 30px; 
            background: var(--bg-card); 
            border-radius: 12px; 
            border-left: 5px solid var(--primary);
            transition: transform 0.2s ease;
        }
        .chapter-item:hover { transform: translateX(5px); }
        .chapter-num { font-size: 3rem; font-weight: 900; color: rgba(212, 175, 55, 0.15); line-height: 1; }
        .chapter-text h4 { font-size: 1.2rem; color: white; margin-bottom: 10px; }
        .chapter-text p { font-size: 0.95rem; margin-bottom: 0; }

        /* --- Bahagian Previu Visual --- */
        .sneak-peek { background-color: var(--bg-card); overflow: hidden; border-top: 1px solid var(--border-subtle); }
        .demo-chart-wrapper {
            background: #131722; /* TradingView Dark Theme */
            padding: 50px 30px; 
            border-radius: 16px; 
            border: 1px solid #2a2e39; 
            display: flex; 
            justify-content: space-around; 
            align-items: flex-end; 
            height: 300px; 
            margin-top: 50px; 
            position: relative;
            box-shadow: inset 0 0 50px rgba(0,0,0,0.5);
        }
        /* Support Line Simulation */
        .demo-chart-wrapper::before { 
            content: 'ZON SOKONGAN (AREA BUY)'; 
            position: absolute; 
            bottom: 30px; 
            left: 30px; 
            color: var(--bullish); 
            font-weight: 700; 
            font-size: 0.8rem;
            letter-spacing: 1px;
            border-top: 2px dashed rgba(16, 185, 129, 0.6); 
            width: calc(100% - 60px); 
            padding-top: 8px; 
        }
        
        /* Mini Candlestick Simulation */
        .mc-wrapper { position: relative; width: 24px; height: 100%; display: flex; justify-content: center; z-index: 2; }
        .mc-wick { position: absolute; width: 3px; background: #787b86; border-radius: 2px;}
        .mc-body { position: absolute; width: 18px; border-radius: 3px; }
        .mc-bull { background: var(--bullish); }
        .mc-bear { background: var(--bearish); }
        
        /* Sorotan Corak Hammer */
        .highlight-pattern {
            position: absolute;
            bottom: 10px; /* Menutupi kawasan ekor bawah dan badan */
            left: 50%;
            transform: translateX(-50%);
            width: 40px;
            height: 120px;
            border: 2px solid var(--primary);
            border-radius: 8px;
            background: rgba(212, 175, 55, 0.1);
            animation: pulse 2s infinite;
            z-index: 1;
        }
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(212, 175, 55, 0.4); }
            70% { box-shadow: 0 0 0 15px rgba(212, 175, 55, 0); }
            100% { box-shadow: 0 0 0 0 rgba(212, 175, 55, 0); }
        }

        /* --- Bahagian Seruan Bertindak (Call to Action) --- */
        .cta-section { 
            text-align: center; 
            background: radial-gradient(circle at 50% 100%, rgba(212, 175, 55, 0.15) 0%, #0f172a 70%); 
            border-top: 1px solid rgba(212, 175, 55, 0.2); 
            padding: 100px 0;
        }
        .cta-content { max-width: 700px; margin: 0 auto; }
        
        /* Footer */
        footer { 
            padding: 40px 0; 
            text-align: center; 
            background-color: var(--bg-dark);
            border-top: 1px solid var(--border-subtle); 
        }
        .footer-disclaimer {
            font-size: 0.8rem; 
            margin-top: 20px; 
            max-width: 800px; 
            margin-left: auto; 
            margin-right: auto; 
            color: #64748b;
        }

        /* ==========================================================================
           4. RESPONSIVE DESIGN (Media Queries)
           ========================================================================== */
        @media (max-width: 992px) {
            .hero-content { grid-template-columns: 1fr; text-align: center; gap: 40px; }
            .hero-text p { margin: 0 auto 30px auto; }
            .badge-group { justify-content: center; }
            .hero-buttons { justify-content: center; }
            .book-mockup-wrapper { margin-top: 20px; }
            .grid-3 { grid-template-columns: 1fr; }
            .chapter-grid { grid-template-columns: 1fr; }
        }

        @media (max-width: 768px) {
            .nav-links { display: none; } /* Sembunyi menu di mobile untuk kesederhanaan landing page */
            .btn-header { font-size: 0.9rem; padding: 10px 20px; }
            h1 { font-size: 2.5rem; }
            h2 { font-size: 2rem; }
            .section-padding { padding: 60px 0; }
            .demo-chart-wrapper { height: 200px; padding: 30px 15px; }
        }
    </style>
</head>
<body>

    <!-- 1. NAVBAR -->
    <nav id="navbar">
        <div class="container nav-container">
            <div class="logo">
                <span class="text-gold">M</span>C GOLD
            </div>
            <div class="nav-links">
                <a href="#masalah" class="scroll-link">Masalah</a>
                <a href="#kandungan" class="scroll-link">Isi Kandungan</a>
                <a href="#previu" class="scroll-link">Previu Visual</a>
            </div>
            <a href="#muat-turun" class="btn btn-outline btn-header scroll-link">Dapatkan Sekarang</a>
        </div>
    </nav>

    <!-- 2. HERO SECTION -->
    <section id="utama" class="hero">
        <div class="container hero-content">
            <div class="hero-text">
                <div class="badge-group">
                    <span class="badge">🔥 Edisi Terkini 2024</span>
                    <span class="badge">📊 Khas Untuk XAU/USD</span>
                </div>
                <h1>Berhenti <span class="text-gold">Teka-Teki</span> Arah Pasaran Emas.</h1>
                <p>Kuasai seni membaca \textit{candlestick}, fahami rahsia Support & Resistance sebenar, dan intip jejak langkah jerung pasaran melalui E-Buku premium ini.</p>
                <div class="hero-buttons">
                    <a href="#muat-turun" class="btn btn-gold scroll-link">Muat Turun Percuma</a>
                    <a href="#kandungan" class="btn btn-outline scroll-link">Lihat Kandungan</a>
                </div>
            </div>
            
            <div class="book-mockup-wrapper">
                <!-- Elemen 3D Buku menggunakan CSS Vanilla -->
                <div class="book-3d">
                    <div class="book-spine"></div>
                    <div class="book-front">
                        <div>
                            <div class="book-title-sub">MASTER CLASS GOLD</div>
                            <div class="book-title-main">Seni Membaca<br>Candlestick<br>XAU/USD</div>
                        </div>
                        <div>
                            <div class="book-divider"></div>
                            <div class="book-author">Panduan Lengkap Setup Entry & Pengurusan Risiko</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 3. PAIN POINTS SECTION (Masalah) -->
    <section id="masalah" class="section-padding pain-points">
        <div class="container">
            <div class="text-center">
                <h2>Adakah Anda Sering Mengalami Ini?</h2>
                <p style="max-width: 650px; margin: 0 auto;">Pasaran emas sangat kejam kepada mereka yang tidak berilmu. Jika 3 situasi di bawah sering berlaku pada anda, E-buku ini ditulis khas untuk anda.</p>
            </div>
            
            <div class="grid-3">
                <div class="feature-card">
                    <div class="card-icon">📉</div>
                    <h3>Asyik Terkena "Fakeout"</h3>
                    <p>Baru tekan BUY kerana nampak lilin hijau panjang memecah rintangan, tiba-tiba harga terus pacak junam ke bawah perangkap anda.</p>
                </div>
                <div class="feature-card">
                    <div class="card-icon">🎯</div>
                    <h3>Langgar Stop Loss (SL)</h3>
                    <p>Jerung seolah-olah nampak SL anda. Harga pergi menjilat garisan SL, mematikan posisi anda, kemudian terus terbang ke arah Take Profit.</p>
                </div>
                <div class="feature-card">
                    <div class="card-icon">🤯</div>
                    <h3>Gagap Waktu Berita (News)</h3>
                    <p>Tidak tahu apa kaitan data US Dollar (DXY), NFP, dan CPI dengan kenaikan atau kejatuhan harga emas yang secara mendadak.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 4. CHAPTERS SECTION (Isi Kandungan) -->
    <section id="kandungan" class="section-padding chapters">
        <div class="container">
            <div class="text-center">
                <h2><span class="text-gold">Apa Yang Anda Akan Belajar?</span></h2>
                <p style="max-width: 650px; margin: 0 auto;">Rahsia pasaran dibongkarkan dalam 6 bab padat tanpa teori meleret. Terus kepada praktikal teknikal.</p>
            </div>

            <div class="chapter-grid">
                <div class="chapter-item">
                    <div class="chapter-num">01</div>
                    <div class="chapter-text">
                        <h4>Asas & Anatomi Emas</h4>
                        <p>Kenali maksud tersembunyi di sebalik ekor (wick) panjang dan ketebalan badan (body) pasaran yang bergejolak.</p>
                    </div>
                </div>
                <div class="chapter-item">
                    <div class="chapter-num">02</div>
                    <div class="chapter-text">
                        <h4>Rahsia Support & Resistance</h4>
                        <p>Ketepikan candlestick sementara, fahami dahulu "Lantai & Bumbung" harga sebenar di mana jerung menanti mangsa.</p>
                    </div>
                </div>
                <div class="chapter-item">
                    <div class="chapter-num">03</div>
                    <div class="chapter-text">
                        <h4>Setup Kukuh BUY (Hammer)</h4>
                        <p>Gabungan mematikan: Harga terjun + Sentuh Garisan Support + Muncul pola Hammer. Kami tunjukkan cara entry tepat!</p>
                    </div>
                </div>
                <div class="chapter-item">
                    <div class="chapter-num">04</div>
                    <div class="chapter-text">
                        <h4>Setup Kukuh SELL (Shooting Star)</h4>
                        <p>Baca corak penolakan tegas di bumbung pasaran (Resistance) untuk 'ride' pasaran jatuh beratus-ratus pips.</p>
                    </div>
                </div>
                <div class="chapter-item">
                    <div class="chapter-num">05</div>
                    <div class="chapter-text">
                        <h4>Waktu & Berita (NFP / CPI)</h4>
                        <p>Ketahui Waktu Malaysia (MYT) yang paling agresif untuk entry dan fahami korelasi terbalik harga emas dengan kekuatan USD.</p>
                    </div>
                </div>
                <div class="chapter-item">
                    <div class="chapter-num">06</div>
                    <div class="chapter-text">
                        <h4>Pengurusan Risiko (SL & Lot)</h4>
                        <p>Formula mengira lot selamat dan penetapan nisbah 1:3. Strategi di mana walaupun anda kalah 5 kali, anda tetap meraih keuntungan bersih!</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 5. SNEAK PEEK SECTION (Previu Visual) -->
    <section id="previu" class="section-padding sneak-peek">
        <div class="container">
            <div class="text-center">
                <h2>Mengapa Buku Ini Berbeza?</h2>
                <p style="max-width: 750px; margin: 0 auto;">Bukan sekadar teks tulisan yang membosankan. E-Buku ini disertakan dengan gambar rajah simulasi pasaran (seperti di bawah) berserta garisan Zon Entry dan paras selamat Stop Loss yang sangat jelas.</p>
            </div>

            <!-- Simulasi Carta (CSS Only) -->
            <div class="demo-chart-wrapper">
                <!-- Lilin 1: Turun -->
                <div class="mc-wrapper"><div class="mc-wick" style="top: 15%; bottom: 40%;"></div><div class="mc-body mc-bear" style="top: 25%; bottom: 40%;"></div></div>
                <!-- Lilin 2: Turun -->
                <div class="mc-wrapper"><div class="mc-wick" style="top: 35%; bottom: 55%;"></div><div class="mc-body mc-bear" style="top: 40%; bottom: 55%;"></div></div>
                
                <!-- Lilin 3: THE HAMMER (Dengan Animasi Fokus) -->
                <div class="mc-wrapper">
                    <div class="highlight-pattern"></div>
                    <div class="mc-wick" style="top: 50%; bottom: 5%; z-index: 2;"></div> 
                    <div class="mc-body mc-bull" style="top: 50%; height: 20%; z-index: 2;"></div>
                </div>

                <!-- Lilin 4: Naik (Pengesahan) -->
                <div class="mc-wrapper"><div class="mc-wick" style="top: 25%; bottom: 15%;"></div><div class="mc-body mc-bull" style="top: 25%; bottom: 45%;"></div></div>
                <!-- Lilin 5: Naik -->
                <div class="mc-wrapper"><div class="mc-wick" style="top: 5%; bottom: 15%;"></div><div class="mc-body mc-bull" style="top: 10%; bottom: 30%;"></div></div>
            </div>
        </div>
    </section>

    <!-- 6. CALL TO ACTION SECTION (Muat Turun) -->
    <section id="muat-turun" class="cta-section">
        <div class="container cta-content">
            <h2 style="font-size: clamp(2rem, 4vw, 2.8rem); margin-bottom: 20px;">Bersedia Untuk Mengubah Cara Anda Berdagang?</h2>
            <p style="font-size: 1.15rem; margin-bottom: 40px;">Berhenti merisikokan modal titik peluh anda tanpa ilmu teknikal yang betul. Muat turun E-Buku lengkap (PDF/HTML) ini sekarang dan mula membacanya secara terus pada mana-mana peranti.</p>
            
            <!-- Butang Tindakan -->
            <a href="javascript:void(0)" id="downloadBtn" class="btn btn-gold" style="font-size: 1.25rem; padding: 20px 50px;">
                MUAT TURUN E-BUKU (PERCUMA)
            </a>
            
            <p style="margin-top: 20px; font-size: 0.9rem; color: var(--text-muted);">Format PDF Berkualiti Tinggi. Sedia untuk dibaca terus.</p>
        </div>
    </section>

    <!-- 7. FOOTER -->
    <footer>
        <div class="container">
            <div class="logo" style="justify-content: center; margin-bottom: 15px;">
                <span class="text-gold">M</span>C GOLD
            </div>
            <p style="margin-bottom: 10px;">&copy; <span id="currentYear"></span> Master Class Gold Trading. Hak Cipta Terpelihara.</p>
            <p class="footer-disclaimer">
                Penafian (Disclaimer): Dagangan tukaran mata wang asing (Forex) dan komoditi emas (XAU/USD) melibatkan tahap risiko yang sangat tinggi dan mungkin tidak sesuai untuk semua pelabur. Anda mungkin mengalami kerugian sebahagian atau keseluruhan modal awal anda. Kandungan E-Buku dan laman web ini hanyalah untuk tujuan pendidikan (edukasi) semata-mata dan tidak boleh dianggap sebagai nasihat kewangan profesional.
            </p>
        </div>
    </footer>

    <!-- ==========================================================================
         JAVASCRIPT LOGIC (Vanilla JS)
         ========================================================================== -->
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            
            // 1. Logik Kemas Kini Tahun Footer (Dinamik)
            document.getElementById('currentYear').textContent = new Date().getFullYear();

            // 2. Logik Skrol Lancar (Smooth Scroll) untuk pautan menu
            const scrollLinks = document.querySelectorAll('.scroll-link');
            
            scrollLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    
                    // Dapatkan ID sasaran
                    const targetId = this.getAttribute('href');
                    if(targetId === '#') return;
                    
                    const targetSection = document.querySelector(targetId);
                    if(targetSection) {
                        // Tolak ketinggian navbar statik supaya tajuk tidak tertutup
                        const headerOffset = 80; 
                        const elementPosition = targetSection.getBoundingClientRect().top;
                        const offsetPosition = elementPosition + window.pageYOffset - headerOffset;
        
                        window.scrollTo({
                            top: offsetPosition,
                            behavior: "smooth"
                        });
                    }
                });
            });

            // 3. Logik Penukaran Gaya Navbar Apabila Di-skrol (Navbar Shrink/Shadow)
            const navbar = document.getElementById('navbar');
            
            window.addEventListener('scroll', () => {
                if (window.scrollY > 50) {
                    navbar.classList.add('scrolled');
                } else {
                    navbar.classList.remove('scrolled');
                }
            });

            // 4. Sistem ScrollSpy (Menonjolkan menu aktif berdasarkan posisi skrin)
            const sections = document.querySelectorAll("section");
            const navLinks = document.querySelectorAll(".nav-links a");

            window.addEventListener('scroll', () => {
                let current = "";
                // Offset tambahan untuk trigger pertukaran menu lebih awal
                const scrollPosition = window.scrollY + 200; 

                sections.forEach(section => {
                    const sectionTop = section.offsetTop;
                    const sectionHeight = section.clientHeight;
                    if (scrollPosition >= sectionTop && scrollPosition < sectionTop + sectionHeight) {
                        current = section.getAttribute("id");
                    }
                });

                navLinks.forEach(link => {
                    link.classList.remove("active");
                    if (link.getAttribute("href") === `#${current}`) {
                        link.classList.add("active");
                    }
                });
            });

            // 5. Fungsi Simulasi Butang Muat Turun (Call to Action)
            const downloadBtn = document.getElementById('downloadBtn');
            downloadBtn.addEventListener('click', function() {
                // Tukar rupa butang buat sementara waktu untuk UX yang baik
                const originalText = this.innerHTML;
                this.innerHTML = "Memproses Muat Turun...";
                this.style.opacity = "0.8";
                this.style.pointerEvents = "none";
                
                setTimeout(() => {
                    // Arahan untuk sistem sebenar: 
                    // Gantikan arahan alert() di bawah dengan kod muat turun (contoh: window.open('link-ke-pdf-anda.pdf'))
                    alert("Terima kasih! Dalam persekitaran web sebenar, butang ini akan terus memuat turun fail PDF E-Buku Trading Gold anda ke peranti pengguna.");
                    
                    // Kembalikan keadaan butang kepada asal
                    this.innerHTML = originalText;
                    this.style.opacity = "1";
                    this.style.pointerEvents = "auto";
                }, 1500);
            });
        });
    </script>

</body>
</html>
<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>بورتفوليو محمد مداح</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Cairo', sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            color: #fff;
            direction: rtl;
            overflow-x: hidden;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        /* ناف بار */
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 40px;
            background: rgba(0, 0, 0, 0.4);
            backdrop-filter: blur(10px);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            transition: 0.3s;
            box-shadow: 0 0 15px rgba(138, 43, 226, 0.5);
        }

        nav.scrolled {
            background: rgba(0, 0, 0, 0.8);
            box-shadow: 0 0 25px rgba(0, 212, 255, 0.6);
        }

        nav h1 {
            font-size: 1.8rem;
            font-weight: bold;
            color: #00d4ff;
            text-shadow: 0 0 10px #00d4ff, 0 0 20px #6a5acd;
        }

        nav ul {
            display: flex;
            gap: 25px;
            list-style: none;
        }

        nav ul li {
            font-size: 1.1rem;
            cursor: pointer;
            transition: 0.3s;
        }

        nav ul li:hover {
            color: #00d4ff;
            text-shadow: 0 0 10px #00d4ff, 0 0 20px #6a5acd;
        }

        /* الهيرو */
        .hero {
            padding-top: 150px;
            text-align: center;
            margin-bottom: 60px;
        }

        .name-box {
            display: inline-block;
            padding: 20px 50px;
            border: 3px solid #6a5acd;
            border-radius: 20px;
            background: rgba(255, 255, 255, 0.05);
            box-shadow: 0 0 25px #6a5acd, 0 0 40px #00d4ff;
            font-size: 3rem;
            font-weight: bold;
            color: #fff;
            animation: glow 2s infinite alternate;
            transition: transform 0.3s;
        }

        .name-box:hover {
            transform: scale(1.07) rotate(1deg);
        }

        @keyframes glow {
            from { box-shadow: 0 0 15px #6a5acd, 0 0 25px #00d4ff; }
            to { box-shadow: 0 0 35px #00d4ff, 0 0 55px #6a5acd; }
        }

        .subtitle {
            font-size: 1.3rem;
            margin-top: 15px;
            color: #ccc;
            animation: fadeIn 2s ease forwards;
        }

        @keyframes fadeIn {
            0% { opacity: 0; transform: translateY(20px);}
            100% { opacity: 1; transform: translateY(0);}
        }

        /* آراء الطلاب */
        .reviews {
            text-align: center;
            padding: 60px 20px;
        }

        .reviews h2 {
            font-size: 2rem;
            margin-bottom: 30px;
            color: #00d4ff;
            text-shadow: 0 0 10px #00d4ff;
        }

        .slider {
            display: flex;
            overflow-x: auto;
            scroll-snap-type: x mandatory;
            gap: 15px;
            padding: 20px;
            scrollbar-width: thin;
            scrollbar-color: #6a5acd transparent;
        }

        .slider::-webkit-scrollbar {
            height: 8px;
        }

        .slider::-webkit-scrollbar-thumb {
            background: #6a5acd;
            border-radius: 4px;
        }

        .card {
            min-width: 250px;
            flex: none;
            background: rgba(255, 255, 255, 0.05);
            padding: 25px;
            border-radius: 20px;
            box-shadow: 0 0 15px rgba(106, 90, 205, 0.7);
            scroll-snap-align: start;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .card:hover {
            transform: scale(1.06) translateY(-5px);
            box-shadow: 0 0 25px #00d4ff, 0 0 40px #6a5acd;
        }

        .card p {
            font-size: 1rem;
            color: #fff;
            line-height: 1.5;
        }

        /* الحجز */
        .booking {
            text-align: center;
            padding: 40px 20px;
        }

        .btn {
            display: inline-block;
            background: linear-gradient(135deg, #6a5acd, #00d4ff);
            padding: 18px 50px;
            border-radius: 50px;
            font-size: 1.5rem;
            font-weight: bold;
            color: #fff;
            box-shadow: 0 0 15px #00d4ff, 0 0 30px #6a5acd;
            transition: transform 0.3s, box-shadow 0.3s;
            animation: pulse 1.5s infinite;
        }

        .btn:hover {
            transform: scale(1.08);
            box-shadow: 0 0 30px #00d4ff, 0 0 50px #6a5acd;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        .whatsapp {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
            margin-top: 20px;
            font-size: 1.2rem;
        }

        .whatsapp img {
            width: 35px;
            height: 35px;
            animation: bounce 1.5s infinite;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-5px); }
        }

        /* فوتر */
        footer {
            text-align: center;
            padding: 20px;
            margin-top: 30px;
            color: #aaa;
            font-size: 0.9rem;
            border-top: 1px solid rgba(255,255,255,0.1);
        }

        /* تحسين تجربة الهواتف */
        @media (max-width: 768px) {
            .name-box {
                font-size: 2.2rem;
                padding: 15px 30px;
            }
            nav ul {
                gap: 15px;
                font-size: 0.95rem;
            }
            .card {
                min-width: 200px;
            }
        }

        @media (max-width: 480px) {
            .name-box {
                font-size: 1.8rem;
                padding: 12px 20px;
            }
            .btn {
                padding: 15px 35px;
                font-size: 1.2rem;
            }
        }

    </style>
</head>
<body>

    <!-- ناف بار -->
    <nav id="navbar">
        <h1>محمد مداح | Mohamed Maddah</h1>
        <ul>
            <li><a href="#hero">الرئيسية</a></li>
            <li><a href="#reviews">آراء الطلاب</a></li>
            <li><a href="#booking">احجز الآن</a></li>
        </ul>
    </nav>

    <!-- الهيرو -->
    <section class="hero" id="hero">
        <div class="name-box">محمد مداح | Mohamed Maddah</div>
        <p class="subtitle">مدرس الكيمياء والعلوم المتكاملة</p>
    </section>

    <!-- آراء الطلاب -->
    <section class="reviews" id="reviews">
        <h2>آراء الطلاب</h2>
        <div class="slider">
            <div class="card"><p>مستوى الشرح ممتاز جدًا! 🌟</p></div>
            <div class="card"><p>أسلوبه بسيط وسلس 👌</p></div>
            <div class="card"><p>أفهم الكيمياء لأول مرة 😍</p></div>
            <div class="card"><p>أفضل مدرس على الإطلاق! 💙</p></div>
            <div class="card"><p>تعلمت منه كتير 🙌</p></div>
            <div class="card"><p>شرح ممتع وشيق جدًا ✨</p></div>
            <div class="card"><p>بيوصل المعلومة بسهولة 👌</p></div>
            <div class="card"><p>مدرس محترم جدًا 🌟</p></div>
            <div class="card"><p>أنصح أي حد يحضر معاه 💯</p></div>
            <div class="card"><p>أفضل تجربة تعلم كيمياء 🧪</p></div>
        </div>
    </section>

    <!-- الحجز -->
    <section class="booking" id="booking">
        <a href="https://wa.me/201099540842" class="btn" aria-label="احجز الآن على واتساب">احجز الآن</a>
        <div class="whatsapp">
            <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg" alt="واتساب">
            <span>01099540842</span>
        </div>
    </section>

    <!-- فوتر -->
    <footer>
        © 2025 جميع الحقوق محفوظة | محمد مداح
    </footer>

    <script>
        // تغيير لون الناف بار عند التمرير
        const navbar = document.getElementById('navbar');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });
    </script>
</body>
</html>

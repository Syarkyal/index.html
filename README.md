# index.html
https://www.facebook.com/share/17x1B4dKsh/?mibextid=wwXIfr
<!DOCTYPE html>
<html lang="my">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BoKyalsin | Official Portfolio & Blog</title>
    <style>
        /* --- Root Variables for Dark/Light Mode --- */
        :root {
            --bg-primary: #f8f9fa;
            --bg-card: #ffffff;
            --text-main: #2d3436;
            --text-muted: #636e72;
            --accent-color: #d35400;
            --nav-bg: #1e272e;
            --border-color: #f1f2f6;
        }

        [data-theme="dark"] {
            --bg-primary: #111215;
            --bg-card: #1a1c23;
            --text-main: #f5f6fa;
            --text-muted: #a4b0be;
            --accent-color: #e67e22;
            --nav-bg: #090a0c;
            --border-color: #2c2f3a;
        }

        /* --- Global Styles --- */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            transition: background-color 0.3s ease, color 0.3s ease;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif, 'Pyidaungsu';
            background-color: var(--bg-primary);
            color: var(--text-main);
            line-height: 1.8;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* --- Navigation --- */
        nav {
            background-color: var(--nav-bg);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            color: #f1c40f;
            font-size: 24px;
            font-weight: 700;
            text-decoration: none;
            letter-spacing: 1px;
        }

        .logo span { color: #ffffff; font-weight: 300; }

        .theme-toggle {
            background: #2c3e50;
            border: none;
            color: #f1c40f;
            padding: 8px 15px;
            cursor: pointer;
            border-radius: 20px;
            font-size: 14px;
            font-weight: bold;
        }

        /* --- Hero Section --- */
        .hero {
            background: linear-gradient(135deg, #1e272e 0%, #2c3e50 100%);
            color: #ffffff;
            padding: 80px 0;
            text-align: center;
            border-bottom: 5px solid var(--accent-color);
        }

        .hero h1 {
            font-size: 42px;
            margin-bottom: 15px;
            letter-spacing: 1px;
        }

        .hero p {
            font-size: 18px;
            color: #ced6e0;
            max-width: 600px;
            margin: 0 auto;
        }

        /* --- Main Layout --- */
        .grid-layout {
            display: grid;
            grid-template-columns: 2.5fr 1fr;
            gap: 30px;
            margin-top: 40px;
        }

        @media (max-width: 900px) {
            .grid-layout { grid-template-columns: 1fr; }
        }

        /* --- Category Tabs --- */
        .tabs {
            display: flex;
            gap: 10px;
            margin-bottom: 25px;
            overflow-x: auto;
            padding-bottom: 5px;
        }

        .tab-btn {
            background-color: var(--bg-card);
            border: 1px solid var(--border-color);
            color: var(--text-main);
            padding: 10px 20px;
            font-size: 15px;
            font-weight: 600;
            cursor: pointer;
            border-radius: 30px;
            white-space: nowrap;
        }

        .tab-btn.active {
            background-color: var(--accent-color);
            color: white;
            border-color: var(--accent-color);
        }

        /* --- Content Cards --- */
        .content-section { display: none; }
        .content-section.active { display: block; animation: slideUp 0.4s ease; }

        @keyframes slideUp {
            from { opacity: 0; transform: translateY(15px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .card {
            background-color: var(--bg-card);
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.03);
            margin-bottom: 25px;
            border: 1px solid var(--border-color);
        }

        .card h2 {
            font-size: 22px;
            margin-bottom: 20px;
            color: var(--accent-color);
        }

        .post {
            border-bottom: 1px solid var(--border-color);
            padding-bottom: 20px;
            margin-bottom: 20px;
        }

        .post:last-child { border-bottom: none; padding-bottom: 0; margin-bottom: 0; }
        
        .post-title { font-size: 19px; margin: 10px 0; color: var(--text-main); }
        .post-meta { font-size: 13px; color: var(--text-muted); }
        .post p { color: var(--text-muted); font-size: 15px; }

        .badge {
            background-color: var(--accent-color);
            color: white;
            padding: 3px 10px;
            font-size: 11px;
            text-transform: uppercase;
            border-radius: 4px;
            font-weight: bold;
        }

        /* --- Sidebar --- */
        .sidebar-card {
            background-color: var(--bg-card);
            padding: 25px;
            border-radius: 12px;
            border: 1px solid var(--border-color);
            margin-bottom: 25px;
        }

        .sidebar-card h3 {
            font-size: 18px;
            margin-bottom: 15px;
            border-bottom: 2px solid var(--accent-color);
            padding-bottom: 5px;
        }

        .sidebar-card ul { list-style: none; }
        .sidebar-card li {
            padding: 10px 0;
            border-bottom: 1px solid var(--border-color);
            font-size: 14px;
            color: var(--text-muted);
        }

        /* --- Footer --- */
        footer {
            background-color: var(--nav-bg);
            color: #a4b0be;
            text-align: center;
            padding: 30px 0;
            margin-top: 60px;
            font-size: 14px;
            border-top: 3px solid var(--accent-color);
        }
    </style>
</head>
<body>

    <!-- Navigation -->
    <nav>
        <div class="container nav-container">
            <a href="#" class="logo">BoKyalsin<span>.Space</span></a>
            <button class="theme-toggle" onclick="toggleTheme()">🌓 Theme</button>
        </div>
    </nav>

    <!-- Header / Hero -->
    <header class="hero">
        <div class="container">
            <h1>BoKyalsin</h1>
            <p>သမိုင်းဝင် စုံထောက်ဝတ္ထုများ၊ အနုပညာဖန်တီးမှုများနှင့် နည်းပညာအမြင်များ စုစည်းရာ နေရာဆန်း</p>
        </div>
    </header>

    <!-- Main Grid Layout -->
    <div class="container grid-layout">
        
        <!-- Left Content Component -->
        <main>
            <!-- Category Filter Tabs -->
            <div class="tabs">
                <button class="tab-btn active" onclick="switchTab(event, 'novels')">📖 ဝတ္ထုရှည်များ</button>
                <button class="tab-btn" onclick="switchTab(event, 'lyrics')">🎵 တေးကဗျာ / Lyrics</button>
                <button class="tab-btn" onclick="switchTab(event, 'history')">📜 သမိုင်းကဏ္ဍ</button>
                <button class="tab-btn" onclick="switchTab(event, 'sports')">⚽ အားကစားဆောင်းပါး</button>
            </div>

            <!-- Tab: Novels -->
            <div id="novels" class="content-section active">
                <div class="card">
                    <h2>၁၉၄၀ ကာလနောက်ခံ သမိုင်းဝင်စုံထောက်ဝတ္ထုကြီး</h2>
                    <div class="post">
                        <span class="badge">ထွက်ရှိပြီးသမျှ ဇာတ်လမ်းများ</span>
                        <h3 class="post-title">မြိတ်ကျွန်းစုမှ ဆန်းကြယ်သောအမှုအခင်း (ISP ဗိုလ်ကြယ်နှင့် ဒေါက်တာဖြိုးထွန်း)</h3>
                        <p class="post-meta">ရေးသူ - BoKyalsin | အခန်းပေါင်း (၁၇) ခန်းလုံးကို စိတ်ကြိုက် ဖတ်ရှုနိုင်ရန် မကြာမီ စုံလင်စွာ တင်ဆက်ပေးသွားပါမည်။</p>
                        <p>၁၉၄၀ ပြည့်လွန်နှစ်များ ကိုလိုနီခေတ် နှောင်းပိုင်းကာလ မြိတ်ကျွန်းစု၏ အုံ့မှိုင်းဆန်းကြယ်သော ရာသီဥတုနှင့်အတူ ပေါ်ပေါက်လာသည့် နက်နဲလှသော လူသတ်မှုတစ်ခု။ အမှန်တရားကို ဖော်ထုတ်မည့် စုံထောက်အရာရှိ အိုင်အက်စ်ပီ ဗိုလ်ကြယ်နှင့် ၎င်း၏ မိတ်ဆွေ ဒေါက်တာဖြိုးထွန်းတို့၏ သည်းထိတ်ရင်ဖို စုံထောက်ခရီးစဉ်။</p>
                    </div>
                </div>
            </div>

            <!-- Tab: Lyrics -->
            <div id="lyrics" class="content-section">
                <div class="card">
                    <h2>လွမ်းဆွေးမှုနှင့် ကြေကွဲမှုနောက်ခံ တေးကဗျာများ</h2>
                    <div class="post">
                        <span class="badge">Pop Genre</span>
                        <h3 class="post-title">နှလုံးသားကြေကွဲမှုနှင့် Lovesick ကဗျာစာသားများ</h3>
                        <p class="post-meta">အချစ်ဦး ဆုံးရှုံးရခြင်းနှင့် Mourning Themes များ</p>
                        <p>သစ္စာဖောက်ဖျက်ခြင်းခံရမှု၊ ရင်ထဲက အလွမ်းဓာတ်များနှင့် သံယောဇဉ် ဖြတ်တောက်ရခက်ပုံများကို စာသားအလှများဖြင့် ပုံဖော်ထားသော ပေါ့ပ်ဂီတနောက်ခံ ကိုယ်ပိုင် Lyrics မော်ကွန်းစုများ။</p>
                    </div>
                </div>
            </div>

            <!-- Tab: History -->
            <div id="history" class="content-section">
                <div class="card">
                    <h2>မြန်မာ့သမိုင်းနှင့် ကုန်းဘောင်ခေတ်အမြင်များ</h2>
                    <div class="post">
                        <span class="badge">သမိုင်းသုတေသန</span>
                        <h3 class="post-title">နတ်သျှင်နောင်နှင့် ကုန်းဘောင်ခေတ် ထင်ရှားသူများ</h3>
                        <p class="post-meta">သမိုင်းဝင် ဖြစ်ရပ်မှန်များလေ့လာချက်</p>
                        <p>ကုန်းဘောင်ခေတ်၏ ယဉ်ကျေးမှု၊ ဗိသုကာအတတ်ပညာများနှင့် ထင်ရှားကျော်ကြားလှသော သမိုင်းဝင် ပုဂ္ဂိုလ်ကြီးများ (ဥပမာ- နတ်သျှင်နောင်) တို့၏ ဘဝကဏ္ဍများကို စိတ်ဝင်စားဖွယ် ဆန်းစစ်တင်ပြထားချက်များ။</p>
                    </div>
                </div>
            </div>

            <!-- Tab: Sports -->
            <div id="sports" class="content-section">
                <div class="card">
                    <h2>ဘောလုံးလောကနှင့် ဂန္ထဝင်ကစားသမားများ သုံးသပ်ချက်</h2>
                    <div class="post">
                        <span class="badge">Football Analysis</span>
                        <h3 class="post-title">Cristiano Ronaldo နှင့် Lionel Messi ဆယ်စုနှစ်တစ်ခုကျော် အားပြိုင်မှု</h3>
                        <p class="post-meta">လတ်တလော အားကစားသတင်းများနှင့် ကစားသမားစွမ်းဆောင်ရည် နှိုင်းယှဉ်ချက်</p>
                        <p>ဘောလုံးလောက၏ အကြီးကျယ်ဆုံးသော ပြိုင်ဘက်ကြီးနှစ်ဦးဖြစ်သည့် ရော်နယ်ဒိုနှင့် မက်ဆီတို့၏ သမိုင်းဝင် မှတ်တမ်းများ၊ ကစားဟန်များနှင့် ကလပ်အသင်းအလိုက် ရလဒ်များကို အချိန်နဲ့တစ်ပြေးညီ လေ့လာဆန်းစစ်ချက် ဆောင်းပါးများ။</p>
                    </div>
                </div>
            </div>
        </main>

        <!-- Right Sidebar Area -->
        <aside>
            <div class="sidebar-card">
                <h3>Author Profile</h3>
                <p>ကျွန်တော်ကတော့ စာပေရေးသားခြင်း၊ သမိုင်းလေ့လာခြင်းနှင့် ခေတ်မီနည်းပညာရပ်များကို ဖော်ထုတ်ရတာ ဝါသနာပါတဲ့ ဖန်တီးသူ BoKyalsin ဖြစ်ပါတယ်။</p>
            </div>

            <div class="sidebar-card">
                <h3>Gaming & Tech Hardware</h3>
                <p>မိုဘိုင်းလ်ဂိမ်းများကို စွမ်းဆောင်ရည်အမြင့်ဆုံး (Max Efficiency) ဖြင့် ဆော့ကစားနိုင်ရန်အတွက် လိုအပ်သော Specs များနှင့် Hardware ပိုင်းဆိုင်ရာ လမ်းညွှန်ချက်များ။</p>
                <ul>
                    <li>• Mobile Processor Analysis</li>
                    <li>• Gaming Device Reviews</li>
                    <li>• Performance Automation</li>
                </ul>
            </div>
        </aside>

    </div>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2026 BoKyalsin. Powered by GitHub Pages. All Rights Reserved.</p>
        </div>
    </footer>

    <!-- Scripts for Functionality -->
    <script>
        // Tab Switcher Function
        function switchTab(evt, tabId) {
            let contents = document.getElementsByClassName("content-section");
            for (let i = 0; i < contents.length; i++) {
                contents[i].className = contents[i].className.replace(" active", "");
            }

            let buttons = document.getElementsByClassName("tab-btn");
            for (let i = 0; i < buttons.length; i++) {
                buttons[i].className = buttons[i].className.replace(" active", "");
            }

            document.getElementById(tabId).className += " active";
            evt.currentTarget.className += " active";
        }

        // Dark/Light Mode Theme Switcher
        function toggleTheme() {
            const currentTheme = document.documentElement.getAttribute("data-theme");
            if (currentTheme === "dark") {
                document.documentElement.setAttribute("data-theme", "light");
            } else {
                document.documentElement.setAttribute("data-theme", "dark");
            }
        }
        
        // Default to Light Mode
        document.documentElement.setAttribute("data-theme", "light");
    </script>
</body>
</html>

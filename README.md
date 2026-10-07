<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>This is your website</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
        body { background-color: #fdfbf7; color: #2c2c2c; line-height: 1.6; }
        header { background: #1a1a1a; color: #fff; padding: 20px 8%; display: flex; justify-content: space-between; align-items: center; }
        header h1 { font-size: 22px; font-weight: 600; letter-spacing: 1px; }
        nav a { color: #ddd; margin-left: 20px; text-decoration: none; font-size: 14px; }
        nav a:hover { color: #d4af37; }
        
        .hero { text-align: center; padding: 80px 20px; background: #f4efe6; border-bottom: 1px solid #e2dacb; }
        .hero h2 { font-size: 38px; color: #1a1a1a; margin-bottom: 10px; }
        .hero p { font-size: 18px; color: #555; max-width: 600px; margin: 0 auto 25px; }
        .btn { display: inline-block; background: #d4af37; color: #fff; padding: 12px 28px; text-decoration: none; border-radius: 4px; font-weight: bold; }
        .btn:hover { background: #b8952b; }

        .container { padding: 60px 8%; max-width: 1100px; margin: 0 auto; }
        .section-title { text-align: center; font-size: 28px; margin-bottom: 40px; position: relative; }
        
        .menu-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 25px; }
        .menu-card { background: #fff; border: 1px solid #eee; padding: 20px; border-radius: 6px; box-shadow: 0 2px 5px rgba(0,0,0,0.03); }
        .menu-card h3 { display: flex; justify-content: space-between; font-size: 18px; margin-bottom: 8px; color: #1a1a1a; }
        .menu-card span { color: #d4af37; font-weight: bold; }
        .menu-card p { font-size: 14px; color: #666; }

        footer { background: #1a1a1a; color: #888; text-align: center; padding: 30px; font-size: 14px; margin-top: 60px; }
        footer strong { color: #fff; }
    </style>
</head>
<body>

    <header>
        <h1>This is your website</h1>
        <nav>
            <a href="#menu">Menu</a>
            <a href="#about">About</a>
            <a href="#contact">Contact</a>
        </nav>
    </header>

    <section class="hero">
        <h2>Fresh & Authentic Taste</h2>
        <p>Handcrafted dishes made daily with fresh local ingredients and traditional recipes.</p>
        <a href="https://wa.me/YOUR_PHONE_NUMBER?text=Hello,%20I%20want%20to%20place%20an%20order" class="btn" target="_blank">Order via WhatsApp</a>
    </section>

    <div class="container" id="menu">
        <h2 class="section-title">Special Menu</h2>
        <div class="menu-grid">
            <div class="menu-card">
                <h3>Special Meal Deal <span>$15</span></h3>
                <p>Freshly cooked main course served with side salad and home-style drink.</p>
            </div>
            <div class="menu-card">
                <h3>Chef Special Platter <span>$22</span></h3>
                <p>Assorted grilled dishes served with custom garlic sauces and fresh bread.</p>
            </div>
            <div class="menu-card">
                <h3>Traditional Dessert <span>$8</span></h3>
                <p>Classic handmade dessert recipe made fresh every morning.</p>
            </div>
        </div>
    </div>

    <footer>
        <p>Designed with care by <strong>Ayan Ahmad</strong></p>
        <p>© 2026 All Rights Reserved.</p>
    </footer>

</body>
</html>

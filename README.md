<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="A warm, modern restaurant website with menu and WhatsApp ordering.">
  <title>This is your website</title>

  <style>
    :root {
      --cream: #f8f3e8;
      --cream-dark: #eee5d3;
      --charcoal: #25231f;
      --muted: #716b61;
      --gold: #b58a45;
      --gold-dark: #946e35;
      --white: #fffdf8;
      --border: #e4dac8;
      --shadow: 0 10px 30px rgba(37, 35, 31, 0.08);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background: var(--cream);
      color: var(--charcoal);
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(1120px, 92%);
      margin: 0 auto;
    }

    /* Header */
    header {
      background: rgba(248, 243, 232, 0.96);
      border-bottom: 1px solid var(--border);
      position: sticky;
      top: 0;
      z-index: 100;
    }

    .nav {
      min-height: 72px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 30px;
    }

    .logo {
      font-family: Georgia, "Times New Roman", serif;
      font-size: 1.35rem;
      font-weight: 700;
      letter-spacing: 0.3px;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 28px;
      list-style: none;
    }

    .nav-links a {
      font-size: 0.95rem;
      color: var(--muted);
      transition: color 0.2s ease;
    }

    .nav-links a:hover {
      color: var(--gold-dark);
    }

    /* Hero */
    .hero {
      min-height: 650px;
      display: flex;
      align-items: center;
      padding: 90px 0;
      background:
        linear-gradient(rgba(248, 243, 232, 0.78), rgba(248, 243, 232, 0.96)),
        radial-gradient(circle at 80% 20%, rgba(181, 138, 69, 0.15), transparent 35%);
    }

    .hero-content {
      max-width: 760px;
    }

    .eyebrow {
      color: var(--gold-dark);
      text-transform: uppercase;
      letter-spacing: 3px;
      font-size: 0.78rem;
      font-weight: 700;
      margin-bottom: 18px;
    }

    .hero h1 {
      font-family: Georgia, "Times New Roman", serif;
      font-size: clamp(3rem, 7vw, 5.8rem);
      line-height: 0.98;
      font-weight: 500;
      margin-bottom: 25px;
    }

    .hero h1 span {
      color: var(--gold-dark);
    }

    .hero p {
      max-width: 620px;
      color: var(--muted);
      font-size: 1.15rem;
      margin-bottom: 35px;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      min-height: 52px;
      padding: 0 26px;
      border-radius: 4px;
      font-weight: 700;
      font-size: 0.95rem;
      transition: background 0.2s ease, transform 0.2s ease;
    }

    .btn-primary {
      background: var(--charcoal);
      color: var(--white);
    }

    .btn-primary:hover {
      background: var(--gold-dark);
      transform: translateY(-2px);
    }

    /* Sections */
    section {
      padding: 90px 0;
    }

    .section-heading {
      max-width: 650px;
      margin-bottom: 45px;
    }

    .section-heading .eyebrow {
      margin-bottom: 10px;
    }

    .section-heading h2 {
      font-family: Georgia, "Times New Roman", serif;
      font-size: clamp(2.2rem, 5vw, 3.4rem);
      font-weight: 500;
      line-height: 1.1;
      margin-bottom: 15px;
    }

    .section-heading p {
      color: var(--muted);
    }

    /* Menu */
    .menu-section {
      background: var(--white);
    }

    .menu-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 22px;
    }

    .menu-card {
      background: var(--cream);
      border: 1px solid var(--border);
      padding: 28px;
      border-radius: 8px;
      box-shadow: var(--shadow);
    }

    .menu-card h3 {
      font-family: Georgia, "Times New Roman", serif;
      font-size: 1.45rem;
      font-weight: 600;
      margin-bottom: 10px;
    }

    .menu-card p {
      color: var(--muted);
      font-size: 0.94rem;
      margin-bottom: 22px;
    }

    .price {
      color: var(--gold-dark);
      font-size: 1.05rem;
      font-weight: 700;
    }

    /* About */
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 70px;
      align-items: center;
    }

    .about-title {
      font-family: Georgia, "Times New Roman", serif;
      font-size: clamp(2.2rem, 5vw, 3.5rem);
      line-height: 1.1;
      font-weight: 500;
      margin-bottom: 20px;
    }

    .about-text {
      color: var(--muted);
      margin-bottom: 18px;
    }

    .about-box {
      min-height: 360px;
      background: var(--charcoal);
      color: var(--white);
      border-radius: 8px;
      padding: 45px;
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
    }

    .about-box small {
      color: #d7bd91;
      text-transform: uppercase;
      letter-spacing: 2px;
      margin-bottom: 10px;
    }

    .about-box h3 {
      font-family: Georgia, "Times New Roman", serif;
      font-size: 2rem;
      font-weight: 500;
    }

    /* Contact */
    .contact-section {
      background: var(--cream-dark);
    }

    .contact-box {
      background: var(--white);
      border: 1px solid var(--border);
      padding: 45px;
      border-radius: 8px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 35px;
    }

    .contact-box h2 {
      font-family: Georgia, "Times New Roman", serif;
      font-size: 2.3rem;
      font-weight: 500;
      margin-bottom: 10px;
    }

    .contact-box p {
      color: var(--muted);
    }

    /* Footer */
    footer {
      background: var(--charcoal);
      color: var(--white);
      padding: 35px 0;
    }

    .footer-content {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }

    .footer-content p {
      color: #c9c2b7;
      font-size: 0.9rem;
    }

    .footer-brand {
      font-family: Georgia, "Times New Roman", serif;
      font-size: 1.15rem;
    }

    /* Mobile */
    @media (max-width: 800px) {
      .nav {
        min-height: 64px;
      }

      .nav-links {
        gap: 16px;
      }

      .nav-links a {
        font-size: 0.85rem;
      }

      .hero {
        min-height: 590px;
        padding: 75px 0;
      }

      section {
        padding: 70px 0;
      }

      .menu-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .about-grid {
        grid-template-columns: 1fr;
        gap: 35px;
      }

      .contact-box {
        flex-direction: column;
        align-items: flex-start;
      }
    }

    @media (max-width: 560px) {
      .logo {
        font-size: 1.1rem;
      }

      .nav-links {
        gap: 12px;
      }

      .nav-links a {
        font-size: 0.78rem;
      }

      .hero h1 {
        font-size: 3.3rem;
      }

      .hero p {
        font-size: 1rem;
      }

      .menu-grid {
        grid-template-columns: 1fr;
      }

      .menu-card {
        padding: 24px;
      }

      .about-box {
        min-height: 280px;
        padding: 30px;
      }

      .contact-box {
        padding: 30px;
      }

      .contact-box h2 {
        font-size: 1.9rem;
      }

      .footer-content {
        flex-direction: column;
        align-items: flex-start;
      }
    }
  </style>
</head>

<body>

  <!-- Header -->
  <header>
    <div class="container nav">
      <a href="#home" class="logo">This is your website</a>

      <nav aria-label="Main navigation">
        <ul class="nav-links">
          <li><a href="#menu">Menu</a></li>
          <li><a href="#about">About</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main>

    <!-- Hero -->
    <section class="hero" id="home">
      <div class="container">
        <div class="hero-content">
          <div class="eyebrow">Good food. Good company.</div>

          <h1>
            Made with care,<br>
            served with <span>heart.</span>
          </h1>

          <p>
            Fresh ingredients, comforting flavors, and dishes made to bring
            people together. Discover something delicious today.
          </p>

          <a
            class="btn btn-primary"
            href="https://wa.me/YOUR_PHONE_NUMBER"
            target="_blank"
            rel="noopener noreferrer"
          >
            Order via WhatsApp
          </a>
        </div>
      </div>
    </section>

    <!-- Menu -->
    <section class="menu-section" id="menu">
      <div class="container">
        <div class="section-heading">
          <div class="eyebrow">Our menu</div>
          <h2>Simple food, thoughtfully made.</h2>
          <p>
            A selection of our favorite dishes, prepared fresh and served with
            attention to every detail.
          </p>
        </div>

        <div class="menu-grid">

          <article class="menu-card">
            <h3>Classic Beef Burger</h3>
            <p>
              Juicy grilled beef, fresh lettuce, tomato, onion, and our
              signature house sauce in a toasted bun.
            </p>
            <div class="price">$12.00</div>
          </article>

          <article class="menu-card">
            <h3>Margherita Pizza</h3>
            <p>
              A thin, crisp base topped with tomato, mozzarella, fresh basil,
              and a touch of extra virgin olive oil.
            </p>
            <div class="price">$14.00</div>
          </article>

          <article class="menu-card">
            <h3>Creamy Chicken Pasta</h3>
            <p>
              Tender chicken and pasta tossed in a rich, creamy garlic sauce
              with herbs and parmesan.
            </p>
            <div class="price">$15.00</div>
          </article>

          <article class="menu-card">
            <h3>Grilled Chicken Plate</h3>
            <p>
              Tender grilled chicken served with seasoned vegetables, fresh
              salad, and house-made sauce.
            </p>
            <div class="price">$16.00</div>
          </article>

          <article class="menu-card">
            <h3>Crispy Chicken Wings</h3>
            <p>
              Golden, crispy chicken wings seasoned with our special blend of
              herbs and spices, served with dip.
            </p>
            <div class="price">$11.00</div>
          </article>

          <article class="menu-card">
            <h3>Chocolate Dessert</h3>
            <p>
              A rich and smooth chocolate dessert finished with a light dusting
              of cocoa and served fresh.
            </p>
            <div class="price">$8.00</div>
          </article>

        </div>
      </div>
    </section>

    <!-- About -->
    <section id="about">
      <div class="container about-grid">

        <div>
          <div class="eyebrow">About us</div>
          <h2 class="about-title">
            Food that feels like home.
          </h2>

          <p class="about-text">
            We believe great food does not need to be complicated. Our kitchen
            focuses on quality ingredients, honest flavors, and generous
            portions.
          </p>

          <p class="about-text">
            Whether you're joining us for a quick meal or sharing dinner with
            family and friends, our goal is simple: make every visit worth
            remembering.
          </p>
        </div>

        <div class="about-box">
          <small>Our philosophy</small>
          <h3>Fresh ingredients.<br>Honest flavors.</h3>
        </div>

      </div>
    </section>

    <!-- Contact -->
    <section class="contact-section" id="contact">
      <div class="container">

        <div class="contact-box">
          <div>
            <div class="eyebrow">Get in touch</div>
            <h2>Ready to order?</h2>
            <p>
              Message us directly on WhatsApp and we'll be happy to help.
            </p>
          </div>

          <a
            class="btn btn-primary"
            href="https://wa.me/YOUR_PHONE_NUMBER"
            target="_blank"
            rel="noopener noreferrer"
          >
            Chat on WhatsApp
          </a>
        </div>

      </div>
    </section>

  </main>

  <!-- Footer -->
  <footer>
    <div class="container footer-content">
      <div class="footer-brand">This is your website</div>

      <p>
        Designed with care by Ayan Ahmad ·
        <span id="year"></span> All rights reserved.
      </p>
    </div>
  </footer>

  <script>
    // Automatically updates the copyright year.
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>

</body>
</html>

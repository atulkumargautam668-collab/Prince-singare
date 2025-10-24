<!doctype html>
<html lang="hi">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Meri Website</title>
  <style>
    :root{
      --accent:#2563EB; --bg:#f7f9fc; --card:#ffffff; --muted:#6b7280;
      font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    *{box-sizing:border-box}
    body{margin:0;background:var(--bg);color:#0f172a;line-height:1.5}
    header{background:linear-gradient(90deg, rgba(37,99,235,0.12), transparent);padding:18px 24px;backdrop-filter:blur(4px)}
    .container{max-width:1100px;margin:0 auto;padding:24px}
    nav{display:flex;align-items:center;justify-content:space-between;gap:16px}
    .brand{font-weight:700;color:var(--accent);font-size:1.1rem}
    .navlinks{display:flex;gap:12px}
    .navlinks a{text-decoration:none;color:var(--muted);font-weight:600}
    .hero{display:grid;grid-template-columns:1fr;gap:20px;align-items:center;padding:40px 0}
    .hero h1{font-size:2rem;margin:0 0 8px}
    .hero p{margin:0;color:var(--muted)}
    .btn{display:inline-block;padding:10px 16px;background:var(--accent);color:#fff;border-radius:8px;text-decoration:none;font-weight:600}
    .grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:16px;margin-top:24px}
    .card{background:var(--card);padding:18px;border-radius:12px;box-shadow:0 6px 18px rgba(15,23,42,0.06)}
    footer{padding:24px 0;color:var(--muted);font-size:0.95rem;text-align:center;margin-top:36px}
    form input, form textarea{width:100%;padding:10px;border:1px solid #e6eef8;border-radius:8px;margin-top:8px}
    @media(min-width:800px){ .hero{grid-template-columns:1fr 420px} .hero h1{font-size:2.4rem} }
  </style>
</head>
<body>
  <header>
    <div class="container">
      <nav>
        <div class="brand">MeriSite</div>
        <div class="navlinks">
          <a href="#features">Features</a>
          <a href="#pricing">Pricing</a>
          <a href="#contact">Contact</a>
        </div>
      </nav>
    </div>
  </header>

  <main class="container">
    <section class="hero">
      <div>
        <h1>Apni online maujoodgi shuru karo</h1>
        <p>Simple, tez aur responsive website — chhota business, portfolio ya personal blog ke liye perfect.</p>
        <div style="margin-top:16px">
          <a class="btn" href="#contact">Get Started</a>
        </div>

        <div id="features" class="grid" style="margin-top:28px">
          <div class="card">
            <h3>Responsive design</h3>
            <p style="color:var(--muted)">Mobile-first layout jo har device par achha dikhe.</p>
          </div>
          <div class="card">
            <h3>Fast & Lightweight</h3>
            <p style="color:var(--muted)">Minimal code for quick load times.</p>
          </div>
          <div class="card">
            <h3>Easy to customize</h3>
            <p style="color:var(--muted)">Colors, fonts aur content easily badal sakte ho.</p>
          </div>
        </div>
      </div>

      <aside class="card" style="padding:22px">
        <h2>Free consultation</h2>
        <p style="color:var(--muted)">Mujhe batao kya chahiye — main design aur hosting options bata dunga.</p>

        <form id="contact" style="margin-top:12px" onsubmit="event.preventDefault(); alert('Form demo — aap server side add kar sakte ho.');">
          <label>Naam</label>
          <input type="text" placeholder="Aapka naam" required>
          <label>Email</label>
          <input type="email" placeholder="name@example.com" required>
          <label>Message</label>
          <textarea rows="4" placeholder="Chhota sa message"></textarea>
          <div style="margin-top:12px">
            <button class="btn" type="submit">Send</button>
          </div>
        </form>
      </aside>
    </section>

    <section id="pricing" style="margin-top:32px">
      <h2>Pricing (example)</h2>
      <div class="grid" style="margin-top:12px">
        <div class="card">
          <h3>Basic</h3>
          <p style="color:var(--muted)">Single page, contact form, SEO basics.</p>
        </div>
        <div class="card">
          <h3>Pro</h3>
          <p style="color:var(--muted)">Multiple pages, blog, analytics integration.</p>
        </div>
        <div class="card">
          <h3>Custom</h3>
          <p style="color:var(--muted)">E-commerce, user accounts, integrations.</p>
        </div>
      </div>
    </section>

    <footer>
      © <span id="year"></span> MeriSite — Banaya gaya by you + helper.  
    </footer>
  </main>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>

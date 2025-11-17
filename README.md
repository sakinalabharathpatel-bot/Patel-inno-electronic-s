<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>My Simple Site</title>
  <meta name="description" content="A simple responsive starter website" />
  <style>
    /* Simple reset + layout */
    :root{ --accent:#1e88e5; --maxw:1100px; --radius:12px; font-family: Inter, system-ui, Arial; }
    *{box-sizing:border-box}
    body{margin:0;background:#f7f9fc;color:#111;line-height:1.5}
    header{background:linear-gradient(90deg,var(--accent),#5ab0ff);color:white;padding:28px 16px}
    .wrap{max-width:var(--maxw);margin:0 auto;padding:0 16px}
    nav{display:flex;gap:16px;align-items:center;justify-content:space-between}
    .brand{font-weight:700;font-size:1.2rem}
    .navlinks{display:flex;gap:12px}
    .navlinks a{color:rgba(255,255,255,0.95);text-decoration:none;padding:6px 10px;border-radius:8px}
    .hero{display:grid;grid-template-columns:1fr;gap:18px;align-items:center;padding:48px 0}
    h1{margin:0 0 8px;font-size:2rem}
    p.lead{margin:0;color:#e6f2ff}
    .card-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:16px;margin-top:24px}
    .card{background:white;padding:18px;border-radius:12px;box-shadow:0 6px 18px rgba(2,6,23,0.06)}
    footer{padding:24px 0;text-align:center;color:#6b7280;font-size:.95rem}
    /* responsive */
    @media(min-width:800px){
      .hero{grid-template-columns:1fr 420px}
      h1{font-size:2.4rem}
    }
    /* simple button */
    .btn{display:inline-block;background:white;color:var(--accent);padding:10px 14px;border-radius:10px;font-weight:600;text-decoration:none}
  </style>
</head>
<body>
  <header>
    <div class="wrap">
      <nav>
        <div class="brand">MySite</div>
        <div class="navlinks">
          <a href="#features">Features</a>
          <a href="#about">About</a>
          <a href="#contact">Contact</a>
        </div>
      </nav>

      <section class="hero">
        <div>
          <h1>Simple, fast website — made by you</h1>
          <p class="lead">A small, responsive starter site. Edit text, add images, and publish to GitHub Pages or Netlify.</p>
          <p style="margin-top:12px">
            <a class="btn" href="#contact">Get in touch</a>
          </p>
          <div class="card-grid" id="features">
            <div class="card"><strong>Fast</strong><div>Lightweight HTML + CSS</div></div>
            <div class="card"><strong>Responsive</strong><div>Looks good on phones & desktop</div></div>
            <div class="card"><strong>Extendable</strong><div>Add JavaScript or a CMS later</div></div>
          </div>
        </div>

        <aside>
          <div class="card">
            <h3 style="margin-top:0">About this starter</h3>
            <p style="margin:0">Copy this file, change the text and images, then host it online. Add more pages as needed.</p>
            <hr style="margin:12px 0"/>
            <div><strong>Skills used:</strong> HTML, CSS, responsive layout</div>
          </div>
        </aside>
      </section>
    </div>
  </header>

  <main class="wrap" id="about" style="padding:28px 16px;">
    <section class="card" style="margin-bottom:16px">
      <h2 style="margin-top:0">About</h2>
      <p>This is your site — change the content, add images, or connect a contact form service (Formspree, Netlify Forms) to receive messages.</p>
    </section>

    <section id="contact" class="card">
      <h2 style="margin-top:0">Contact</h2>
      <!-- Example static form (use a form backend to receive mails) -->
      <form action="#" onsubmit="alert('Form not configured — replace action with a form backend.'); return false;">
        <label style="display:block;margin-bottom:8px">Name<input required style="width:100%;padding:8px;margin-top:6px;border-radius:8px;border:1px solid #e6eef8" /></label>
        <label style="display:block;margin:12px 0 8px">Message<textarea required style="width:100%;padding:8px;border-radius:8px;border:1px solid #e6eef8" rows="5"></textarea></label>
        <button type="submit" class="btn" style="background:var(--accent);color:white;border:none">Send message</button>
      </form>
    </section>
  </main>

  <footer>
    <div class="wrap">
      © <span id="year"></span> MySite · Built with HTML & CSS
    </div>
  </footer>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();
    // Add small JS enhancements later
  </script>
</body>
</html>

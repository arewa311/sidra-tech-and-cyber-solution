<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>SIDRA Technology & Cyber Solution</title>
  <meta name="description" content="SIDRA Technology & Cyber Solution — cybersecurity, IT consulting, cloud, and managed services." />
  <meta name="color-scheme" content="light dark">
  <link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 64 64'%3E%3Cpath fill='%2300a3ff' d='M32 4l26 15v26L32 60 6 45V19z'/%3E%3Cpath fill='%23fff' d='M32 12l18 10v20L32 52 14 42V22z'/%3E%3Cpath fill='%2300a3ff' d='M24 26h16v12H24z'/%3E%3C/svg%3E" />
  <style>
    :root{
      --bg: #0b1020;      /* deep navy */
      --bg-soft:#11162a;
      --card:#0f1427;
      --text:#eaf2ff;
      --muted:#b7c4d6;
      --brand:#00a3ff;
      --accent:#58ffa6;
      --danger:#ff5d6c;
      --ring: 0 0 0 3px color-mix(in oklab, var(--brand), transparent 70%);
      --radius: 18px;
      --shadow: 0 10px 30px rgba(0,0,0,.35), 0 2px 8px rgba(0,0,0,.2);
    }
    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{
      margin:0; font: 16px/1.6 system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, Inter, "Noto Sans", Arial, sans-serif;
      color:var(--text); background: radial-gradient(1200px 800px at 10% -10%, #152046 0%, transparent 60%),
                         radial-gradient(1200px 800px at 100% 0%, #0d1a33 0%, transparent 55%),
                         var(--bg);
    }
    a{color:var(--brand); text-decoration:none}
    a:hover{text-decoration:underline}
    .container{width:min(1200px, 92%); margin:auto}
    header{
      position:sticky; top:0; z-index:50; backdrop-filter: blur(10px);
      background: color-mix(in oklab, var(--bg), black 8% / 30%);
      border-bottom: 1px solid color-mix(in oklab, var(--brand), transparent 82%);
    }
    .nav{display:flex; align-items:center; justify-content:space-between; padding:.8rem 0}
    .brand{display:flex; align-items:center; gap:.6rem; font-weight:800; letter-spacing:.3px}
    .brand svg{width:28px; height:28px}
    nav ul{display:flex; gap:1rem; list-style:none; padding:0; margin:0}
    nav a{display:block; padding:.6rem .8rem; border-radius:999px}
    nav a:hover{background: color-mix(in oklab, var(--brand), transparent 90%)}
    .cta{display:inline-flex; align-items:center; gap:.5rem; background:linear-gradient(135deg, var(--brand), #4fd1ff); color:#00111d; font-weight:700; padding:.7rem 1rem; border-radius:999px; box-shadow:var(--shadow)}
    .cta:hover{filter:saturate(1.1)}
    .menu-btn{display:none; background:none; border:1px solid color-mix(in oklab, var(--brand), transparent 75%); padding:.4rem .7rem; border-radius:12px; color:var(--text)}

    /* Hero */
    .hero{padding: clamp(3rem, 8vw, 7rem) 0; position:relative; overflow:hidden}
    .hero-grid{display:grid; grid-template-columns: 1.1fr .9fr; gap:2rem; align-items:center}
    .kicker{color:var(--accent); font-weight:700; text-transform:uppercase; letter-spacing:.15em; font-size:.85rem}
    h1{font-size: clamp(2rem, 4.5vw, 3.4rem); line-height:1.15; margin:.4rem 0 1rem}
    .lead{color:var(--muted); font-size: clamp(1rem, 1.2vw, 1.15rem)}
    .hero-cards{display:grid; gap:1rem; grid-template-columns:repeat(2, 1fr)}
    .card{background:linear-gradient(180deg, color-mix(in oklab, var(--card), black 10%), var(--card)); border:1px solid color-mix(in oklab, var(--brand), transparent 80%); border-radius:var(--radius); padding:1.2rem; box-shadow:var(--shadow)}
    .card h3{margin:.2rem 0 .4rem; font-size:1.05rem}
    .pill{display:inline-flex; align-items:center; gap:.4rem; font-size:.8rem; padding:.35rem .6rem; border-radius:999px; border:1px solid color-mix(in oklab, var(--accent), transparent 70%); color:var(--accent)}

    /* Sections */
    section{padding: clamp(2.5rem, 6vw, 4rem) 0}
    .section-title{font-size: clamp(1.4rem, 2.4vw, 2rem); margin:0 0 1rem}
    .muted{color:var(--muted)}

    /* Services */
    .grid{display:grid; gap:1rem}
    .grid-3{grid-template-columns: repeat(3, 1fr)}
    .grid-4{grid-template-columns: repeat(4, 1fr)}
    .service{padding:1.1rem}
    .service svg{width:28px; height:28px}

    /* Showcase */
    .showcase{display:grid; grid-template-columns:1.2fr .8fr; gap:1rem}
    .panel{min-height:280px; border-radius:var(--radius); background:linear-gradient(180deg, #0a1730, #0b2042); border:1px solid color-mix(in oklab, var(--brand), transparent 80%); padding:1.2rem; position:relative; overflow:hidden}
    .panel pre{white-space:pre-wrap; font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", monospace; color:#d7e8ff; background:#071226; padding:1rem; border-radius:14px; border:1px solid #122349}

    /* Pricing */
    .pricing{display:grid; grid-template-columns: repeat(3, 1fr); gap:1rem}
    .price-card{padding:1.2rem; border-radius:var(--radius); border:1px solid color-mix(in oklab, var(--brand), transparent 80%); background:linear-gradient(180deg, var(--card), #0b142d)}
    .price{font-size:2rem; font-weight:800}
    .badge{font-size:.75rem; padding:.3rem .5rem; border-radius:8px; border:1px solid color-mix(in oklab, var(--brand), transparent 60%); color:var(--brand)}
    .features{margin:.8rem 0 0; padding:0; list-style:none}
    .features li{margin:.35rem 0}

    /* Footer */
    footer{padding:2rem 0; border-top:1px solid color-mix(in oklab, var(--brand), transparent 82%); color:var(--muted)}

    /* Forms */
    input, textarea, select, button{
      font:inherit; color:inherit; background:#0a142a; border:1px solid color-mix(in oklab, var(--brand), transparent 75%); border-radius:12px; padding:.7rem .9rem; width:100%
    }
    input:focus, textarea:focus, select:focus{outline:none; box-shadow: var(--ring); border-color: var(--brand)}
    button{cursor:pointer; width:auto}

    /* Responsive */
    @media (max-width: 980px){
      .hero-grid{grid-template-columns:1fr}
      .showcase{grid-template-columns:1fr}
      .grid-3{grid-template-columns:1fr}
      .grid-4{grid-template-columns:1fr 1fr}
      .pricing{grid-template-columns:1fr}
      nav ul{display:none}
      .menu-btn{display:inline-flex}
      .mobile-open nav ul{display:flex; flex-direction:column; gap:.25rem; position:absolute; right:4%; top:60px; background:var(--bg-soft); border:1px solid color-mix(in oklab, var(--brand), transparent 80%); padding:.6rem; border-radius:14px}
    }
  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <div class="brand" aria-label="SIDRA home">
        <svg viewBox="0 0 64 64" aria-hidden="true" role="img"><path fill="var(--brand)" d="M32 4l26 15v26L32 60 6 45V19z"/><path fill="#fff" d="M32 12l18 10v20L32 52 14 42V22z"/><path fill="var(--brand)" d="M24 26h16v12H24z"/></svg>
        <span>S I D R A</span>
      </div>
      <button class="menu-btn" id="menuBtn" aria-expanded="false" aria-controls="primaryNav">Menu</button>
      <nav id="primaryNav" aria-label="Primary">
        <ul>
          <li><a href="#services">Services</a></li>
          <li><a href="#solutions">Solutions</a></li>
          <li><a href="#about">About</a></li>
          <li><a href="#pricing">Pricing</a></li>
          <li><a href="#contact" class="cta">Get a Quote</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main>
    <!-- HERO -->
    <section class="hero">
      <div class="container hero-grid">
        <div>
          <div class="pill" aria-hidden="true">ISO‑minded • SOC‑Ready • Cloud‑Native</div>
          <p class="kicker" style="margin-top:1rem">SIDRA TECHNOLOGY & CYBER SOLUTION</p>
          <h1>Secure. Scalable. Simple.<br>We harden your business for tomorrow.</h1>
          <p class="lead">We deliver end‑to‑end cybersecurity, modern IT, and cloud operations for SMEs, fintech, schools, and public sector teams. From risk assessments to 24/7 monitoring—we’ve got you covered.</p>
          <p style="margin-top:1rem; display:flex; gap:.6rem; flex-wrap:wrap">
            <a class="cta" href="#contact">Start a Project</a>
            <a class="pill" href="#showcase" aria-label="See how we work">See our work →</a>
          </p>
        </div>
        <div class="hero-cards">
          <article class="card service" aria-label="Managed SOC">
            <div class="pill" style="border-color:color-mix(in oklab, var(--brand), transparent 60%); color:var(--brand)">Managed SOC</div>
            <h3>24/7 Threat Monitoring</h3>
            <p class="muted">SIEM/SOAR setup, alert triage, and rapid response playbooks tailored to your stack.</p>
          </article>
          <article class="card service" aria-label="Cloud Security">
            <div class="pill">Cloud Security</div>
            <h3>Azure • AWS • GCP</h3>
            <p class="muted">Least‑privilege IAM, guardrails, posture management, and cost optimization.</p>
          </article>
          <article class="card service" aria-label="Compliance">
            <div class="pill">Compliance</div>
            <h3>ISO 27001 • NDPR • PCI</h3>
            <p class="muted">Policies, risk registers, training, and audit readiness without the headaches.</p>
          </article>
          <article class="card service" aria-label="IT Support">
            <div class="pill">IT Support</div>
            <h3>Modern Workplace</h3>
            <p class="muted">Device management, secure Wi‑Fi, backups, and friendly support your team will love.</p>
          </article>
        </div>
      </div>
    </section>

    <!-- SERVICES -->
    <section id="services">
      <div class="container">
        <h2 class="section-title">Core Services</h2>
        <p class="muted">Pick a single service or mix‑and‑match into a managed package.</p>
        <div class="grid grid-4" style="margin-top:1rem">
          <article class="card service">
            <svg viewBox="0 0 24 24" aria-hidden="true"><path fill="currentColor" d="M12 1l9 5v6c0 5-4 9-9 11C7 21 3 17 3 12V6l9-5zm0 3L6 7v5c0 3.9 2.9 7.2 6 8.9 3.1-1.7 6-5 6-8.9V7l-6-3z"/></svg>
            <h3>Penetration Testing</h3>
            <p class="muted">Network, web, and mobile testing with clear, prioritized fixes.</p>
          </article>
          <article class="card service">
            <svg viewBox="0 0 24 24" aria-hidden="true"><path fill="currentColor" d="M4 4h16v4H4zm0 6h10v4H4zm0 6h16v4H4z"/></svg>
            <h3>Security Operations</h3>
            <p class="muted">SIEM tuning, log pipelines, detection engineering, and IR retainers.</p>
          </article>
          <article class="card service">
            <svg viewBox="0 0 24 24" aria-hidden="true"><path fill="currentColor" d="M12 2a7 7 0 100 14 7 7 0 000-14zm0 16c-5 0-9 2.2-9 5v1h18v-1c0-2.8-4-5-9-5z"/></svg>
            <h3>Managed IT</h3>
            <p class="muted">Endpoint management, patching, backups, and helpdesk SLAs.</p>
          </article>
          <article class="card service">
            <svg viewBox="0 0 24 24" aria-hidden="true"><path fill="currentColor" d="M12 3l9 4v4c0 5-4 9-9 10C7 20 3 16 3 11V7l9-4zm0 4L6 9v2c0 3.4 2.7 6.3 6 7.7 3.3-1.4 6-4.3 6-7.7V9l-6-2z"/></svg>
            <h3>Training & Awareness</h3>
            <p class="muted">Phishing simulations and workshops for leadership and staff.</p>
          </article>
        </div>
      </div>
    </section>

    <!-- SOLUTIONS / SHOWCASE -->
    <section id="solutions">
      <div class="container">
        <h2 class="section-title">Solutions We Deploy</h2>
        <p class="muted">Best‑practice reference architectures, ready to tailor to your environment.</p>
        <div id="showcase" class="showcase" style="margin-top:1rem">
          <div class="panel">
            <h3>Zero Trust Network Access</h3>
            <p class="muted">Identity‑aware access with device posture checks and just‑in‑time permissions.</p>
            <pre aria-label="Zero Trust snippet">policy "finance-app" {
  subject.roles  = ["employee", "finance"]
  device.posture = compliant
  access         = allow if within("9:00-18:00", tz="Africa/Lagos")
}</pre>
          </div>
          <div class="panel">
            <h3>Backup & Recovery</h3>
            <p class="muted">Immutable backups, 3‑2‑1 rule, and 1‑hour RTO for business‑critical systems.</p>
            <pre aria-label="Backup plan snippet">backup_plan:
  schedule: daily 22:00 WAT
  retention: 30d
  replicas:
    - local encrypted
    - cloud (immutable)
  test: quarterly disaster‑recovery drill</pre>
          </div>
        </div>
      </div>
    </section>

    <!-- ABOUT -->
    <section id="about">
      <div class="container">
        <h2 class="section-title">About SIDRA</h2>
        <div class="grid grid-3" style="margin-top:1rem">
          <article class="card">
            <h3>Mission</h3>
            <p class="muted">Enable African businesses to grow with confidence by making security simple, affordable, and continuous.</p>
          </article>
          <article class="card">
            <h3>Approach</h3>
            <p class="muted">Assess → Secure → Operate. We map risks, deploy controls, and stay to run them with you.</p>
          </article>
          <article class="card">
            <h3>Footprint</h3>
            <p class="muted">HQ in Kano, projects across Nigeria and West Africa. Remote‑first delivery with on‑site options.</p>
          </article>
        </div>
      </div>
    </section>

    <!-- PRICING -->
    <section id="pricing">
      <div class="container">
        <h2 class="section-title">Simple Pricing</h2>
        <p class="muted">Transparent monthly plans. Custom quotes for enterprise and public sector.</p>
        <div class="pricing" style="margin-top:1rem">
          <article class="price-card">
            <div class="badge">Starter</div>
            <h3>Essentials</h3>
            <p class="price">₦149k<span class="muted" style="font-size:.9rem">/mo</span></p>
            <ul class="features">
              <li>Helpdesk (8×5)</li>
              <li>Endpoint protection</li>
              <li>Backup basic (1TB)</li>
            </ul>
            <p style="margin-top:1rem"><a href="#contact" class="cta">Choose Essentials</a></p>
          </article>
          <article class="price-card" style="border:2px solid var(--brand)">
            <div class="badge">Most Popular</div>
            <h3>Business</h3>
            <p class="price">₦349k<span class="muted" style="font-size:.9rem">/mo</span></p>
            <ul class="features">
              <li>Helpdesk (12×5)</li>
              <li>SIEM lite + alerts</li>
              <li>Cloud security review</li>
              <li>Backup pro (3TB)</li>
            </ul>
            <p style="margin-top:1rem"><a href="#contact" class="cta">Choose Business</a></p>
          </article>
          <article class="price-card">
            <div class="badge">Custom</div>
            <h3>Enterprise</h3>
            <p class="price">Let's talk</p>
            <ul class="features">
              <li>24/7 SOC & IR</li>
              <li>Compliance program</li>
              <li>On‑site support</li>
            </ul>
            <p style="margin-top:1rem"><a href="#contact" class="cta">Request Quote</a></p>
          </article>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact">
      <div class="container">
        <h2 class="section-title">Contact Us</h2>
        <p class="muted">Tell us a bit about your needs. We’ll respond within one business day.</p>
        <div class="grid" style="grid-template-columns: 1fr 1fr; gap:1rem; margin-top:1rem">
          <form class="card" id="contactForm" novalidate>
            <div class="grid" style="grid-template-columns:1fr 1fr; gap:.8rem">
              <p>
                <label for="name">Full Name</label><br>
                <input id="name" name="name" required placeholder="Jane Doe" />
              </p>
              <p>
                <label for="email">Email</label><br>
                <input id="email" name="email" type="email" required placeholder="jane@example.com" />
              </p>
            </div>
            <div class="grid" style="grid-template-columns:1fr 1fr; gap:.8rem">
              <p>
                <label for="phone">Phone/WhatsApp</label><br>
                <input id="phone" name="phone" placeholder="+234 800 000 0000" />
              </p>
              <p>
                <label for="company">Company</label><br>
                <input id="company" name="company" placeholder="Your Company Ltd" />
              </p>
            </div>
            <p>
              <label for="service">Interested In</label><br>
              <select id="service" name="service" required>
                <option value="">Select a service…</option>
                <option>Penetration Testing</option>
                <option>Managed SOC</option>
                <option>Cloud Security</option>
                <option>Managed IT</option>
                <option>Training & Awareness</option>
              </select>
            </p>
            <p>
              <label for="message">Message</label><br>
              <textarea id="message" name="message" rows="5" placeholder="Tell us about your project…" required></textarea>
            </p>
            <div style="display:flex; gap:.6rem; align-items:center; flex-wrap:wrap">
              <button class="cta" type="submit">Send Message</button>
              <span id="formNote" class="muted" aria-live="polite"></span>
            </div>
          </form>
          <aside class="card" aria-label="Company details">
            <h3>SIDRA Technology & Cyber Solution</h3>
            <p class="muted">Kano, Nigeria • Remote & On‑site</p>
            <p>Email: <a href="mailto:hello@sidratech.ng">hello@sidratech.ng</a><br>
               Phone: <a href="tel:+2348000000000">+234 800 000 0000</a></p>
            <hr style="border-color: color-mix(in oklab, var(--brand), transparent 70%)">
            <p class="muted">Business Hours: Mon–Fri, 9:00–17:00 WAT</p>
            <p class="muted">Follow: <a href="#">LinkedIn</a> • <a href="#">Twitter/X</a>
          </aside>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container" style="display:flex; gap:1rem; justify-content:space-between; align-items:center; flex-wrap:wrap">
      <p>© <span id="yyyy"></span> SIDRA Technology & Cyber Solution. All rights reserved.</p>
      <p><a href="#" id="toTop">Back to top ↑</a></p>
    </div>
  </footer>

  <script>
    // Mobile menu toggle
    const body = document.body;
    const btn  = document.getElementById('menuBtn');
    btn?.addEventListener('click', () => {
      const open = body.classList.toggle('mobile-open');
      btn.setAttribute('aria-expanded', open ? 'true' : 'false');
    });

    // Simple form validation (no backend)
    const form = document.getElementById('contactForm');
    const note = document.getElementById('formNote');
    form?.addEventListener('submit', (e) => {
      e.preventDefault();
      if (!form.checkValidity()){
        note.textContent = 'Please complete the required fields.';
        note.style.color = getComputedStyle(document.documentElement).getPropertyValue('--danger');
        form.reportValidity();
        return;
      }
      note.textContent = 'Thanks! Your message is ready to send. Replace the form handler with your email/API.';
      note.style.color = getComputedStyle(document.documentElement).getPropertyValue('--accent');
    });

    // Back to top + year
    document.getElementById('toTop')?.addEventListener('click', (e)=>{
      e.preventDefault(); window.scrollTo({top:0, behavior:'smooth'});
    });
    document.getElementById('yyyy').textContent = new Date().getFullYear();
  </script>
</body>
</html>

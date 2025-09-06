<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Vikas Bhamore — Full Stack Developer</title>
  <meta name="description" content="Personal portfolio of Vikas Bhamore — Full Stack Developer. Projects, skills and contact."/>
  <style>
    :root{
      --bg:#0f1724; --card:#0b1220; --muted:#9aa4b2; --accent:#06b6d4; --glass: rgba(255,255,255,0.04);
      --radius:14px; --maxw:1100px; --ff: Inter, ui-sans-serif, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;padding:0;font-family:var(--ff);background:linear-gradient(180deg,#071029 0%,var(--bg) 100%);color:#e6eef6;line-height:1.5;-webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;display:flex;justify-content:center;padding:32px 18px;
    }
    .wrap{width:100%;max-width:var(--maxw)}

    /* header */
    header{display:flex;align-items:center;justify-content:space-between;margin-bottom:26px}
    .brand{display:flex;gap:14px;align-items:center}
    .logo{width:52px;height:52px;border-radius:12px;background:linear-gradient(135deg,var(--accent),#7c3aed);display:flex;align-items:center;justify-content:center;font-weight:700}
    .logo span{font-size:20px}
    .nav{display:flex;gap:14px;align-items:center}
    .nav a{color:var(--muted);text-decoration:none;padding:8px 10px;border-radius:8px}
    .nav a:hover{background:var(--glass);color:#fff}
    .cta{background:transparent;border:1px solid rgba(255,255,255,0.06);padding:8px 12px;border-radius:10px;color:var(--muted)}

    /* hero */
    .hero{display:grid;grid-template-columns:1fr 380px;gap:28px;align-items:center;margin-bottom:28px}
    @media (max-width:920px){.hero{grid-template-columns:1fr}}
    .card{background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);padding:28px;border-radius:var(--radius);box-shadow:0 6px 30px rgba(2,6,23,0.6)}
    h1{margin:0 0 8px;font-size:28px}
    p.lead{color:var(--muted);margin-top:0}
    .hero .actions{margin-top:18px;display:flex;gap:12px}
    .btn{background:var(--accent);color:#06202a;padding:10px 14px;border-radius:10px;text-decoration:none;font-weight:600}
    .btn.secondary{background:transparent;border:1px solid rgba(255,255,255,0.06);color:var(--muted)}

    /* skills */
    .skills{display:flex;flex-wrap:wrap;gap:8px;margin-top:16px}
    .skill{background:rgba(255,255,255,0.03);padding:8px 10px;border-radius:10px;color:var(--muted);font-size:14px}

    /* right column -- profile */
    .profile{display:flex;flex-direction:column;align-items:center;text-align:center;gap:12px}
    .avatar{width:140px;height:140px;border-radius:20px;background:linear-gradient(135deg,#153c4b,#042f2f);display:flex;align-items:center;justify-content:center;font-size:44px}
    .profile .meta{color:var(--muted)}

    /* projects grid */
    .section{margin-bottom:26px}
    .section h2{margin:0 0 14px}
    .projects{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}
    @media (max-width:980px){.projects{grid-template-columns:repeat(2,1fr)}}
    @media (max-width:640px){.projects{grid-template-columns:1fr}}
    .project{background:linear-gradient(90deg, rgba(255,255,255,0.02), transparent);padding:16px;border-radius:12px;border:1px solid rgba(255,255,255,0.03)}
    .project h3{margin:0 0 8px;font-size:16px}
    .project p{margin:0;color:var(--muted);font-size:14px}
    .project .tags{margin-top:10px;display:flex;gap:8px;flex-wrap:wrap}
    .tag{background:rgba(255,255,255,0.03);padding:6px 8px;border-radius:8px;font-size:12px;color:var(--muted)}
    .links{margin-top:12px;display:flex;gap:10px}
    .links a{font-size:14px;color:var(--muted);text-decoration:none}

    /* footer/contact */
    .contact-grid{display:grid;grid-template-columns:1fr 1fr;gap:16px}
    @media (max-width:720px){.contact-grid{grid-template-columns:1fr}}
    label{display:block;font-size:13px;color:var(--muted);margin-bottom:6px}
    input,textarea{width:100%;padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit}
    textarea{min-height:110px}

    footer{margin-top:18px;color:var(--muted);font-size:14px;text-align:center}

    /* small utilities */
    .small{font-size:13px;color:var(--muted)}
    .flex{display:flex;align-items:center}
    .space{flex:1}

    /* mobile nav */
    .mobile-toggle{display:none}
    @media (max-width:720px){.nav{display:none}.mobile-toggle{display:block}}

    /* subtle animations */
    .fade-up{transform:translateY(10px);opacity:0;transition:all 420ms ease;}
    .fade-up.show{transform:none;opacity:1}
    .project:hover{transform:translateY(-6px);transition:transform 180ms ease}

    /* accessibility focus */
    a:focus,button:focus,input:focus,textarea:focus{outline:2px solid rgba(6,182,212,0.18);outline-offset:2px}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="brand">
        <div class="logo" aria-hidden="true"><span>VB</span></div>
        <div>
          <div style="font-weight:700">Vikas Bhamore</div>
          <div class="small">Full Stack Developer</div>
        </div>
      </div>

      <nav class="nav" aria-label="Main navigation">
        <a href="#about">About</a>
        <a href="#projects">Projects</a>
        <a href="#skills">Skills</a>
        <a href="#contact">Contact</a>
        <a class="cta" href="mailto:vikas@example.com">Hire Me</a>
      </nav>

      <button class="mobile-toggle" aria-label="open menu" onclick="toggleNav()">☰</button>
    </header>

    <main>
      <section class="hero">
        <div class="card fade-up show">
          <h1>Hi, I'm <span style="color:var(--accent)">Vikas</span> — a Full Stack Developer</h1>
          <p class="lead">I build web applications, dashboards, and APIs. I love turning ideas into clean, maintainable code that scales.</p>

          <div class="skills" aria-hidden="true">
            <div class="skill">HTML</div>
            <div class="skill">CSS</div>
            <div class="skill">JavaScript</div>
            <div class="skill">React</div>
            <div class="skill">Node.js</div>
            <div class="skill">MongoDB</div>
          </div>

          <div class="actions">
            <a class="btn" href="#projects">View Projects</a>
            <a class="btn secondary" href="#contact">Contact</a>
          </div>

          <p class="small" style="margin-top:14px">Available for internships & freelance projects. Based in India.</p>
        </div>

        <aside class="profile card fade-up show" style="align-self:start">
          <div class="avatar">VB</div>
          <div style="font-weight:700">Vikas Bhamore</div>
          <div class="meta">Full Stack Developer</div>
          <div class="small">5'11" • Open to internships • vegetarian</div>

          <div style="margin-top:12px;display:flex;gap:8px">
            <a class="small" href="https://github.com/" target="_blank" rel="noopener">GitHub</a>
            <a class="small" href="https://www.linkedin.com/" target="_blank" rel="noopener">LinkedIn</a>
          </div>
        </aside>
      </section>

      <section id="about" class="section">
        <div class="card fade-up show">
          <h2>About Me</h2>
          <p class="small">I'm a BCA student focusing on web development and freelancing. I enjoy building end-to-end applications using the MERN stack. I solve problems, write clean code, and constantly learn new tools and frameworks.</p>
        </div>
      </section>

      <section id="projects" class="section">
        <h2>Projects</h2>
        <div class="projects">
          <article class="project">
            <h3>Portfolio Website</h3>
            <p>Personal portfolio to showcase projects and get clients.</p>
            <div class="tags"><span class="tag">HTML</span><span class="tag">CSS</span><span class="tag">JS</span></div>
            <div class="links"><a href="#" onclick="openDemo(event,'Portfolio Website','A single-file portfolio built with HTML/CSS/JS. Hosted on Netlify/Vercel.')">Details</a> · <a href="#">Source</a></div>
          </article>

          <article class="project">
            <h3>Blog Platform</h3>
            <p>Users can sign up, create posts, and comment.</p>
            <div class="tags"><span class="tag">React</span><span class="tag">Node</span><span class="tag">MongoDB</span></div>
            <div class="links"><a href="#" onclick="openDemo(event,'Blog Platform','MERN app with authentication and CRUD operations.')">Details</a> · <a href="#">Source</a></div>
          </article>

          <article class="project">
            <h3>E‑commerce Store</h3>
            <p>Product listing, cart, and checkout simulation.</p>
            <div class="tags"><span class="tag">React</span><span class="tag">Express</span><span class="tag">Stripe</span></div>
            <div class="links"><a href="#" onclick="openDemo(event,'E‑commerce Store','Store with product pages, cart and order summary. Integration-ready for payment gateways.')">Details</a> · <a href="#">Source</a></div>
          </article>

          <article class="project">
            <h3>Chat App</h3>
            <p>Realtime messaging using WebSockets.</p>
            <div class="tags"><span class="tag">Socket.io</span><span class="tag">Node</span><span class="tag">React</span></div>
            <div class="links"><a href="#" onclick="openDemo(event,'Chat App','Realtime chat with rooms and online presence.')">Details</a> · <a href="#">Source</a></div>
          </article>

          <article class="project">
            <h3>Quiz System</h3>
            <p>Admin panel to add questions and users to attempt quizzes.</p>
            <div class="tags"><span class="tag">React</span><span class="tag">MySQL</span></div>
            <div class="links"><a href="#" onclick="openDemo(event,'Quiz System','Admin and user flows with scoring and timers.')">Details</a> · <a href="#">Source</a></div>
          </article>

          <article class="project">
            <h3>Expense Tracker</h3>
            <p>Track expenses and view charts.</p>
            <div class="tags"><span class="tag">React</span><span class="tag">Chart.js</span></div>
            <div class="links"><a href="#" onclick="openDemo(event,'Expense Tracker','Add/remove expenses and view monthly charts.')">Details</a> · <a href="#">Source</a></div>
          </article>

        </div>
      </section>

      <section id="skills" class="section">
        <div class="card">
          <h2>Skills</h2>
          <div style="display:flex;gap:20px;flex-wrap:wrap;margin-top:12px">
            <div style="min-width:220px">
              <strong>Frontend</strong>
              <div class="small">HTML, CSS, JavaScript, React, Next.js (learning), Tailwind</div>
            </div>
            <div style="min-width:220px">
              <strong>Backend & DB</strong>
              <div class="small">Node.js, Express, MongoDB, MySQL, REST APIs</div>
            </div>
            <div style="min-width:220px">
              <strong>Tools</strong>
              <div class="small">Git, GitHub, Docker (basic), Vercel/Heroku</div>
            </div>
          </div>
        </div>
      </section>

      <section id="contact" class="section">
        <h2>Contact</h2>
        <div class="contact-grid">
          <form class="card" onsubmit="sendMessage(event)">
            <label for="name">Name</label>
            <input id="name" name="name" required />
            <label for="email">Email</label>
            <input id="email" name="email" type="email" required />
            <label for="message">Message</label>
            <textarea id="message" name="message" required></textarea>
            <div style="display:flex;gap:8px;margin-top:12px">
              <button class="btn" type="submit">Send</button>
              <button type="button" class="btn secondary" onclick="location.href='mailto:vikas@example.com'">Email Me</button>
            </div>
            <div id="formResult" class="small" style="margin-top:10px;color:var(--muted)"></div>
          </form>

          <div class="card">
            <h3>Get in touch</h3>
            <p class="small">Feel free to reach out for internships, freelance work or collaborations.</p>
            <p class="small"><strong>Email:</strong> vikas@example.com</p>
            <p class="small"><strong>Location:</strong> Bhopal, India</p>

            <div style="margin-top:10px">
              <a href="#" class="small">GitHub</a> · <a href="#" class="small">LinkedIn</a> · <a href="#" class="small">Resume</a>
            </div>
          </div>
        </div>
      </section>

      <footer>
        Built with ❤️ by Vikas • © <span id="year"></span>
      </footer>
    </main>
  </div>

  <script>
    // small utilities: mobile nav
    function toggleNav(){
      const nav=document.querySelector('.nav');
      if(nav.style.display==='flex'){nav.style.display='none';return}
      nav.style.display='flex';nav.style.flexDirection='column';nav.style.position='absolute';nav.style.right='18px';nav.style.top='80px';nav.style.background='var(--card)';nav.style.padding='12px';nav.style.borderRadius='12px';
    }

    // Demo modal (simple) — reuses browser alert for simplicity; you can replace with a modal
    function openDemo(e,title,desc){
      e.preventDefault();
      alert(title + '\n\n' + desc);
    }

    // form handler — this uses mailto fallback if no backend is configured
    function sendMessage(e){
      e.preventDefault();
      const name=document.getElementById('name').value.trim();
      const email=document.getElementById('email').value.trim();
      const message=document.getElementById('message').value.trim();
      const out=document.getElementById('formResult');
      if(!name || !email || !message){out.textContent='Please fill all fields.';return}
      // create mailto link so user can send from their email client
      const subject = encodeURIComponent('Portfolio message from ' + name);
      const body = encodeURIComponent('Name: '+name+'\nEmail: '+email+'\n\n'+message);
      const mailto = `mailto:vikas@example.com?subject=${subject}&body=${body}`;
      // open user's mail client
      window.location.href = mailto;
      out.textContent = 'Opening your email client...';
    }

    // small animation reveal
    document.addEventListener('DOMContentLoaded',()=>{
      document.querySelectorAll('.fade-up').forEach((el,i)=>{
        setTimeout(()=>el.classList.add('show'), 80*i);
      });
      document.getElementById('year').textContent = new Date().getFullYear();
    });
  </script>
</body>
</html>

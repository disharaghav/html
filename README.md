<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Disha Raghav — Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg: #0f1724;
      --card: #0b1220;
      --muted: #9aa4b2;
      --accent: #7c5cff;
      --accent-2: #27b6ff;
      --glass: rgba(255,255,255,0.03);
      --radius: 1rem;
      --max-width: 1100px;
      font-size: 16px;
      color-scheme: dark;
    }
    *{ box-sizing:border-box; }
    body{
      margin:0;
      font-family:"Inter",sans-serif;
      background: linear-gradient(180deg,#071025,#0b1422);
      color:#e6eef8;
    }

    .container{
      width:clamp(90%,90%,var(--max-width));
      max-width:var(--max-width);
      margin:0 auto;
      padding:2rem 0;
    }

    
    .site-header{
      position:sticky; top:0; z-index:20;
      backdrop-filter:blur(6px);
      background:rgba(7,10,20,0.4);
      border-bottom:1px solid rgba(255,255,255,0.05);
    }
    .header-inner{
      display:flex; justify-content:space-between;
      align-items:center; padding:0.8rem 0;
    }
    .logo{ font-weight:700; }
    .nav{ display:flex; gap:1rem; }
    .nav a{
      color:var(--muted); text-decoration:none;
      padding:0.35rem 0.6rem;
      border-radius:8px;
      transition:0.25s;
      font-weight:600;
    }
    .nav a:hover{
      color:white;
      background:rgba(255,255,255,0.05);
      transform:translateY(-2px);
    }

    .cta{
      background:linear-gradient(90deg,var(--accent),var(--accent-2));
      padding:0.55rem 0.9rem;
      color:white;
      font-weight:600;
      border:0;
      border-radius:12px;
      cursor:pointer;
      transition:0.2s;
    }
    .cta:hover{ transform:translateY(-3px); }

    
    .hero{ padding:3rem 0; }
    .hero-inner{
      display:flex;
      flex-direction:column;
      gap:2rem;
      align-items:center;
    }
    .hero-content{ text-align:center; max-width:55ch; }
    .hero-content h1{
      font-size:clamp(1.6rem,4vw,3rem);
      margin:0;
    }
    .role{ margin:0.5rem 0 1rem 0; color:var(--muted); }
    .lead{ color:var(--muted); margin-bottom:1.1rem; }

    .highlighted-role{
      animation:colorShift 6s linear infinite;
      padding:0.2rem 0.4rem;
      border-radius:6px;
      font-weight:700;
    }

    .hero-image img{
      width:280px;
      border-radius:1rem;
      border:1px solid rgba(255,255,255,0.05);
      box-shadow:0 10px 35px rgba(2,6,23,0.6);
    }

    
    .btn{
      text-decoration:none;
      display:inline-block;
      padding:0.6rem 0.9rem;
      border-radius:10px;
      font-weight:600;
      transition:0.2s;
    }
    .btn:hover{ transform:translateY(-3px); }

    .primary{
      background:linear-gradient(90deg,var(--accent),var(--accent-2));
      color:white;
    }
    .ghost{
      border:1px solid rgba(255,255,255,0.05);
      color:var(--muted);
    }
    .hero-actions{
      display:flex;
      gap:0.75rem;
      justify-content:center;
    }

    
    .section-title{
      font-size:1.4rem;
      margin-bottom:1rem;
    }
    .about-grid{
      display:grid;
      grid-template-columns:1fr;
      gap:1.5rem;
    }
    .about-text p{ color:var(--muted); }
    .about-list{
      list-style:none; padding:0; color:var(--muted);
    }

    .about-stats{
      display:flex; gap:1rem;
      justify-content:space-between;
    }
    .stat{
      background:var(--glass);
      padding:1rem;
      border-radius:0.8rem;
      text-align:center;
    }
    .stat-num{ font-size:1.3rem; font-weight:700; }

   
    .skills-grid{
      display:grid;
      grid-template-columns:repeat(2,1fr);
      gap:1rem;
    }
    .card{
      background:rgba(255,255,255,0.03);
      padding:1rem;
      border-radius:0.8rem;
      transition:0.25s;
    }
    .card:hover{
      transform:translateY(-5px);
      box-shadow:0 20px 40px rgba(0,0,0,0.5);
    }

    
    .projects-grid{
      display:grid;
      grid-template-columns:1fr;
      gap:1rem;
    }
    .project img{
      width:100%;
      border-radius:0.7rem;
    }

    .project-body{ margin-top:0.5rem; }
    .project-tags{
      display:flex; gap:0.5rem;
      flex-wrap:wrap;
      margin-top:0.7rem;
    }
    .project-tags span{
      background:rgba(255,255,255,0.05);
      padding:0.2rem 0.5rem;
      border-radius:8px;
      font-size:0.85rem;
      color:var(--muted);
    }

    .contact-grid{
      display:grid;
      grid-template-columns:1fr;
      gap:1rem;
    }
    .contact-form input,
    .contact-form textarea{
      width:100%;
      background:rgba(255,255,255,0.05);
      border:1px solid rgba(255,255,255,0.05);
      padding:0.6rem;
      border-radius:8px;
      color:white;
      margin-top:0.4rem;
      outline:none;
    }

    .contact-info{ padding:1rem; }

  
    .site-footer{
      border-top:1px solid rgba(255,255,255,0.05);
      padding:1rem 0;
      color:var(--muted);
      text-align:center;
      margin-top:2rem;
    }

   
    @keyframes colorShift{
      0%{ background:linear-gradient(90deg,#7c5cff,#27b6ff); }
      50%{ background:linear-gradient(90deg,#27b6ff,#7c5cff); }
      100%{ background:linear-gradient(90deg,#7c5cff,#27b6ff); }
    }

    @media (min-width:48rem){
      .hero-inner{
        flex-direction:row;
        text-align:left;
      }
      .hero-actions{
        justify-content:flex-start;
      }
      .about-grid{
        grid-template-columns:1fr 300px;
      }
      .skills-grid{
        grid-template-columns:repeat(3,1fr);
      }
      .projects-grid{
        grid-template-columns:repeat(2,1fr);
      }
      .contact-grid{
        grid-template-columns:1fr 300px;
      }
    }

    @media (min-width:64rem){
      .projects-grid{
        grid-template-columns:repeat(3,1fr);
      }
    }
  </style>
</head>

<body>

  <header class="site-header">
    <div class="container header-inner">
      <div class="logo">Disha R.</div>

      <nav class="nav">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
      </nav>

      <button class="cta">Download CV</button>
    </div>
  </header>

  <section id="home" class="hero">
    <div class="container hero-inner">

      <div class="hero-content">
        <h1>Hello, I'm <span class="name">Disha Raghav</span></h1>
        <h2 class="role">I build things — <span class="highlighted-role">Full Stack Developer</span></h2>

        <p class="lead">Student | Aspiring coder | Future coder who makes parents proud.</p>

        <div class="hero-actions">
          <a class="btn primary" href="#projects">See Projects</a>
          <a class="btn ghost" href="#contact">Contact Me</a>
        </div>
      </div>

      <div class="hero-image">
        <img src="disha phto.jpg" alt="Profile Picture">
      </div>

    </div>
  </section>


  <section id="about" class="about">
    <div class="container">
      <h3 class="section-title">About</h3>

      <div class="about-grid">
        <div class="about-text">
          <p>
            I'm Disha — a student passionate about development and design. I enjoy learning new
            things, creating interfaces, solving problems, and working with modern web technologies.
          </p>

          <ul class="about-list">
            <li><strong>Location:</strong> India</li>
            <li><strong>Education:</strong> BSc CS</li>
            <li><strong>Interests:</strong> Web Dev, UI/UX, Medicine</li>
          </ul>
        </div>

        <div class="about-stats">
          <div class="stat">
            <div class="stat-num">12</div>
            <div class="stat-label">Projects</div>
          </div>
          <div class="stat">
            <div class="stat-num">3</div>
            <div class="stat-label">Languages</div>
          </div>
          <div class="stat">
            <div class="stat-num">100%</div>
            <div class="stat-label">Curiosity</div>
          </div>
        </div>
      </div>
    </div>
  </section>


  <section id="skills" class="skills">
    <div class="container">
      <h3 class="section-title">Skills</h3>

      <div class="skills-grid">
        <div class="card"><h4>HTML</h4><p>Semantic structure</p></div>
        <div class="card"><h4>CSS</h4><p>Flexbox, Grid, animations</p></div>
        <div class="card"><h4>JS</h4><p>DOM & logic</p></div>
        <div class="card"><h4>Python</h4><p>Scripting & logic</p></div>
        <div class="card"><h4>Git</h4><p>Version control</p></div>
        <div class="card"><h4>Design</h4><p>UI/UX basics</p></div>
      </div>
    </div>
  </section>

  <section id="projects" class="projects">
    <div class="container">
      <h3 class="section-title">Projects</h3>

      <div class="projects-grid">

        <div class="project card">
          <img src="create-a-python-script.webp">
          <div class="project-body">
            <h4>Mini Library (Python)</h4>
            <p>File-based book management system.</p>
            <div class="project-tags">
              <span>Python</span><span>File I/O</span>
            </div>
          </div>
        </div>

        <div class="project card">
          <img src="js.png">
          <div class="project-body">
            <h4>Prompt Quizzer (JS)</h4>
            <p>Console-based quiz app using prompt() & alert().</p>
            <div class="project-tags">
              <span>JavaScript</span><span>Console</span>
            </div>
          </div>
        </div>

        <div class="project card">
          <img src="web.webp">
          <div class="project-body">
            <h4>Portfolio Website</h4>
            <p>Responsive one-page site (this!)</p>
            <div class="project-tags">
              <span>HTML</span><span>CSS</span>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>

  <section id="contact" class="contact">
    <div class="container">
      <h3 class="section-title">Contact</h3>

      <div class="contact-grid">

        <form class="contact-form" onsubmit="event.preventDefault(); alert('Message Sent!');">
          <label>
            Name
            <input type="text" required>
          </label>

          <label>
            Email
            <input type="email" required>
          </label>

          <label>
            Message
            <textarea rows="4" required></textarea>
          </label>

          <button class="btn primary" type="submit">Send</button>
        </form>

        <div class="contact-info card">
          <h4>Get in touch</h4>
          <p>Email: disharaghav@gmail.com</p>
          <p>Phone: +91 98XXXXXX</p>
        </div>

      </div>
    </div>
  </section>

  
  <footer class="site-footer">
    © 2025 — Disha Raghav. All rights reserved.
  </footer>

</body>
</html>

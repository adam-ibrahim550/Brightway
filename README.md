[index.html](https://github.com/user-attachments/files/22411447/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>BrightWave Portfolio</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<style>
/* Reset and Base */
* { margin:0; padding:0; box-sizing:border-box; font-family:"Segoe UI", Arial, sans-serif; transition:0.3s; }
body { background:#111; color:white; line-height:1.6; scroll-behavior:smooth; overflow-x:hidden; }
body.light { background:#f0f0f0; color:#111; }

/* Navigation */
nav {
  display:flex; justify-content:space-between; align-items:center;
  padding:1rem 2rem; background:#222; color:white;
  position:sticky; top:0; z-index:1000; box-shadow:0 4px 6px rgba(0,0,0,0.5);
}
nav h1 { font-size:1.8rem; letter-spacing:1px; cursor:pointer; color:#ff6b6b; }
nav ul { list-style:none; display:flex; gap:2rem; }
nav ul li a { color:white; text-decoration:none; font-weight:bold; }
nav ul li a:hover { color:#ff6b6b; }
#themeToggle { padding:0.4rem 0.8rem; border:none; border-radius:6px; cursor:pointer; background:#ff6b6b; color:white; font-weight:bold; }

/* Hero Section */
.hero { height:90vh; display:flex; justify-content:center; align-items:center; position:relative; overflow:hidden; 
       background:url('https://images.unsplash.com/photo-1517433456452-f9633a875f6f?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=Mnw0NzE5NzB8MHwxfHNlYXJjaHwxfHxjb2RpbmclMjBzdG9ja3xlbnwwfHx8fDE2OTU4OTQ3Mzg&ixlib=rb-4.0.3&q=80&w=1600') no-repeat center/cover;}
.hero::after { content:""; position:absolute; top:0; left:0; width:100%; height:100%; background:rgba(0,0,0,0.3); }
.hero-content { position:relative; z-index:1; text-align:center; max-width:700px; }
.hero h2 { font-size:3rem; margin-bottom:1rem; animation:fadeUp 1.5s ease forwards; opacity:0; transform:translateY(30px); }
.hero p { font-size:1.3rem; animation:fadeUp 2s ease forwards; color:#f0f0f0; opacity:0; transform:translateY(30px); }

@keyframes fadeUp { 0%{opacity:0; transform:translateY(30px);} 100%{opacity:1; transform:translateY(0);} }

/* Container & Sections */
.container { max-width:1000px; margin:3rem auto; padding:0 1rem; }
section { margin-bottom:4rem; padding:2rem; border-radius:12px; opacity:0; transform:translateY(50px); transition:0.8s ease-out; position:relative; }
section.visible { opacity:1; transform:translateY(0); }

/* Section Titles */
section h2 { font-size:2rem; margin-bottom:1rem; padding-left:0.5rem; letter-spacing:1px; color:white; }

/* Section Colors */
#about { background:#1abc9c; color:white; }
#projects .card:nth-child(1){background:#e74c3c;color:white;}
#projects .card:nth-child(2){background:#f1c40f;color:#111;}
#projects .card:nth-child(3){background:#3498db;color:white;}
#projects .card:nth-child(4){background:#9b59b6;color:white;}

/* Cards */
.card { border-radius:12px; padding:1.5rem; margin:1rem 0; box-shadow:0 4px 12px rgba(0,0,0,0.3); transition:transform 0.4s, box-shadow 0.4s, opacity 0.6s; opacity:0; transform:translateY(50px); }
.card.visible { opacity:1; transform:translateY(0); }
.card:hover { transform:translateY(-10px) scale(1.05) rotateX(2deg); box-shadow:0 12px 25px rgba(0,0,0,0.5); }

/* Projects Grid */
.grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(250px,1fr)); gap:1.5rem; }

/* Contact Form */
form { display:flex; flex-direction:column; gap:1rem; background:white; padding:1.5rem; border-radius:12px; color:#111; opacity:0; transform:translateY(50px); transition:0.8s ease-out; }
form.visible { opacity:1; transform:translateY(0); }
form input, form textarea { padding:0.9rem; border:1px solid #ccc; border-radius:8px; font-size:1rem; }
form button { padding:0.9rem; border:none; border-radius:8px; background:#111; color:white; font-size:1rem; cursor:pointer; font-weight:bold; }
form button:hover { background:#333; transform:scale(1.05); }

/* Footer */
footer { text-align:center; padding:1rem; display:flex; flex-direction:column; align-items:center; gap:0.5rem; background:#222; color:white; }
footer a { color:#ff6b6b; margin:0 0.5rem; font-size:1.2rem; transition:0.3s; }
footer a:hover { color:#ff4c4c; transform:scale(1.2); }

/* Report Button */
#reportBtn { position:fixed; bottom:20px; left:20px; background:#ff6b6b; color:white; padding:0.8rem 1rem; border-radius:50px; cursor:pointer; font-weight:bold; box-shadow:0 4px 8px rgba(0,0,0,0.3); }
#reportBtn:hover { transform:scale(1.1); }

/* Responsive */
@media(max-width:900px){ .hero{background-position:center;} }
@media(max-width:600px){ .hero h2{font-size:2rem;} nav ul{flex-direction:column; gap:1rem;} }
</style>
</head>
<body>

<nav>
  <h1>BrightWave</h1>
  <div><button id="themeToggle">Toggle Mode</button></div>
  <ul>
    <li><a href="#about">About</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<section class="hero">
  <div class="hero-content">
    <h2>Welcome to BrightWave</h2>
    <p>Interactive, coding-inspired, and visually striking web experiences!</p>
  </div>
</section>

<div class="container">
  <section id="about">
    <h2>About Me</h2>
    <div class="card">
      <p>Creative web developer passionate about coding, building interactive projects, and delivering premium digital experiences.</p>
    </div>
  </section>

  <section id="projects">
    <h2>Projects</h2>
    <div class="grid">
      <div class="card"><h3>BrightWave Landing</h3><p>Interactive landing page with code-inspired design.</p></div>
      <div class="card"><h3>Blog Hub</h3><p>Responsive blogging platform with modern UI.</p></div>
      <div class="card"><h3>Mini Game</h3><p>HTML5 Canvas game with interactive effects.</p></div>
      <div class="card"><h3>Portfolio Showcase</h3><p>Showcase of my best work with premium visuals.</p></div>
    </div>
  </section>

  <section id="contact">
    <h2>Contact Me</h2>
    <form id="contactForm" action="https://api.web3forms.com/submit" method="POST">
      <input type="hidden" name="access_key" value="0d0910eb-a77d-42df-96df-2294735a6062">
      <input type="text" name="name" placeholder="Full Name" required>
      <input type="text" name="username" placeholder="Username" required>
      <input type="tel" name="phone" placeholder="Phone Number (+Country Code)" required>
      <input type="email" name="email" placeholder="Email" required>
      <textarea name="message" rows="5" placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>
</div>

<footer>
  <div>© 2025 BrightWave | Built with ❤</div>
  <div>
    <a href="https://github.com/" target="_blank"><i class="fab fa-github"></i></a>
    <a href="https://www.linkedin.com/" target="_blank"><i class="fab fa-linkedin"></i></a>
    <a href="mailto:adamibrahim007550@gmail.com"><i class="fas fa-envelope"></i></a>
  </div>
</footer>

<a id="reportBtn" href="https://wa.me/97070876384" target="_blank"><i class="fas fa-flag"></i> Report</a>

<script>
// Dark/light toggle
document.getElementById('themeToggle').addEventListener('click', ()=>{
  document.body.classList.toggle('light');
});

// IntersectionObserver for sections, cards, and form
const elements = document.querySelectorAll('section, .card, form');
const observer = new IntersectionObserver(entries=>{
  entries.forEach(entry=>{
    if(entry.isIntersecting){ entry.target.classList.add('visible'); }
  });
},{threshold:0.2});
elements.forEach(el=>observer.observe(el));
</script>

</body>
</html>

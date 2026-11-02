<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Alankar Sharma | Android, IoT & Security</title>
<meta name="description" content="Portfolio of Alankar Sharma: Android apps, IoT automation and ethical hacking.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,400;12..96,600;12..96,800&display=swap" rel="stylesheet">
<style>
:root{
  --ink:#10142b; --panel:#1a2048; --line:#2b3366; --paper:#eef0ff; --muted:#a3a9d6;
  --stop:#ff5d73; --calm:#7ee0c3;
  --font:"Bricolage Grotesque",system-ui,-apple-system,"Segoe UI",sans-serif;
}
*{box-sizing:border-box;margin:0}
html{scroll-behavior:smooth}
body{background:var(--ink);color:var(--paper);font:400 1.05rem/1.65 var(--font);-webkit-font-smoothing:antialiased}
a{color:inherit}
:focus-visible{outline:3px solid var(--calm);outline-offset:3px;border-radius:6px}
.wrap{max-width:1040px;margin:0 auto;padding:0 22px}

nav{position:sticky;top:0;z-index:5;background:rgba(16,20,43,.86);backdrop-filter:blur(10px);border-bottom:1px solid var(--line)}
nav .wrap{display:flex;justify-content:space-between;align-items:center;height:60px}
nav b{font-weight:800;letter-spacing:-.01em}
nav ul{display:flex;gap:22px;list-style:none;padding:0}
nav a{text-decoration:none;color:var(--muted);transition:color .2s}
nav a:hover{color:var(--paper)}

/* hero */
.hero{display:grid;grid-template-columns:1.2fr .8fr;gap:48px;align-items:center;padding:84px 0 70px}
h1{font-size:clamp(2.6rem,7vw,4.9rem);line-height:1;font-weight:800;letter-spacing:-.035em}
.role{margin-top:18px;font-size:1.35rem;color:var(--calm);min-height:2em;font-weight:600}
.caret{display:inline-block;width:3px;height:1.1em;background:var(--calm);margin-left:3px;vertical-align:-.18em;animation:blink 1s steps(1) infinite}
.lead{margin-top:14px;color:var(--muted);max-width:46ch}
.cta{display:flex;gap:12px;margin-top:28px;flex-wrap:wrap}
.btn{display:inline-block;padding:12px 22px;border-radius:999px;font-weight:600;text-decoration:none;border:1.5px solid var(--line);transition:transform .15s,background .2s}
.btn.main{background:var(--paper);color:var(--ink);border-color:var(--paper)}
.btn:hover{transform:translateY(-2px)}

/* phone demo: the one memorable element */
.phone{width:min(270px,100%);margin:0 auto;border:2px solid var(--line);border-radius:34px;padding:14px;background:var(--panel);box-shadow:0 30px 70px rgba(0,0,0,.45)}
.screen{position:relative;height:350px;border-radius:22px;background:#0a0d1f;overflow:hidden;display:flex;flex-direction:column;justify-content:flex-end;padding:18px}
.reel{position:absolute;inset:0;display:flex;align-items:center;justify-content:center;font-size:3.4rem;transition:transform .35s ease,background .35s}
.reel.out{transform:translateY(-100%)}
.block{position:absolute;inset:0;background:var(--stop);color:#fff;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:20px;transform:translateY(100%);transition:transform .4s ease}
.block.on{transform:none}
.block strong{font-size:1.5rem;line-height:1.2}
.block span{font-size:.9rem;opacity:.9;margin-top:8px}
.count{position:relative;z-index:1;font-size:.9rem;color:#fff;background:rgba(0,0,0,.45);padding:6px 12px;border-radius:999px;align-self:flex-start}
.phone button{width:100%;margin-top:12px;padding:12px;border-radius:14px;border:0;font:600 1rem var(--font);background:var(--calm);color:var(--ink);cursor:pointer}
.phone button:active{transform:scale(.97)}
.hint{text-align:center;color:var(--muted);font-size:.85rem;margin-top:12px}

/* sections */
section{padding:64px 0;border-top:1px solid var(--line)}
h2{font-size:clamp(1.8rem,4vw,2.5rem);letter-spacing:-.025em;font-weight:800;margin-bottom:26px}

/* projects: first card is larger, so cards are not all identical */
.grid{display:grid;grid-template-columns:repeat(6,1fr);gap:18px}
.card{grid-column:span 2;display:flex;flex-direction:column;gap:10px;padding:24px;border:1px solid var(--line);border-radius:18px;background:var(--panel);text-decoration:none;transition:transform .2s,border-color .2s}
.card:first-child{grid-column:span 4;border-radius:26px;padding:30px;border-color:var(--calm)}
.card:hover{transform:translateY(-4px);border-color:var(--paper)}
.card h3{font-size:1.3rem;letter-spacing:-.01em}
.card p{color:var(--muted);flex:1}
.tags{display:flex;gap:8px;flex-wrap:wrap}
.tags span{font-size:.82rem;padding:3px 11px;border-radius:999px;background:var(--ink);border:1px solid var(--line);color:var(--muted)}

/* skills */
.skills{display:flex;flex-wrap:wrap;gap:12px}
.skills span{padding:9px 18px;border-radius:12px;border:1px solid var(--line);background:var(--panel);font-weight:600;transition:border-color .2s,transform .2s}
.skills span:hover{border-color:var(--calm);transform:translateY(-2px)}

.now{list-style:none;padding:0;display:grid;gap:10px;max-width:60ch}
.now li{padding-left:28px;position:relative;color:var(--muted)}
.now li::before{content:"";position:absolute;left:4px;top:.65em;width:10px;height:10px;border-radius:50%;background:var(--calm)}

footer{padding:40px 0 60px;border-top:1px solid var(--line);color:var(--muted);display:flex;justify-content:space-between;flex-wrap:wrap;gap:12px}

.reveal{opacity:0;transform:translateY(18px);transition:opacity .6s,transform .6s}
.reveal.in{opacity:1;transform:none}

@keyframes blink{50%{opacity:0}}
@media(max-width:820px){
  .hero{grid-template-columns:1fr;padding-top:50px}
  .grid{grid-template-columns:1fr}
  .card,.card:first-child{grid-column:auto}
  nav ul{gap:14px}
}
@media(prefers-reduced-motion:reduce){
  *{animation:none!important;transition:none!important}
  .reveal{opacity:1;transform:none}
}
</style>
</head>
<body>

<nav><div class="wrap">
  <b>Alankar Sharma</b>
  <ul>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</div></nav>

<main class="wrap">
  <header class="hero">
    <div>
      <h1>Alankar Sharma</h1>
      <p class="role"><span id="typed"></span><span class="caret" aria-hidden="true"></span></p>
      <p class="lead">I build Android apps and IoT automation, and I'm learning ethical hacking. I like fixing everyday annoyances with working software.</p>
      <div class="cta">
        <a class="btn main" href="#projects">See my projects</a>
        <a class="btn" href="https://github.com/CreaterAlankar7">GitHub profile</a>
      </div>
    </div>

    <--Interactive demo of Doomstop -->
    <div>
      <div class="phone" aria-label="Doomstop demo">
        <div class="screen">
          <div class="reel" id="reel" aria-hidden="true">🎬</div>
          <div class="block" id="block" role="status">
            <strong>Reel limit reached</strong>
            <span>Doomstop blocked this for you.</span>
          </div>
          <div class="count" id="count">Reels watched: 0 / 5</div>
        </div>
        <button id="swipe" type="button">Swipe to next reel</button>
      </div>
      <p class="hint">A tiny demo of Doomstop. Try to doomscroll.</p>
    </div>
  </header>

  <section id="projects">
    <h2 class="reveal">Projects</h2>
    <div class="grid" id="grid"></div>
  </section>

  <section id="skills">
    <h2 class="reveal">Skills</h2>
    <div class="skills reveal">
      <span>Kotlin</span><span>Android</span><span>Python</span><span>C#</span>
      <span>HTML &amp; CSS</span><span>Batch scripting</span><span>IoT &amp; Arduino</span>
    </div>
  </section>

  <section id="now">
    <h2 class="reveal">What I'm working on</h2>
    <ul class="now reveal">
      <li>Improving Doomstop, my Kotlin app that limits Instagram Reels</li>
      <li>Learning ethical hacking and cybersecurity</li>
      <li>Building IoT automation projects</li>
    </ul>
  </section>

  <section id="contact">
    <h2 class="reveal">Contact</h2>
    <p class="lead reveal">Want to collaborate or have a question? Send me a message.</p>
    <div class="cta reveal">
      <a class="btn main" href="mailto:your-email@example.com">Email me</a>
      <a class="btn" href="https://linkedin.com/in/your-link">LinkedIn</a>
      <a class="btn" href="https://github.com/CreaterAlankar7">GitHub</a>
    </div>
  </section>
</main>

<footer class="wrap">
  <span>&copy; <span id="yr"></span> Alankar Sharma</span>
  <span>Built with HTML, CSS and JavaScript</span>
</footer>

<script>
/* ---- EDIT YOUR PROJECTS HERE ---- */
const projects = [
  {name:"Doomstop", desc:"Android app written in Kotlin that blocks Instagram Reels after a time or scroll limit you set.", tags:["Kotlin","Android"], link:"https://github.com/CreaterAlankar7/Doomstop"},
  {name:"Project 2", desc:"One-line description of what it does.", tags:["Python"], link:"https://github.com/CreaterAlankar7"},
  {name:"Project 3", desc:"One-line description of what it does.", tags:["IoT"], link:"https://github.com/CreaterAlankar7"}
];
const grid = document.getElementById("grid");
projects.forEach(p=>{
  const a = document.createElement("a");
  a.className = "card reveal"; a.href = p.link;
  a.innerHTML = "<h3></h3><p></p><div class='tags'></div>";
  a.querySelector("h3").textContent = p.name;
  a.querySelector("p").textContent = p.desc;
  p.tags.forEach(t=>{const s=document.createElement("span");s.textContent=t;a.querySelector(".tags").appendChild(s)});
  grid.appendChild(a);
});

/* ---- Typing effect ---- */
const roles = ["Android developer","IoT and automation builder","Ethical hacking learner"];
const typed = document.getElementById("typed");
const still = matchMedia("(prefers-reduced-motion: reduce)").matches;
if(still){ typed.textContent = roles.join(" · "); }
else{
  let r=0,c=0,del=false;
  (function tick(){
    const w = roles[r];
    typed.textContent = w.slice(0,c);
    if(!del && c===w.length){ del=true; return setTimeout(tick,1400); }
    if(del && c===0){ del=false; r=(r+1)%roles.length; }
    c += del ? -1 : 1;
    setTimeout(tick, del ? 35 : 75);
  })();
}

/* ---- Doomstop demo ---- */
const LIMIT = 5, emojis = ["🎬","😂","🐱","🍕","🎵"];
let n = 0;
const reel = document.getElementById("reel"), block = document.getElementById("block"),
      count = document.getElementById("count"), btn = document.getElementById("swipe");
btn.addEventListener("click", ()=>{
  if(n >= LIMIT){ n = 0; block.classList.remove("on"); btn.textContent = "Swipe to next reel"; reel.textContent = emojis[0]; count.textContent = "Reels watched: 0 / " + LIMIT; return; }
  n++;
  reel.classList.add("out");
  setTimeout(()=>{ reel.textContent = emojis[n % emojis.length]; reel.classList.remove("out"); }, 250);
  count.textContent = "Reels watched: " + n + " / " + LIMIT;
  if(n >= LIMIT){ block.classList.add("on"); btn.textContent = "Reset demo"; }
});

/* ---- Reveal on scroll ---- */
const io = new IntersectionObserver(es=>es.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add("in"); io.unobserve(e.target);} }), {threshold:.15});
document.querySelectorAll(".reveal").forEach(el=>io.observe(el));

document.getElementById("yr").textContent = new Date().getFullYear();
</script>
</body>
</html>

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

/* nav */
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

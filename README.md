<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#2558d8">
<meta name="description" content="EduBridge — learn, practise and grow from early learning to university.">
<title>EduBridge | Learn Without Limits</title>
<style>
:root{--blue:#2558d8;--blue2:#eaf0ff;--ink:#17233c;--muted:#68758e;--bg:#f7f9ff;--white:#fff;--line:#e3e9f5;--shadow:0 12px 35px rgba(31,57,111,.09)}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{margin:0;font-family:system-ui,-apple-system,BlinkMacSystemFont,"Segoe UI",sans-serif;color:var(--ink);background:var(--bg);line-height:1.55}
button,input,select{font:inherit}
button{cursor:pointer}
.wrap{width:min(1120px,92%);margin:auto}
.topbar{background:#14264a;color:#eaf0ff;text-align:center;padding:8px 12px;font-size:.85rem}
.nav{display:flex;align-items:center;justify-content:space-between;gap:16px;padding:17px 0}
.brand{display:flex;align-items:center;gap:10px;font-weight:850;font-size:1.35rem;letter-spacing:-.5px;color:var(--ink);text-decoration:none}
.logo{width:42px;height:42px;border-radius:14px;background:linear-gradient(135deg,var(--blue),#6e8fff);display:grid;place-items:center;color:#fff;font-size:1.25rem;box-shadow:0 7px 18px #2558d833}
.navlinks{display:flex;gap:22px;align-items:center}
.navlinks a{color:var(--muted);text-decoration:none;font-weight:650;font-size:.94rem}
.navlinks a:hover{color:var(--blue)}
.btn{border:0;border-radius:13px;padding:12px 17px;font-weight:750;display:inline-flex;align-items:center;justify-content:center;gap:8px;text-decoration:none;transition:transform .15s,box-shadow .15s}
.btn:hover{transform:translateY(-1px)}
.primary{background:var(--blue);color:#fff;box-shadow:0 8px 18px #2558d82b}
.secondary{background:var(--blue2);color:var(--blue)}
.hero{padding:42px 0 35px;background:radial-gradient(circle at 90% 10%,#dfe8ff 0,transparent 32%),linear-gradient(180deg,#fff,#f7f9ff)}
.hero-grid{display:grid;grid-template-columns:1.1fr .9fr;gap:38px;align-items:center}
.eyebrow{display:inline-flex;align-items:center;gap:8px;background:#e8f8f2;color:#087657;border-radius:99px;padding:7px 12px;font-weight:750;font-size:.82rem}
.hero h1{font-size:clamp(2.35rem,5vw,4.15rem);line-height:1.08;letter-spacing:-2px;margin:18px 0}
.hero h1 span{color:var(--blue)}
.hero p{font-size:1.08rem;color:var(--muted);max-width:590px}
.hero-actions{display:flex;gap:12px;flex-wrap:wrap;margin:25px 0}
.trust{display:flex;gap:18px;flex-wrap:wrap;color:var(--muted);font-size:.88rem;font-weight:650}
.hero-art{position:relative;min-height:330px;border-radius:32px;background:linear-gradient(145deg,#dfe8ff,#f3eaff);display:grid;place-items:center;overflow:hidden}
.orbit{position:absolute;width:260px;height:260px;border:2px dashed #91a9f0;border-radius:50%}
.book{position:relative;z-index:1;width:180px;height:190px;background:#fff;border-radius:20px;box-shadow:0 22px 45px #213c7d26;display:flex;flex-direction:column;align-items:center;justify-content:center;transform:rotate(-5deg);border:1px solid #edf0fa}
.book .big{font-size:3.5rem}
.book strong{font-size:1.1rem;color:var(--blue)}
.float{position:absolute;background:#fff;border-radius:16px;padding:12px 15px;box-shadow:var(--shadow);font-weight:750;font-size:.9rem}
.f1{top:35px;left:22px}.f2{right:20px;top:90px}.f3{bottom:28px;left:30px}
.section{padding:48px 0}
.section-head{display:flex;justify-content:space-between;align-items:end;gap:20px;margin-bottom:22px}
.section-head h2{margin:0;font-size:clamp(1.6rem,3vw,2.2rem);letter-spacing:-.8px}
.section-head p{margin:6px 0 0;color:var(--muted)}
.levels{display:grid;grid-template-columns:repeat(5,1fr);gap:14px}
.level,.subject,.lesson,.feature{background:var(--white);border:1px solid var(--line);border-radius:20px;padding:19px;box-shadow:0 5px 20px #1b377508}
.level{transition:.18s;cursor:pointer;text-align:left}
.level:hover,.level.active{border-color:#8da8ff;box-shadow:var(--shadow);transform:translateY(-3px)}
.level .emoji{width:48px;height:48px;border-radius:15px;display:grid;place-items:center;font-size:1.55rem;background:var(--blue2);margin-bottom:12px}
.level h3,.subject h3,.lesson h3{margin:0 0 5px;font-size:1.02rem}
.level p,.subject p,.lesson p{color:var(--muted);font-size:.88rem;margin:0}
.filterbar{display:flex;gap:12px;flex-wrap:wrap;margin:20px 0}
.field{display:flex;flex-direction:column;gap:6px;flex:1;min-width:170px}
.field label{font-size:.83rem;font-weight:750;color:#45536e}
.field select,.field input{width:100%;border:1px solid #dce3f1;border-radius:12px;background:#fff;padding:12px 13px;color:var(--ink);outline:none}
.field select:focus,.field input:focus{border-color:var(--blue);box-shadow:0 0 0 3px #2558d81a}
.subjects{display:grid;grid-template-columns:repeat(3,1fr);gap:15px}
.subject{display:flex;gap:14px;align-items:flex-start}
.subject-icon{flex:0 0 48px;width:48px;height:48px;border-radius:15px;display:grid;place-items:center;font-size:1.45rem;background:#e9f8f3}
.subject:nth-child(2) .subject-icon{background:#fff2d9}
.subject:nth-child(3) .subject-icon{background:#eee8ff}
.subject:nth-child(4) .subject-icon{background:#e3f3ff}
.subject:nth-child(5) .subject-icon{background:#ffe9ef}
.subject:nth-child(6) .subject-icon{background:#edf4db}
.subject .btn{margin-top:12px;padding:9px 12px;font-size:.85rem}
.lesson-area{background:#eef3ff;border-radius:26px;padding:25px}
.lesson-grid{display:grid;grid-template-columns:1fr 1fr;gap:16px}
.lesson{box-shadow:none}
.tag{display:inline-block;background:#e8efff;color:var(--blue);font-size:.75rem;font-weight:800;padding:4px 9px;border-radius:99px;margin-bottom:10px}
.lesson .btn{margin-top:13px}
.feature-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:15px}
.feature .emoji{font-size:1.7rem}
.feature h3{margin:8px 0 4px}
.feature p{margin:0;color:var(--muted);font-size:.92rem}
.callout{background:linear-gradient(120deg,#214ec5,#6d62dd);color:#fff;border-radius:26px;padding:28px;display:flex;justify-content:space-between;align-items:center;gap:20px}
.callout p{color:#e6eaff;margin:6px 0 0}
.callout .btn{background:#fff;color:#244fc1;white-space:nowrap}
.footer{margin-top:45px;background:#14264a;color:#eaf0ff;padding:30px 0}
.footer-row{display:flex;justify-content:space-between;gap:18px;flex-wrap:wrap}
.footer p{margin:6px 0;color:#bac7e4;font-size:.88rem}
.notice{color:var(--muted);font-size:.83rem;margin-top:14px}
.hidden{display:none!important}
.modal{position:fixed;inset:0;background:#101a32aa;display:grid;place-items:center;padding:16px;z-index:10}
.modal-card{background:#fff;border-radius:22px;padding:24px;width:min(570px,100%);max-height:90vh;overflow:auto;box-shadow:0 25px 80px #07132b44}
.modal-head{display:flex;justify-content:space-between;gap:15px;align-items:start}
.close{border:0;background:#eef2fb;border-radius:10px;width:38px;height:38px;font-size:1.2rem}
.answer{display:block;width:100%;text-align:left;border:1px solid var(--line);background:#fff;border-radius:12px;padding:12px;margin:9px 0}
.answer:hover{border-color:var(--blue);background:#f4f7ff}
.answer.correct{border-color:#15956e;background:#e9f8f2}
.answer.wrong{border-color:#d65353;background:#fff0f0}
.feedback{font-weight:750;margin:12px 0}
@media(max-width:850px){
.hero-grid{grid-template-columns:1fr}
.hero-art{min-height:270px}
.levels{grid-template-columns:repeat(3,1fr)}
.subjects{grid-template-columns:repeat(2,1fr)}
.navlinks{gap:12px}
.navlinks a:not(.btn){display:none}
}
@media(max-width:560px){
.hero{padding-top:25px}
.hero-art{min-height:240px}
.levels{grid-template-columns:repeat(2,1fr)}
.subjects,.lesson-grid,.feature-grid{grid-template-columns:1fr}
.section{padding:35px 0}
.section-head,.callout{align-items:start;flex-direction:column}
.level{padding:14px}
.hero h1{letter-spacing:-1.2px}
.nav .primary{padding:10px 12px}
.trust{gap:10px}
}
.units{display:grid;grid-template-columns:repeat(3,1fr);gap:15px}
.unit{background:#fff;border:1px solid var(--line);border-radius:20px;padding:19px;box-shadow:0 5px 20px #1b377508}
.unit .code{font-size:.78rem;font-weight:800;color:var(--blue)}
.unit h3{margin:4px 0 5px;font-size:1.02rem}
.unit p{color:var(--muted);font-size:.88rem;margin:0}
.unit .btn{margin-top:12px;padding:9px 12px;font-size:.85rem}
@media(max-width:850px){.units{grid-template-columns:repeat(2,1fr)}}
@media(max-width:560px){.units{grid-template-columns:1fr}}
.group-title{margin:28px 0 12px;font-size:1.15rem}
.bot-fab{position:fixed;right:16px;bottom:16px;z-index:9;border:0;border-radius:99px;background:var(--blue);color:#fff;font-weight:750;padding:13px 18px;box-shadow:0 10px 28px #2558d855}
.bot-card{background:#fff;border-radius:22px;width:min(560px,100%);height:min(700px,92vh);display:flex;flex-direction:column;overflow:hidden;box-shadow:0 25px 80px #07132b44}
.bot-head{padding:14px 18px;background:var(--blue);color:#fff;display:flex;justify-content:space-between;align-items:center;gap:12px}
.bot-head small{display:block;color:#dbe6ff;font-size:.78rem}
.bot-head .close{background:#ffffff26;color:#fff}
.bot-log{flex:1;overflow:auto;padding:16px;display:flex;flex-direction:column;gap:10px;background:#f4f7ff}
.msg{max-width:92%;padding:11px 14px;border-radius:16px;font-size:.93rem;line-height:1.5}
.msg p{margin:0 0 8px}.msg p:last-child{margin:0}
.msg.bot{background:#fff;border:1px solid var(--line);align-self:flex-start}
.msg.me{background:var(--blue);color:#fff;align-self:flex-end}
.bot-actions{padding:12px;border-top:1px solid var(--line);background:#fff;display:flex;flex-direction:column;gap:8px;max-height:48%;overflow:auto}
.bot-actions select{width:100%;border:1px solid #dce3f1;border-radius:12px;padding:12px 13px;background:#fff;color:var(--ink)}
.bot-actions .btn:disabled{opacity:.55;cursor:not-allowed;transform:none}
.bot-intro{display:flex;gap:18px;align-items:center;justify-content:space-between;background:#fff;border:1px solid var(--line);border-radius:26px;padding:24px;box-shadow:var(--shadow)}
.bot-intro h2{margin:0 0 6px}.bot-intro p{margin:0;color:var(--muted)}
@media(max-width:560px){.bot-intro{flex-direction:column;align-items:stretch}}
</style>
</head>
<body>
<div class="topbar">🌍 Learn at your own pace — from your first lesson to university-level study.</div>

<header class="wrap nav">
  <a class="brand" href="#home"><span class="logo">E</span> EduBridge</a>
  <nav class="navlinks">
    <a href="#levels">Learning levels</a>
    <a href="#subjects">Subjects</a>
    <a href="#lessons">Try a lesson</a>
    <a class="btn primary" href="#subjects">Start learning →</a>
  </nav>
</header>

<main>
<section class="hero" id="home">
  <div class="wrap hero-grid">
    <div>
      <span class="eyebrow">✨ Your journey. Your future.</span>
      <h1>Make learning feel <span>possible.</span></h1>
      <p>Explore lessons, practise important skills, and build confidence — whether you're just starting school or preparing for university.</p>
      <div class="hero-actions">
        <a class="btn primary" href="#levels">Explore learning levels →</a>
        <a class="btn secondary" href="#lessons">Try a free lesson</a>
        <button class="btn secondary open-bot">🤖 Meet Study Bot</button>
      </div>
      <div class="trust">
        <span>✓ Beginner-friendly</span>
        <span>✓ Learn at your pace</span>
        <span>✓ Made for mobile</span>
      </div>
    </div>
    <div class="hero-art" aria-label="Illustration of learning resources">
      <div class="orbit"></div>
      <div class="book">
        <span class="big">📚</span>
        <strong>Learn &amp; grow</strong>
        <span style="color:#68758e;font-size:.8rem">One step at a time</span>
      </div>
      <div class="float f1">🧠 Keep curious</div>
      <div class="float f2">⭐ Practice daily</div>
      <div class="float f3">🎯 Reach your goals</div>
    </div>
  </div>
</section>

<section class="section wrap" id="studybot">
  <div class="bot-intro">
    <div>
      <h2>🤖 Meet your Study Bot</h2>
      <p>Choose any unit. The bot gives you the lesson to read first, then asks questions and awards marks.</p>
      <p class="notice">The Study Bot is a guided tutor built into this page. It is not a live AI model yet.</p>
    </div>
    <button class="btn primary open-bot">Start with Study Bot</button>
  </div>
</section>

<section class="section wrap" id="levels">
  <div class="section-head"><div>
    <h2>Where are you on your learning journey?</h2>
    <p>Choose a level to explore learning pathways.</p>
  </div></div>
  <div class="levels" id="levelCards">
    <button class="level active" data-level="All levels"><span class="emoji">🌈</span><h3>All levels</h3><p>Explore everything</p></button>
    <button class="level" data-level="Kindergarten"><span class="emoji">🧸</span><h3>Kindergarten</h3><p>Play and discover</p></button>
    <button class="level" data-level="Primary"><span class="emoji">✏️</span><h3>Primary</h3><p>Build foundations</p></button>
    <button class="level" data-level="Secondary"><span class="emoji">🔭</span><h3>Secondary</h3><p>Grow your skills</p></button>
    <button class="level" data-level="College & University"><span class="emoji">🎓</span><h3>College &amp; university</h3><p>Study in depth</p></button>
  </div>
  <p class="notice">Curriculum coverage and lesson libraries will grow over time. Choose your country below to help personalise your learning.</p>
</section>

<section class="section wrap" id="subjects">
  <div class="section-head"><div>
    <h2>Find your next subject</h2>
    <p>Choose a country and level, or search for a subject.</p>
  </div></div>

  <div class="filterbar">
    <div class="field">
      <label for="country">Country / curriculum</label>
      <select id="country">
        <option value="International">International learning</option>
        <option>Kenya</option><option>Uganda</option><option>Tanzania</option>
        <option>Rwanda</option><option>Nigeria</option><option>South Africa</option>
        <option>United Kingdom</option><option>United States</option><option>India</option>
        <option>Other / not listed</option>
      </select>
    </div>
    <div class="field">
      <label for="levelSelect">Learning level</label>
      <select id="levelSelect">
        <option>All levels</option><option>Kindergarten</option><option>Primary</option>
        <option>Secondary</option><option>College &amp; University</option>
      </select>
    </div>
    <div class="field">
      <label for="search">Search subjects</label>
      <input id="search" type="search" placeholder="e.g. Biology, maths…">
    </div>
  </div>

  <div class="subjects" id="subjectCards">
    <article class="subject" data-name="mathematics maths numeracy" data-levels="Kindergarten,Primary,Secondary,College & University">
      <div class="subject-icon">🔢</div>
      <div><h3>Mathematics</h3><p>Numbers, patterns, sets and problem-solving.</p>
      <button class="btn primary open-lesson" data-subject="Mathematics">Learn &amp; take quiz →</button></div>
    </article>
    <article class="subject" data-name="languages english communication literacy" data-levels="Kindergarten,Primary,Secondary,College & University">
      <div class="subject-icon">🗣️</div>
      <div><h3>Languages</h3><p>Reading, writing, grammar and communication.</p>
      <button class="btn primary open-lesson" data-subject="Languages">Learn &amp; take quiz →</button></div>
    </article>
    <article class="subject" data-name="biology science plants animals cells genetics" data-levels="Primary,Secondary,College & University">
      <div class="subject-icon">🧬</div>
      <div><h3>Biology</h3><p>Cells, living organisms and the environment.</p>
      <button class="btn primary open-lesson" data-subject="Biology">Learn &amp; take quiz →</button></div>
    </article>
    <article class="subject" data-name="chemistry matter reactions atoms" data-levels="Secondary,College & University">
      <div class="subject-icon">⚗️</div>
      <div><h3>Chemistry</h3><p>Matter, atoms, substances and reactions.</p>
      <button class="btn primary open-lesson" data-subject="Chemistry">Learn &amp; take quiz →</button></div>
    </article>
    <article class="subject" data-name="physics energy forces motion electricity" data-levels="Primary,Secondary,College & University">
      <div class="subject-icon">⚛️</div>
      <div><h3>Physics</h3><p>Forces, energy, motion and the natural world.</p>
      <button class="btn primary open-lesson" data-subject="Physics">Learn &amp; take quiz →</button></div>
    </article>
    <article class="subject" data-name="computer studies computing digital technology" data-levels="Primary,Secondary,College & University">
      <div class="subject-icon">💻</div>
      <div><h3>Computer Studies</h3><p>Computers, software and digital skills.</p>
      <button class="btn primary open-lesson" data-subject="Computer Studies">Learn &amp; take quiz →</button></div>
    </article>
  </div>

  <p id="noResults" class="notice hidden">No subjects match your search. Try another word or choose a different level.</p>
  <p id="curriculumNote" class="notice">Choose a country to help personalise the subjects displayed.</p>
</section>

<section class="section wrap hidden" id="units">
  <div class="section-head"><div>
    <h2>University &amp; college fields of study</h2>
    <p>Browse the main academic fields taught at universities worldwide.</p>
  </div></div>
  <h3 class="group-title">Humanities</h3>
  <div class="units">
    <article class="unit"><h3>Arts &amp; Visual Arts</h3><p>Fine art, art history, photography, design</p>
    <button class="btn primary open-lesson" data-subject="Arts &amp; Visual Arts">Learn &amp; take quiz →</button></article>
    <article class="unit"><h3>Performing Arts</h3><p>Music, theatre, dance, film studies</p>
    <button class="btn primary open-lesson" data-subject="Performing Arts">Learn &amp; take quiz →</button></article>
    <article class="unit"><h3>Language &amp; Literature</h3><p>Linguistics, rhetoric, creative writing, world languages</p>
    <button class="btn primary open-lesson" data-subject="Language &amp; Literature">Learn &amp; take quiz →</button></article>
    <article class="unit"><h3>Philosophy, Religion &amp; Ethics</h3><p>Epistemology, metaphysics, comparative religion, theology</p>
    <button class="btn primary open-lesson" data-subject="Philosophy, Religion &amp; Ethics">Learn &amp; take quiz →</button></article>
    <article class="unit"><h3>History</h3><p>World history, archaeology, classical studies</p>
    <button class="btn primary open-lesson" data-subject="History">Learn &amp; take quiz →</button></article>
    <article class="unit"><h3>Law</h3><p>Jurisprudence, constitutional law, international law</p>
    <button class="btn primary open-lesson" data-subject="Law">Learn &amp; take quiz →</button></article>
  </div>
  <h3 class="group-title">Social sciences</h3>
  <div class="units">
    <article class="unit"><h3>Anthropology &amp; Sociology</h3><p>Cultural studies, ethnography, social work</p>
    <button class="btn primary open-lesson" data-subject="Anthropology &amp; Sociology">Learn &amp; take quiz →</button></article>
    <article class="unit"><h3>Psychology</h3><p>Cognitive, clinical, developmental and social psychology</p>
    <button class="btn primary open-lesson" data-subject="Psychology">Learn &amp; take quiz →</button></article>
    <article class="unit"><h3>Economics &amp; Finance</h3><p>Macroeconomics, microeconomics, corporate finance, banking</p>
    <button class="btn primary open-lesson" data-subject="Principles of Microeconomics">Learn &amp; take quiz →</button></article>
    <article class="unit"><h3>Political Science &amp; International Relations</h3><p>Government, public policy, geopolitics</p>
    <button class="btn primary open-lesson" data-subject="Political Science &amp; International Relations">Learn &amp; take quiz →</button></article>
    <article class="unit"><h3>B<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#2558d8">
<meta name="description" content="EduBrigde — learn, practise and grow from early learning to university.">
<title>EduBrigde | Learn Without Limits</title>

<style>
:root {
  --blue: #2558d8;
  --blue2: #eaf0ff;
  --ink: #17233c;
  --muted: #68758e;
  --bg: #f7f9ff;
  --white: #fff;
  --green: #128568;
  --gold: #f2b544;
  --purple: #7856d8;
  --line: #e3e9f5;
  --shadow: 0 12px 35px rgba(31,57,111,.09);
}

* { box-sizing: border-box; }

html { scroll-behavior: smooth; }

body {
  margin: 0;
  font-family: system-ui, -apple-system, BlinkMacSystemFont,
    "Segoe UI", sans-serif;
  color: var(--ink);
  background: var(--bg);
  line-height: 1.55;
}

button, input, select { font: inherit; }
button { cursor: pointer; }

.wrap {
  width: min(1120px, 92%);
  margin: auto;
}

.topbar {
  background: #14264a;
  color: #eaf0ff;
  text-align: center;
  padding: 8px 12px;
  font-size: .85rem;
}

.nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 16px;
  padding: 17px 0;
}

.brand {
  display: flex;
  align-items: center;
  gap: 10px;
  font-weight: 850;
  font-size: 1.35rem;
  letter-spacing: -.5px;
  color: var(--ink);
  text-decoration: none;
}

.logo {
  width: 42px;
  height: 42px;
  border-radius: 14px;
  background: linear-gradient(135deg, var(--blue), #6e8fff);
  display: grid;
  place-items: center;
  color: white;
  font-size: 1.25rem;
  box-shadow: 0 7px 18px #2558d833;
}

.navlinks {
  display: flex;
  gap: 22px;
  align-items: center;
}

.navlinks a {
  color: var(--muted);
  text-decoration: none;
  font-weight: 650;
  font-size: .94rem;
}

.navlinks a:hover { color: var(--blue); }

.btn {
  border: 0;
  border-radius: 13px;
  padding: 12px 17px;
  font-weight: 750;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  text-decoration: none;
  transition: transform .15s, box-shadow .15s;
}

.btn:hover { transform: translateY(-1px); }

.primary {
  background: var(--blue);
  color: white;
  box-shadow: 0 8px 18px #2558d82b;
}

.secondary {
  background: var(--blue2);
  color: var(--blue);
}

.hero {
  padding: 42px 0 35px;
  background:
    radial-gradient(circle at 90% 10%, #dfe8ff 0, transparent 32%),
    linear-gradient(180deg, #fff, #f7f9ff);
}

.hero-grid {
  display: grid;
  grid-template-columns: 1.1fr .9fr;
  gap: 38px;
  align-items: center;
}

.eyebrow {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: #e8f8f2;
  color: #087657;
  border-radius: 99px;
  padding: 7px 12px;
  font-weight: 750;
  font-size: .82rem;
}

.hero h1 {
  font-size: clamp(2.35rem, 5vw, 4.15rem);
  line-height: 1.08;
  letter-spacing: -2px;
  margin: 18px 0;
}

.hero h1 span { color: var(--blue); }

.hero p {
  font-size: 1.08rem;
  color: var(--muted);
  max-width: 590px;
}

.hero-actions {
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
  margin: 25px 0;
}

.trust {
  display: flex;
  gap: 18px;
  flex-wrap: wrap;
  color: var(--muted);
  font-size: .88rem;
  font-weight: 650;
}

.hero-art {
  position: relative;
  min-height: 330px;
  border-radius: 32px;
  background: linear-gradient(145deg, #dfe8ff, #f3eaff);
  display: grid;
  place-items: center;
  overflow: hidden;
}

.orbit {
  position: absolute;
  width: 260px;
  height: 260px;
  border: 2px dashed #91a9f0;
  border-radius: 50%;
}

.book {
  position: relative;
  z-index: 1;
  width: 180px;
  height: 190px;
  background: #fff;
  border-radius: 20px;
  box-shadow: 0 22px 45px #213c7d26;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  transform: rotate(-5deg);
  border: 1px solid #edf0fa;
}

.book .big { font-size: 3.5rem; }
.book strong { font-size: 1.1rem; color: var(--blue); }

.float {
  position: absolute;
  background: white;
  border-radius: 16px;
  padding: 12px 15px;
  box-shadow: var(--shadow);
  font-weight: 750;
  font-size: .9rem;
}

.f1 { top: 35px; left: 22px; }
.f2 { right: 20px; top: 90px; }
.f3 { bottom: 28px; left: 30px; }

.section { padding: 48px 0; }

.section-head {
  display: flex;
  justify-content: space-between;
  align-items: end;
  gap: 20px;
  margin-bottom: 22px;
}

.section-head h2 {
  margin: 0;
  font-size: clamp(1.6rem, 3vw, 2.2rem);
  letter-spacing: -.8px;
}

.section-head p {
  margin: 6px 0 0;
  color: var(--muted);
}

.levels {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 14px;
}

.level, .subject, .lesson, .feature {
  background: var(--white);
  border: 1px solid var(--line);
  border-radius: 20px;
  padding: 19px;
  box-shadow: 0 5px 20px #1b377508;
}

.level {
  transition: .18s;
  cursor: pointer;
}

.level:hover, .level.active {
  border-color: #8da8ff;
  box-shadow: var(--shadow);
  transform: translateY(-3px);
}

.level .emoji {
  width: 48px;
  height: 48px;
  border-radius: 15px;
  display: grid;
  place-items: center;
  font-size: 1.55rem;
  background: var(--blue2);
  margin-bottom: 12px;
}

.level h3, .subject h3, .lesson h3 {
  margin: 0 0 5px;
  font-size: 1.02rem;
}

.level p, .subject p, .lesson p {
  color: var(--muted);
  font-size: .88rem;
  margin: 0;
}

.filterbar {
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
  margin: 20px 0;
}

.field {
  display: flex;
  flex-direction: column;
  gap: 6px;
  flex: 1;
  min-width: 170px;
}

.field label {
  font-size: .83rem;
  font-weight: 750;
  color: #45536e;
}

.field select, .field input {
  width: 100%;
  border: 1px solid #dce3f1;
  border-radius: 12px;
  background: white;
  padding: 12px 13px;
  color: var(--ink);
  outline: none;
}

.field select:focus, .field input:focus {
  border-color: var(--blue);
  box-shadow: 0 0 0 3px #2558d81a;
}

.subjects {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 15px;
}

.subject {
  display: flex;
  gap: 14px;
  align-items: flex-start;
}

.subject-icon {
  flex: 0 0 48px;
  width: 48px;
  height: 48px;
  border-radius: 15px;
  display: grid;
  place-items: center;
  font-size: 1.45rem;
  background: #e9f8f3;
}

.subject:nth-child(2) .subject-icon { background: #fff2d9; }
.subject:nth-child(3) .subject-icon { background: #eee8ff; }
.subject:nth-child(4) .subject-icon { background: #e3f3ff; }
.subject:nth-child(5) .subject-icon { background: #ffe9ef; }
.subject:nth-child(6) .subject-icon { background: #edf4db; }

.subject .btn {
  margin-top: 12px;
  padding: 9px 12px;
  font-size: .85rem;
}

.lesson-area {
  background: #eef3ff;
  border-radius: 26px;
  padding: 25px;
}

.lesson-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
}

.lesson { box-shadow: none; }

.tag {
  display: inline-block;
  background: #e8efff;
  color: var(--blue);
  font-size: .75rem;
  font-weight: 800;
  padding: 4px 9px;
  border-radius: 99px;
  margin-bottom: 10px;
}

.lesson .btn { margin-top: 13px; }

.feature-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 15px;
}

.feature .emoji { font-size: 1.7rem; }
.feature h3 { margin: 8px 0 4px; }

.feature p {
  margin: 0;
  color: var(--muted);
  font-size: .92rem;
}

.callout {
  background: linear-gradient(120deg, #214ec5, #6d62dd);
  color: white;
  border-radius: 26px;
  padding: 28px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
}

.callout p {
  color: #e6eaff;
  margin: 6px 0 0;
}

.callout .btn {
  background: white;
  color: #244fc1;
  white-space: nowrap;
}

.footer {
  margin-top: 45px;
  background: #14264a;
  color: #eaf0ff;
  padding: 30px 0;
}

.footer-row {
  display: flex;
  justify-content: space-between;
  gap: 18px;
  flex-wrap: wrap;
}

.footer p {
  margin: 6px 0;
  color: #bac7e4;
  font-size: .88rem;
}

.notice {
  color: var(--muted);
  font-size: .83rem;
  margin-top: 14px;
}

.hidden { display: none !important; }

.modal {
  position: fixed;
  inset: 0;
  background: #101a32aa;
  display: grid;
  place-items: center;
  padding: 16px;
  z-index: 10;
}

.modal-card {
  background: white;
  border-radius: 22px;
  padding: 24px;
  width: min(570px, 100%);
  max-height: 90vh;
  overflow: auto;
  box-shadow: 0 25px 80px #07132b44;
}

.modal-head {
  display: flex;
  justify-content: space-between;
  gap: 15px;
  align-items: start;
}

.close {
  border: 0;
  background: #eef2fb;
  border-radius: 10px;
  width: 38px;
  height: 38px;
  font-size: 1.2rem;
}

.answer {
  display: block;
  width: 100%;
  text-align: left;
  border: 1px solid var(--line);
  background: #fff;
  border-radius: 12px;
  padding: 12px;
  margin: 9px 0;
}

.answer:hover {
  border-color: var(--blue);
  background: #f4f7ff;
}

.answer.correct {
  border-color: #15956e;
  background: #e9f8f2;
}

.answer.wrong {
  border-color: #d65353;
  background: #fff0f0;
}

.feedback {
  font-weight: 750;
  margin: 12px 0;
}

.score-pill {
  background: #e9f8f2;
  color: #087657;
  border-radius: 12px;
  padding: 10px 13px;
  font-weight: 750;
  display: inline-block;
}

@media (max-width: 850px) {
  .hero-grid { grid-template-columns: 1fr; }
  .hero-art { min-height: 270px; }
  .levels { grid-template-columns: repeat(3, 1fr); }
  .subjects { grid-template-columns: repeat(2, 1fr); }
  .navlinks { gap: 12px; }
  .navlinks a:not(.btn) { display: none; }
}

@media (max-width: 560px) {
  .hero { padding-top: 25px; }
  .hero-art { min-height: 240px; }
  .levels { grid-template-columns: repeat(2, 1fr); }
  .subjects, .lesson-grid, .feature-grid {
    grid-template-columns: 1fr;
  }
  .section { padding: 35px 0; }
  .section-head {
    align-items: start;
    flex-direction: column;
  }
  .callout {
    align-items: start;
    flex-direction: column;
  }
  .level { padding: 14px; }
  .hero h1 { letter-spacing: -1.2px; }
  .nav .primary { padding: 10px 12px; }
  .trust { gap: 10px; }
}
</style>
</head>

<body>
<div class="topbar">
  🌍 Learn at your own pace — from your first lesson to university-level study.
</div>

<header class="wrap nav">
  <a class="brand" href="#home">
    <span class="logo">E</span> EduBrigde
  </a>
  <nav class="navlinks">
    <a href="#levels">Learning levels</a>
    <a href="#subjects">Subjects</a>
    <a href="#lessons">Try a lesson</a>
    <a class="btn primary" href="#subjects">Start learning →</a>
  </nav>
</header>

<main>
<section class="hero" id="home">
  <div class="wrap hero-grid">
    <div>
      <span class="eyebrow">✨ Your journey. Your future.</span>
      <h1>Make learning feel <span>possible.</span></h1>
      <p>
        Explore lessons, practise important skills, and build confidence —
        whether you're just starting school or preparing for university.
      </p>
      <div class="hero-actions">
        <a class="btn primary" href="#levels">Explore learning levels →</a>
        <a class="btn secondary" href="#lessons">Try a free lesson</a>
      </div>
      <div class="trust">
        <span>✓ Beginner-friendly</span>
        <span>✓ Learn at your pace</span>
        <span>✓ Made for mobile</span>
      </div>
    </div>

    <div class="hero-art" aria-label="Illustration of learning resources">
      <div class="orbit"></div>
      <div class="book">
        <span class="big">📚</span>
        <strong>Learn & grow</strong>
        <span style="color:#68758e;font-size:.8rem">One step at a time</span>
      </div>
      <div class="float f1">🧠 Keep curious</div>
      <div class="float f2">⭐ Practice daily</div>
      <div class="float f3">🎯 Reach your goals</div>
    </div>
  </div>
</section>

<section class="section wrap" id="levels">
  <div class="section-head">
    <div>
      <h2>Where are you on your learning journey?</h2>
      <p>Choose a level to explore learning pathways.</p>
    </div>
  </div>

  <div class="levels" id="levelCards">
    <button class="level active" data-level="All levels">
      <span class="emoji">🌈</span>
      <h3>All levels</h3>
      <p>Explore everything</p>
    </button>
    <button class="level" data-level="Kindergarten">
      <span class="emoji">🧸</span>
      <h3>Kindergarten</h3>
      <p>Play and discover</p>
    </button>
    <button class="level" data-level="Primary">
      <span class="emoji">✏️</span>
      <h3>Primary</h3>
      <p>Build foundations</p>
    </button>
    <button class="level" data-level="Secondary">
      <span class="emoji">🔭</span>
      <h3>Secondary</h3>
      <p>Grow your skills</p>
    </button>
    <button class="level" data-level="College & University">
      <span class="emoji">🎓</span>
      <h3>College & university</h3>
      <p>Study in depth</p>
    </button>
  </div>

  <p class="notice">
    Curriculum coverage and lesson libraries will grow over time.
    Choose your country below to help personalise your learning.
  </p>
</section>

<section class="section wrap" id="subjects">
  <div class="section-head">
    <div>
      <h2>Find your next subject</h2>
      <p>Choose a country and level, or search for a subject.</p>
    </div>
  </div>

  <div class="filterbar">
    <div class="field">
      <label for="country">Country / curriculum</label>
      <select id="country">
        <option value="International">International learning</option>
        <option>Kenya</option>
        <option>Uganda</option>
        <option>Tanzania</option>
        <option>Rwanda</option>
        <option>Nigeria</option>
        <option>South Africa</option>
        <option>United Kingdom</option>
        <option>United States</option>
        <option>India</option>
        <option>Other / not listed</option>
      </select>
    </div>

    <div class="field">
      <label for="levelSelect">Learning level</label>
      <select id="levelSelect">
        <option>All levels</option>
        <option>Kindergarten</option>
        <option>Primary</option>
        <option>Secondary</option>
        <option>College & University</option>
      </select>
    </div>

    <div class="field">
      <label for="search">Search subjects</label>
      <input id="search" type="search" placeholder="e.g. Biology, maths…">
    </div>
  </div>

  <div class="subjects" id="subjectCards">
    <article class="subject"
      data-name="mathematics maths numeracy"
      data-levels="Kindergarten,Primary,Secondary,College & University">
      <div class="subject-icon">🔢</div>
      <div>
        <h3>Mathematics</h3>
        <p>Numbers, patterns, sets and problem-solving.</p>
        <button class="btn primary open-lesson" data-subject="Mathematics">
          Learn & take quiz →
        </button>
      </div>
    </article>

    <article class="subject"
      data-name="languages english communication literacy"
      data-levels="Kindergarten,Primary,Secondary,College & University">
      <div class="subject-icon">🗣️</div>
      <div>
        <h3>Languages</h3>
        <p>Reading, writing, grammar and communication.</p>
        <button class="btn primary open-lesson" data-subject="Languages">
          Learn & take quiz →
        </button>
      </div>
    </article>

    <article class="subject"
      data-name="biology science plants animals cells genetics"
      data-levels="Primary,Secondary,College & University">
      <div class="subject-icon">🧬</div>
      <div>
        <h3>Biology</h3>
        <p>Cells, living organisms and the environment.</p>
        <button class="btn primary open-lesson" data-subject="Biology">
          Learn & take quiz →
        </button>
      </div>
    </article>

    <article class="subject"
      data-name="chemistry matter reactions atoms"
      data-levels="Secondary,College & University">
      <div class="subject-icon">⚗️</div>
      <div>
        <h3>Chemistry</h3>
        <p>Matter, atoms, substances and reactions.</p>
        <button class="btn primary open-lesson" data-subject="Chemistry">
          Learn & take quiz →
        </button>
      </div>
    </article>

    <article class="subject"
      data-name="physics energy forces motion electricity"
      data-levels="Primary,Secondary,College & University">
      <div class="subject-icon">⚛️</div>
      <div>
        <h3>Physics</h3>
        <p>Forces, energy, motion and the natural world.</p>
        <button class="btn primary open-lesson" data-subject="Physics">
          Learn & take quiz →
        </button>
      </div>
    </article>

    <article class="subject"
      data-name="computer studies computing digital technology"
      data-levels="Primary,Secondary,College & University">
      <div class="subject-icon">💻</div>
      <div>
        <h3>Computer Studies</h3>
        <p>Computers, software and digital skills.</p>
        <button class="btn primary open-lesson" data-subject="Computer Studies">
          Learn & take quiz →
        </button>
      </div>
    </article>
  </div>

  <p id="noResults" class="notice hidden">
    No subjects match your search. Try another word or choose a different level.
  </p>
  <p id="curriculumNote" class="notice">
    Choose a country to help personalise the subjects displayed.
  </p>
</section>

<section class="section wrap" id="lessons">
  <div class="section-head">
    <div>
      <h2>Start with a short lesson</h2>
      <p>Read a simple explanation, then answer a quick question.</p>
    </div>
  </div>

  <div class="lesson-area">
    <div class="lesson-grid">
      <article class="lesson">
        <span class="tag">MATHEMATICS · BEGINNER</span>
        <h3>What is a set?</h3>
        <p>
          A set is a well-defined collection of distinct objects.
          The objects are called elements or members.
        </p>
        <button class="btn primary open-lesson" data-subject="Mathematics">
          Learn & take quiz →
        </button>
      </article>

      <article class="lesson">
        <span class="tag">BIOLOGY · BEGINNER</span>
        <h3>What is a cell?</h3>
        <p>
          A cell is the basic structural and functional unit of life.
          Some organisms have one cell; others have many cells.
        </p>
        <button class="btn primary open-lesson" data-subject="Biology">
          Learn & take quiz →
        </button>
      </article>
    </div>
  </div>
</section>

<section class="section wrap">
  <div class="section-head">
    <div>
      <h2>Designed to help you keep going</h2>
      <p>A simple starting point for a bigger learning experience.</p>
    </div>
  </div>

  <div class="feature-grid">
    <article class="feature">
      <span class="emoji">🪜</span>
      <h3>Learn step by step</h3>
      <p>Start with the basics and work toward harder ideas when you're ready.</p>
    </article>
    <article class="feature">
      <span class="emoji">📝</span>
      <h3>Practise as you learn</h3>
      <p>Use quick questions to check your understanding and learn from mistakes.</p>
    </article>
    <article class="feature">
      <span class="emoji">🌍</span>
      <h3>Built for many learners</h3>
      <p>Our goal is to support different ages, countries, curricula and learning needs.</p>
    </article>
  </div>
</section>

<section class="wrap">
  <div class="callout">
    <div>
      <h2 style="margin:0">Small steps lead to big progress.</h2>
      <p>Choose a subject and begin with one lesson today.</p>
    </div>
    <a class="btn" href="#subjects">Choose a subject →</a>
  </div>
</section>
</main>

<footer class="footer">
  <div class="wrap footer-row">
    <div>
      <a class="brand" href="#home" style="color:white">
        <span class="logo">E</span> EduBrigde
      </a>
      <p>Learn without limits. Grow with confidence.</p>
    </div>
    <div>
      <strong>Explore</strong>
      <p>
        <a href="#levels" style="color:#bac7e4">Learning levels</a> ·
        <a href="#subjects" style="color:#bac7e4">Subjects</a> ·
        <a href="#lessons" style="color:#bac7e4">Lessons</a>
      </p>
      <p>© <span id="year"></span> EduBrigde · Learning prototype</p>
    </div>
  </div>
</footer>

<div id="modal" class="modal hidden" role="dialog" aria-modal="true"
  aria-labelledby="modalTitle">
  <div class="modal-card">
    <div class="modal-head">
      <div>
        <span class="tag" id="modalTag">QUICK LESSON</span>
        <h2 id="modalTitle" style="margin:0 0 8px">Lesson</h2>
      </div>
      <button class="close" id="closeModal" aria-label="Close lesson">×</button>
    </div>

    <div id="lessonText"></div>
    <hr style="border:0;border-top:1px solid var(--line);margin:20px 0">
    <h3 id="questionText">Quick check</h3>
    <div id="answers"></div>
    <div id="feedback" class="feedback" aria-live="polite"></div>
    <button id="nextQuestion" class="btn primary hidden">
      Try another question →
    </button>
    <p class="notice">
      This prototype gives feedback in this browser. It does not yet create
      accounts or save scores online.
    </p>
  </div>
</div>

<script>
const lessonData = {
  'Mathematics': {
    tag: 'MATHEMATICS · BEGINNER',
    title: 'What is a set?',
    text: `
      <p>A <strong>set</strong> is a well-defined collection of distinct objects.
      The objects are called <em>elements</em> or <em>members</em>.</p>
      <p>Example: A = {1, 2, 3}. The number 2 belongs to A, written 2 ∈ A.
      The number 5 does not belong to A, written 5 ∉ A.</p>
      <p><strong>Remember:</strong> in a set, repeated elements are written only once.</p>
    `,
    questions: [
      {
        q: 'Which option is a set of the first three positive integers?',
        a: ['{1, 2, 3}', '{one, many, some}', '{1, 1, 2, maybe}'],
        correct: 0,
        why: 'Correct! {1, 2, 3} is a clearly defined collection.'
      },
      {
        q: 'If A = {2, 4, 6}, is 4 ∈ A?',
        a: ['Yes', 'No'],
        correct: 0,
        why: 'Correct! The symbol ∈ means “is an element of”.'
      }
    ]
  },

  'Biology': {
    tag: 'BIOLOGY · BEGINNER',
    title: 'What is a cell?',
    text: `
      <p>A <strong>cell</strong> is the basic structural and functional unit of life.
      All living organisms are made of one or more cells.</p>
      <p>Some organisms, such as many bacteria, are unicellular (one cell).
      Humans and plants are multicellular (many cells).</p>
      <p>Many cells contain a cell membrane, cytoplasm and genetic material.
      Plant cells also typically have a cell wall, and many have chloroplasts.</p>
    `,
    questions: [
      {
        q: 'What is the basic unit of life?',
        a: ['An organ', 'A cell', 'A population'],
        correct: 1,
        why: 'Correct! The cell is the basic structural and functional unit of life.'
      },
      {
        q: 'Which structure is typically found in plant cells but not animal cells?',
        a: ['Cell membrane', 'Cytoplasm', 'Cell wall'],
        correct: 2,
        why: 'Correct! Plant cells have a cell wall outside the cell membrane.'
      }
    ]
  },

  'Languages': {
    tag: 'LANGUAGES · BEGINNER',
    title: 'Building a clear sentence',
    text: `
      <p>A sentence expresses a complete thought. In a simple English sentence,
      the <strong>subject</strong> tells us who or what the sentence is about,
      and the <strong>predicate</strong> tells us something about the subject.</p>
      <p>Example: “The learner reads.” Subject: “The learner”.
      Predicate: “reads”. A sentence normally begins with a capital letter
      and ends with suitable punctuation.</p>
    `,
    questions: [
      {
        q: 'Which is a complete sentence?',
        a: ['The clever student', 'The student reads.', 'Because the lesson'],
        correct: 1,
        why: 'Correct! “The student reads.” expresses a complete thought.'
      }
    ]
  },

  'Chemistry': {
    tag: 'CHEMISTRY · BEGINNER',
    title: 'What is matter?',
    text: `
      <p><strong>Matter</strong> is anything that has mass and occupies space.
      Common states of matter are solid, liquid and gas.</p>
      <p>A solid generally keeps its shape and volume. A liquid keeps its volume
      but takes the shape of its container. A gas spreads out to fill its container.</p>
    `,
    questions: [
      {
        q: 'Which state of matter takes the shape of its container but keeps a fixed volume?',
        a: ['Solid', 'Liquid', 'Gas'],
        correct: 1,
        why: 'Correct! A liquid takes the shape of its container while maintaining a fixed volume.'
      }
    ]
  },

  'Physics': {
    tag: 'PHYSICS · BEGINNER',
    title: 'What is force?',
    text: `
      <p>A <strong>force</strong> is a push or pull that can change an object’s
      motion or shape. Forces are measured in newtons (N).</p>
      <p>A balanced force does not change an object’s motion. An unbalanced
      force can cause an object to speed up, slow down or change direction.</p>
    `,
    questions: [
      {
        q: 'What is the SI unit of force?',
        a: ['Joule', 'Newton', 'Watt'],
        correct: 1,
        why: 'Correct! Force is measured in newtons (N).'
      }
    ]
  },

  'Computer Studies': {
    tag: 'COMPUTER STUDIES · BEGINNER',
    title: 'Hardware and software',
    text: `
      <p><strong>Hardware</strong> refers to the physical parts of a computer,
      such as a keyboard, screen or processor. <strong>Software</strong> refers
      to programs and instructions that tell the computer what to do.</p>
      <p>A keyboard is hardware. A word-processing application is software.</p>
    `,
    questions: [
      {
        q: 'Which is an example of hardware?',
        a: ['A keyboard', 'A spreadsheet app', 'A web browser'],
        correct: 0,
        why: 'Correct! A keyboard is a physical computer component.'
      }
    ]
  }
};

let activeLesson = null;
let questionIndex = 0;

const modal = document.getElementById('modal');

function openLesson(subject) {
  activeLesson = lessonData[subject] || lessonData['Mathematics'];
  questionIndex = 0;

  document.getElementById('modalTag').textContent = activeLesson.tag;
  document.getElementById('modalTitle').textContent = activeLesson.title;
  document.getElementById('lessonText').innerHTML = activeLesson.text;
  document.getElementById('nextQuestion').classList.add('hidden');

  showQuestion();
  modal.classList.remove('hidden');
  document.body.style.overflow = 'hidden';
}

function showQuestion() {
  const q = activeLesson.questions[
    questionIndex % activeLesson.questions.length
  ];

  document.getElementById('questionText').textContent = 'Quick check: ' + q.q;

  const box = document.getElementById('answers');
  box.innerHTML = '';
  document.getElementById('feedback').textContent = '';
  document.getElementById('nextQuestion').classList.add('hidden');

  q.a.forEach((answer, i) => {
    const b = document.createElement('button');
    b.className = 'answer';
    b.textContent = String.fromCharCode(65 + i) + '. ' + answer;

    b.onclick = () => {
      [...box.children].forEach(x => x.disabled = true);

      if (i === q.correct) {
        b.classList.add('correct');
        document.getElementById('feedback').textContent = '✅ ' + q.why;
      } else {
        b.classList.add('wrong');
        box.children[q.correct].classList.add('correct');
        document.getElementById('feedback').textContent =
          'Not quite. ' + q.why;
      }

      document.getElementById('nextQuestion').classList.remove('hidden');
    };

    box.appendChild(b);
  });
}

document.querySelectorAll('.open-lesson').forEach(b => {
  b.addEventListener('click', () => openLesson(b.dataset.subject));
});

document.getElementById('closeModal').onclick = () => {
  modal.classList.add('hidden');
  document.body.style.overflow = '';
};

modal.addEventListener('click', e => {
  if (e.target === modal) {
    modal.classList.add('hidden');
    document.body.style.overflow = '';
  }
});

document.getElementById('nextQuestion').onclick = () => {
  questionIndex++;
  showQuestion();
};

document.addEventListener('keydown', e => {
  if (e.key === 'Escape') {
    modal.classList.add('hidden');
    document.body.style.overflow = '';
  }
});

const country = document.getElementById('country');
const levelSelect = document.getElementById('levelSelect');
const search = document.getElementById('search');

function filterSubjects() {
  let count = 0;

  document.querySelectorAll('.subject').forEach(card => {
    const level = levelSelect.value;
    const terms = search.value.toLowerCase().trim();
    const names = card.dataset.name.toLowerCase();
    const levels = card.dataset.levels.split(',');

    const okLevel =
      level === 'All levels' || levels.includes(level);

    const okSearch =
      !terms ||
      names.includes(terms) ||
      card.querySelector('h3').textContent.toLowerCase().includes(terms);

    card.classList.toggle('hidden', !(okLevel && okSearch));

    if (okLevel && okSearch) count++;
  });

  document.getElementById('noResults').classList.toggle('hidden', count > 0);

  document.getElementById('curriculumNote').textContent =
    'Showing starter subjects for ' + country.value +
    '. Country selection is a starting preference; exact syllabus mapping ' +
    'will be added as the library grows.';
}

[levelSelect, search, country].forEach(el => {
  el.addEventListener('input', filterSubjects);
});

document.querySelectorAll('.level').forEach(card => {
  card.addEventListener('click', () => {
    document.querySelectorAll('.level').forEach(x =>
      x.classList.remove('active')
    );

    card.classList.add('active');
    levelSelect.value = card.dataset.level;
    filterSubjects();

    document.getElementById('subjects').scrollIntoView({
      behavior: 'smooth'
    });
  });
});

document.getElementById('year').textContent = new Date().getFullYear();
</script>
</body><div id="modal" class="modal hidden" rol
</html>

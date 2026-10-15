<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#173b8f">
<meta name="description" content="EduBridge helps learners worldwide study, practise and grow from kindergarten to university.">
<title>EduBridge | Learn Without Limits</title>

<style>
:root {
  --blue: #173b8f;
  --light: #edf4ff;
  --text: #17233d;
  --muted: #64748b;
  --white: #ffffff;
  --green: #138a63;
}

* { box-sizing: border-box; }

body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
  background: #f5f8ff;
  color: var(--text);
}

header {
  background: var(--blue);
  color: white;
  padding: 20px 16px;
}

.header-inner, main, footer {
  max-width: 850px;
  margin: auto;
}

.brand {
  font-size: 27px;
  font-weight: 800;
  letter-spacing: -.7px;
}

.brand span { color: #8ee4c0; }

.tagline {
  font-size: 13px;
  margin-top: 5px;
  color: #e0eaff;
}

main { padding: 22px 16px 40px; }

h1 {
  font-size: 29px;
  line-height: 1.2;
  margin: 12px 0;
}

h2 { font-size: 21px; }

p {
  line-height: 1.65;
  color: var(--muted);
}

.hero {
  background: linear-gradient(135deg, #e3edff, #e4fff3);
  border-radius: 22px;
  padding: 25px 20px;
  margin-bottom: 24px;
}

.hero .emoji {
  font-size: 40px;
  margin-bottom: 10px;
}

.hero p { color: #354866; }

button, select {
  font: inherit;
}

button {
  border: 0;
  cursor: pointer;
}

.primary {
  background: var(--blue);
  color: white;
  padding: 14px 19px;
  border-radius: 12px;
  font-weight: 700;
  width: 100%;
  margin-top: 12px;
}

.primary:hover { background: #102d70; }

.back {
  color: var(--blue);
  background: transparent;
  padding: 8px 0 16px;
  font-weight: 700;
}

.grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 12px;
  margin-top: 18px;
}

.card {
  background: white;
  border: 1px solid #e2eaf7;
  border-radius: 17px;
  padding: 18px 13px;
  text-align: left;
  min-height: 135px;
  box-shadow: 0 4px 14px #1b37610b;
}

.card:hover { border-color: #91b5ff; }

.card .emoji {
  font-size: 30px;
  display: block;
  margin-bottom: 13px;
}

.card strong {
  display: block;
  font-size: 15px;
  margin-bottom: 6px;
}

.card small {
  color: var(--muted);
  line-height: 1.4;
}

.panel {
  background: white;
  border: 1px solid #e2eaf7;
  padding: 20px;
  border-radius: 17px;
  margin-top: 18px;
}

label {
  display: block;
  font-weight: 700;
  margin: 18px 0 8px;
}

select {
  width: 100%;
  padding: 13px;
  border: 1px solid #ccd8eb;
  border-radius: 10px;
  background: white;
  color: var(--text);
}

.subject {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 15px 12px;
  background: white;
  border: 1px solid #e2eaf7;
  border-radius: 12px;
  margin: 10px 0;
  width: 100%;
  text-align: left;
  color: var(--text);
}

.subject .emoji { font-size: 25px; }

.lesson {
  background: #edf4ff;
  padding: 17px;
  border-radius: 12px;
  margin: 16px 0;
  line-height: 1.7;
}

.option {
  display: block;
  width: 100%;
  background: white;
  border: 1px solid #ccd8eb;
  border-radius: 10px;
  text-align: left;
  padding: 13px;
  margin: 9px 0;
  color: var(--text);
}

.option:focus, .option:hover {
  border-color: var(--blue);
}

.notice {
  padding: 13px;
  border-radius: 10px;
  background: #e5f8ef;
  color: #126346;
  margin-top: 14px;
  line-height: 1.5;
}

.hidden { display: none !important; }

footer {
  border-top: 1px solid #e2eaf7;
  padding: 22px 16px;
  color: var(--muted);
  font-size: 12px;
  text-align: center;
}

@media (min-width: 650px) {
  main { padding-top: 32px; }
  .hero { padding: 34px; }
  .grid { grid-template-columns: repeat(4, minmax(0, 1fr)); }
}
</style>
</head>

<body>

<header>
  <div class="header-inner">
    <div class="brand">Edu<span>Bridge</span> 🌍</div>
    <div class="tagline">Learn Today. Build Your Tomorrow.</div>
  </div>
</header>

<main>

<section id="home">
  <div class="hero">
    <div class="emoji">📚 🌍 🎓</div>
    <h1>Learning without limits.</h1>
    <p>
      Discover lessons, explore subjects and test your knowledge.
      Wherever you are on your educational journey, your next step
      starts here.
    </p>
    <button class="primary" onclick="show('levels')">
      Start Learning →
    </button>
  </div>

  <h2>One platform. Every stage.</h2>
  <p>Choose the learning pathway that's right for you.</p>

  <div class="grid">
    <button class="card" onclick="chooseLevel('Kindergarten')">
      <span class="emoji">🧸</span>
      <strong>Kindergarten</strong>
      <small>Letters, numbers and discovery</small>
    </button>

    <button class="card" onclick="chooseLevel('Primary School')">
      <span class="emoji">📘</span>
      <strong>Primary School</strong>
      <small>Build strong foundations</small>
    </button>

    <button class="card" onclick="chooseLevel('Secondary School')">
      <span class="emoji">🎒</span>
      <strong>Secondary School</strong>
      <small>Study and exam preparation</small>
    </button>

    <button class="card" onclick="chooseLevel('University')">
      <span class="emoji">🔬</span>
      <strong>University</strong>
      <small>Explore advanced subjects</small>
    </button>
  </div>
</section>

<section id="levels" class="hidden">
  <button class="back" onclick="show('home')">← Home</button>
  <h1>Choose your learning level</h1>
  <p>Start with the level that matches your studies.</p>

  <div class="grid">
    <button class="card" onclick="chooseLevel('Kindergarten')">
      <span class="emoji">🧸</span><strong>Kindergarten</strong>
    </button>
    <button class="card" onclick="chooseLevel('Primary School')">
      <span class="emoji">📘</span><strong>Primary School</strong>
    </button>
    <button class="card" onclick="chooseLevel('Secondary School')">
      <span class="emoji">🎒</span><strong>Secondary School</strong>
    </button>
    <button class="card" onclick="chooseLevel('University')">
      <span class="emoji">🎓</span><strong>University</strong>
    </button>
  </div>
</section>

<section id="curriculum" class="hidden">
  <button class="back" onclick="show('levels')">← Levels</button>
  <h1>Choose your curriculum</h1>
  <p id="selectedLevel"></p>

  <div class="panel">
    <label for="country">Country or learning pathway</label>
    <select id="country">
      <option value="International Learning">International Learning</option>
      <option value="Kenya">Kenya</option>
      <option value="United States">United States</option>
      <option value="United Kingdom">United Kingdom</option>
      <option value="India">India</option>
      <option value="Other Countries">Other Countries</option>
    </select>

    <label for="language">Preferred language</label>
    <select id="language">
      <option>English</option>
      <option>Kiswahili</option>
    </select>

    <button class="primary" onclick="continueToSubjects()">
      Explore Subjects →
    </button>
  </div>
</section>

<section id="subjects" class="hidden">
  <button class="back" onclick="show('curriculum')">← Curriculum</button>
  <h1>Explore your subjects</h1>
  <p id="subjectInfo"></p>
  <div id="subjectList"></div>
</section>

<section id="lesson" class="hidden">
  <button class="back" onclick="show('subjects')">← Subjects</button>
  <h1 id="lessonTitle">Your lesson</h1>
  <p id="lessonInfo"></p>

  <div class="panel">
    <h2>Welcome to your learning space!</h2>
    <p id="lessonIntro"></p>

    <div class="lesson">
      <strong>Learning tip 💡</strong><br>
      Read each topic carefully, write down key points and practise
      what you learn. Regular revision helps you remember information.
    </div>

    <h2>Test your knowledge</h2>
    <p id="question"></p>
    <div id="options"></div>
    <div id="quizResult" aria-live="polite"></div>
    <button class="primary" onclick="resetQuiz()">Try Again</button>
  </div>
</section>

</main>

<footer>
  EduBridge © 2026 · Learning Without Borders
  <br><br>
  This is an early demonstration. Curriculum content and advanced
  features will be added and verified as the platform develops.
</footer>

<script>
const sections = ['home', 'levels', 'curriculum', 'subjects', 'lesson'];

let currentLevel = '';
let currentSubject = '';
let correctAnswer = 1;
let answered = false;

function show(id) {
  sections.forEach(section => {
    document.getElementById(section).classList.toggle(
      'hidden', section !== id
    );
  });
  window.scrollTo(0, 0);
}

function chooseLevel(level) {
  currentLevel = level;
  document.getElementById('selectedLevel').textContent =
    'Your selected level: ' + level;
  show('curriculum');
}

function continueToSubjects() {
  const country = document.getElementById('country').value;
  const language = document.getElementById('language').value;

  document.getElementById('subjectInfo').textContent =
    currentLevel + ' · ' + country + ' · ' + language;

  const subjects = [
    ['🔢', 'Mathematics'],
    ['🗣️', 'Languages'],
    ['🧬', 'Biology'],
    ['⚗️', 'Chemistry'],
    ['⚛️', 'Physics'],
    ['💻', 'Computer Studies']
  ];

  const list = document.getElementById('subjectList');
  list.innerHTML = '';

  subjects.forEach(([emoji, subject]) => {
    const button = document.createElement('button');
    button.className = 'subject';
    button.innerHTML =
      '<span class="emoji">' + emoji + '</span><strong>' +
      subject + '</strong><span style="margin-left:auto">→</span>';
    button.onclick = () => openLesson(subject);
    list.appendChild(button);
  });

  show('subjects');
}

function openLesson(subject) {
  currentSubject = subject;
  document.getElementById('lessonTitle').textContent = subject;
  document.getElementById('lessonInfo').textContent =
    currentLevel + ' · ' +
    document.getElementById('country').value;

  const introductions = {
    'Mathematics':
      'Mathematics helps us understand numbers, patterns, shapes and relationships.',
    'Languages':
      'Languages help us communicate, read, write and understand other people.',
    'Biology':
      'Biology is the study of living organisms and their interactions with the environment.',
    'Chemistry':
      'Chemistry explores substances, their properties and how they change.',
    'Physics':
      'Physics studies matter, energy, motion and the natural world.',
    'Computer Studies':
      'Computer studies explores computers, digital systems and how technology works.'
  };

  document.getElementById('lessonIntro').textContent =
    introductions[subject] || 'Explore and learn something new today.';

  createQuiz(subject);
  show('lesson');
}

function createQuiz(subject) {
  let question = 'Which subject studies living organisms?';
  let options = ['Physics', 'Biology', 'Chemistry', 'Mathematics'];
  correctAnswer = 1;

  if (subject === 'Mathematics') {
    question = 'What is 7 + 5?';
    options = ['10', '11', '12', '13'];
    correctAnswer = 2;
  } else if (subject === 'Chemistry') {
    question = 'What is the chemical symbol for water?';
    options = ['CO₂', 'O₂', 'NaCl', 'H₂O'];
    correctAnswer = 3;
  } else if (subject === 'Physics') {
    question = 'Which force pulls objects toward Earth?';
    options = ['Gravity', 'Friction', 'Magnetism', 'Buoyancy'];
    correctAnswer = 0;
  } else if (subject === 'Languages') {
    question = 'Which word is a noun?';
    options = ['Quickly', 'Beautiful', 'Teacher', 'Run'];
    correctAnswer = 2;
  } else if (subject === 'Computer Studies') {
    question = 'Which device is commonly used to type text?';
    options = ['Monitor', 'Keyboard', 'Speaker', 'Printer'];
    correctAnswer = 1;
  }

  document.getElementById('question').textContent = question;
  document.getElementById('quizResult').textContent = '';
  document.getElementById('options').innerHTML = '';
  answered = false;

  options.forEach((option, index) => {
    const button = document.createElement('button');
    button.className = 'option';
    button.textContent =
      String.fromCharCode(65 + index) + '. ' + option;

    button.onclick = () => {
      if (answered) return;
      answered = true;

      const result = document.getElementById('quizResult');

      if (index === correctAnswer) {
        result.className = 'notice';
        result.textContent = 'Correct! Excellent work! 🎉';
      } else {
        result.className = 'notice';
        result.textContent =
          'Not quite. The correct answer is ' +
          String.fromCharCode(65 + correctAnswer) + '. ' +
          options[correctAnswer] + '. Keep practising!';
      }
    };

    document.getElementById('options').appendChild(button);
  });
}

function resetQuiz() {
  createQuiz(currentSubject);
}
</script>

</body>
</html># edubrigde-
learning platform 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#173b8f">
<meta name="description" content="EduBridge helps learners worldwide study, practise and grow from kindergarten to university.">
<title>EduBridge | Learn Without Limits</title>

<style>
:root {
  --blue: #173b8f;
  --light: #edf4ff;
  --text: #17233d;
  --muted: #64748b;
  --white: #ffffff;
  --green: #138a63;
}

* { box-sizing: border-box; }

body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
  background: #f5f8ff;
  color: var(--text);
}

header {
  background: var(--blue);
  color: white;
  padding: 20px 16px;
}

.header-inner, main, footer {
  max-width: 850px;
  margin: auto;
}

.brand {
  font-size: 27px;
  font-weight: 800;
  letter-spacing: -.7px;
}

.brand span { color: #8ee4c0; }

.tagline {
  font-size: 13px;
  margin-top: 5px;
  color: #e0eaff;
}

main { padding: 22px 16px 40px; }

h1 {
  font-size: 29px;
  line-height: 1.2;
  margin: 12px 0;
}

h2 { font-size: 21px; }

p {
  line-height: 1.65;
  color: var(--muted);
}

.hero {
  background: linear-gradient(135deg, #e3edff, #e4fff3);
  border-radius: 22px;
  padding: 25px 20px;
  margin-bottom: 24px;
}

.hero .emoji {
  font-size: 40px;
  margin-bottom: 10px;
}

.hero p { color: #354866; }

button, select {
  font: inherit;
}

button {
  border: 0;
  cursor: pointer;
}

.primary {
  background: var(--blue);
  color: white;
  padding: 14px 19px;
  border-radius: 12px;
  font-weight: 700;
  width: 100%;
  margin-top: 12px;
}

.primary:hover { background: #102d70; }

.back {
  color: var(--blue);
  background: transparent;
  padding: 8px 0 16px;
  font-weight: 700;
}

.grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 12px;
  margin-top: 18px;
}

.card {
  background: white;
  border: 1px solid #e2eaf7;
  border-radius: 17px;
  padding: 18px 13px;
  text-align: left;
  min-height: 135px;
  box-shadow: 0 4px 14px #1b37610b;
}

.card:hover { border-color: #91b5ff; }

.card .emoji {
  font-size: 30px;
  display: block;
  margin-bottom: 13px;
}

.card strong {
  display: block;
  font-size: 15px;
  margin-bottom: 6px;
}

.card small {
  color: var(--muted);
  line-height: 1.4;
}

.panel {
  background: white;
  border: 1px solid #e2eaf7;
  padding: 20px;
  border-radius: 17px;
  margin-top: 18px;
}

label {
  display: block;
  font-weight: 700;
  margin: 18px 0 8px;
}

select {
  width: 100%;
  padding: 13px;
  border: 1px solid #ccd8eb;
  border-radius: 10px;
  background: white;
  color: var(--text);
}

.subject {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 15px 12px;
  background: white;
  border: 1px solid #e2eaf7;
  border-radius: 12px;
  margin: 10px 0;
  width: 100%;
  text-align: left;
  color: var(--text);
}

.subject .emoji { font-size: 25px; }

.lesson {
  background: #edf4ff;
  padding: 17px;
  border-radius: 12px;
  margin: 16px 0;
  line-height: 1.7;
}

.option {
  display: block;
  width: 100%;
  background: white;
  border: 1px solid #ccd8eb;
  border-radius: 10px;
  text-align: left;
  padding: 13px;
  margin: 9px 0;
  color: var(--text);
}

.option:focus, .option:hover {
  border-color: var(--blue);
}

.notice {
  padding: 13px;
  border-radius: 10px;
  background: #e5f8ef;
  color: #126346;
  margin-top: 14px;
  line-height: 1.5;
}

.hidden { display: none !important; }

footer {
  border-top: 1px solid #e2eaf7;
  padding: 22px 16px;
  color: var(--muted);
  font-size: 12px;
  text-align: center;
}

@media (min-width: 650px) {
  main { padding-top: 32px; }
  .hero { padding: 34px; }
  .grid { grid-template-columns: repeat(4, minmax(0, 1fr)); }
}
</style>
</head>

<body>

<header>
  <div class="header-inner">
    <div class="brand">Edu<span>Bridge</span> 🌍</div>
    <div class="tagline">Learn Today. Build Your Tomorrow.</div>
  </div>
</header>

<main>

<section id="home">
  <div class="hero">
    <div class="emoji">📚 🌍 🎓</div>
    <h1>Learning without limits.</h1>
    <p>
      Discover lessons, explore subjects and test your knowledge.
      Wherever you are on your educational journey, your next step
      starts here.
    </p>
    <button class="primary" onclick="show('levels')">
      Start Learning →
    </button>
  </div>

  <h2>One platform. Every stage.</h2>
  <p>Choose the learning pathway that's right for you.</p>

  <div class="grid">
    <button class="card" onclick="chooseLevel('Kindergarten')">
      <span class="emoji">🧸</span>
      <strong>Kindergarten</strong>
      <small>Letters, numbers and discovery</small>
    </button>

    <button class="card" onclick="chooseLevel('Primary School')">
      <span class="emoji">📘</span>
      <strong>Primary School</strong>
      <small>Build strong foundations</small>
    </button>

    <button class="card" onclick="chooseLevel('Secondary School')">
      <span class="emoji">🎒</span>
      <strong>Secondary School</strong>
      <small>Study and exam preparation</small>
    </button>

    <button class="card" onclick="chooseLevel('University')">
      <span class="emoji">🔬</span>
      <strong>University</strong>
      <small>Explore advanced subjects</small>
    </button>
  </div>
</section>

<section id="levels" class="hidden">
  <button class="back" onclick="show('home')">← Home</button>
  <h1>Choose your learning level</h1>
  <p>Start with the level that matches your studies.</p>

  <div class="grid">
    <button class="card" onclick="chooseLevel('Kindergarten')">
      <span class="emoji">🧸</span><strong>Kindergarten</strong>
    </button>
    <button class="card" onclick="chooseLevel('Primary School')">
      <span class="emoji">📘</span><strong>Primary School</strong>
    </button>
    <button class="card" onclick="chooseLevel('Secondary School')">
      <span class="emoji">🎒</span><strong>Secondary School</strong>
    </button>
    <button class="card" onclick="chooseLevel('University')">
      <span class="emoji">🎓</span><strong>University</strong>
    </button>
  </div>
</section>

<section id="curriculum" class="hidden">
  <button class="back" onclick="show('levels')">← Levels</button>
  <h1>Choose your curriculum</h1>
  <p id="selectedLevel"></p>

  <div class="panel">
    <label for="country">Country or learning pathway</label>
    <select id="country">
      <option value="International Learning">International Learning</option>
      <option value="Kenya">Kenya</option>
      <option value="United States">United States</option>
      <option value="United Kingdom">United Kingdom</option>
      <option value="India">India</option>
      <option value="Other Countries">Other Countries</option>
    </select>

    <label for="language">Preferred language</label>
    <select id="language">
      <option>English</option>
      <option>Kiswahili</option>
    </select>

    <button class="primary" onclick="continueToSubjects()">
      Explore Subjects →
    </button>
  </div>
</section>

<section id="subjects" class="hidden">
  <button class="back" onclick="show('curriculum')">← Curriculum</button>
  <h1>Explore your subjects</h1>
  <p id="subjectInfo"></p>
  <div id="subjectList"></div>
</section>

<section id="lesson" class="hidden">
  <button class="back" onclick="show('subjects')">← Subjects</button>
  <h1 id="lessonTitle">Your lesson</h1>
  <p id="lessonInfo"></p>

  <div class="panel">
    <h2>Welcome to your learning space!</h2>
    <p id="lessonIntro"></p>

    <div class="lesson">
      <strong>Learning tip 💡</strong><br>
      Read each topic carefully, write down key points and practise
      what you learn. Regular revision helps you remember information.
    </div>

    <h2>Test your knowledge</h2>
    <p id="question"></p>
    <div id="options"></div>
    <div id="quizResult" aria-live="polite"></div>
    <button class="primary" onclick="resetQuiz()">Try Again</button>
  </div>
</section>

</main>

<footer>
  EduBridge © 2026 · Learning Without Borders
  <br><br>
  This is an early demonstration. Curriculum content and advanced
  features will be added and verified as the platform develops.
</footer>

<script>
const sections = ['home', 'levels', 'curriculum', 'subjects', 'lesson'];

let currentLevel = '';
let currentSubject = '';
let correctAnswer = 1;
let answered = false;

function show(id) {
  sections.forEach(section => {
    document.getElementById(section).classList.toggle(
      'hidden', section !== id
    );
  });
  window.scrollTo(0, 0);
}

function chooseLevel(level) {
  currentLevel = level;
  document.getElementById('selectedLevel').textContent =
    'Your selected level: ' + level;
  show('curriculum');
}

function continueToSubjects() {
  const country = document.getElementById('country').value;
  const language = document.getElementById('language').value;

  document.getElementById('subjectInfo').textContent =
    currentLevel + ' · ' + country + ' · ' + language;

  const subjects = [
    ['🔢', 'Mathematics'],
    ['🗣️', 'Languages'],
    ['🧬', 'Biology'],
    ['⚗️', 'Chemistry'],
    ['⚛️', 'Physics'],
    ['💻', 'Computer Studies']
  ];

  const list = document.getElementById('subjectList');
  list.innerHTML = '';

  subjects.forEach(([emoji, subject]) => {
    const button = document.createElement('button');
    button.className = 'subject';
    button.innerHTML =
      '<span class="emoji">' + emoji + '</span><strong>' +
      subject + '</strong><span style="margin-left:auto">→</span>';
    button.onclick = () => openLesson(subject);
    list.appendChild(button);
  });

  show('subjects');
}

function openLesson(subject) {
  currentSubject = subject;
  document.getElementById('lessonTitle').textContent = subject;
  document.getElementById('lessonInfo').textContent =
    currentLevel + ' · ' +
    document.getElementById('country').value;

  const introductions = {
    'Mathematics':
      'Mathematics helps us understand numbers, patterns, shapes and relationships.',
    'Languages':
      'Languages help us communicate, read, write and understand other people.',
    'Biology':
      'Biology is the study of living organisms and their interactions with the environment.',
    'Chemistry':
      'Chemistry explores substances, their properties and how they change.',
    'Physics':
      'Physics studies matter, energy, motion and the natural world.',
    'Computer Studies':
      'Computer studies explores computers, digital systems and how technology works.'
  };

  document.getElementById('lessonIntro').textContent =
    introductions[subject] || 'Explore and learn something new today.';

  createQuiz(subject);
  show('lesson');
}

function createQuiz(subject) {
  let question = 'Which subject studies living organisms?';
  let options = ['Physics', 'Biology', 'Chemistry', 'Mathematics'];
  correctAnswer = 1;

  if (subject === 'Mathematics') {
    question = 'What is 7 + 5?';
    options = ['10', '11', '12', '13'];
    correctAnswer = 2;
  } else if (subject === 'Chemistry') {
    question = 'What is the chemical symbol for water?';
    options = ['CO₂', 'O₂', 'NaCl', 'H₂O'];
    correctAnswer = 3;
  } else if (subject === 'Physics') {
    question = 'Which force pulls objects toward Earth?';
    options = ['Gravity', 'Friction', 'Magnetism', 'Buoyancy'];
    correctAnswer = 0;
  } else if (subject === 'Languages') {
    question = 'Which word is a noun?';
    options = ['Quickly', 'Beautiful', 'Teacher', 'Run'];
    correctAnswer = 2;
  } else if (subject === 'Computer Studies') {
    question = 'Which device is commonly used to type text?';
    options = ['Monitor', 'Keyboard', 'Speaker', 'Printer'];
    correctAnswer = 1;
  }

  document.getElementById('question').textContent = question;
  document.getElementById('quizResult').textContent = '';
  document.getElementById('options').innerHTML = '';
  answered = false;

  options.forEach((option, index) => {
    const button = document.createElement('button');
    button.className = 'option';
    button.textContent =
      String.fromCharCode(65 + index) + '. ' + option;

    button.onclick = () => {
      if (answered) return;
      answered = true;

      const result = document.getElementById('quizResult');

      if (index === correctAnswer) {
        result.className = 'notice';
        result.textContent = 'Correct! Excellent work! 🎉';
      } else {
        result.className = 'notice';
        result.textContent =
          'Not quite. The correct answer is ' +
          String.fromCharCode(65 + correctAnswer) + '. ' +
          options[correctAnswer] + '. Keep practising!';
      }
    };

    document.getElementById('options').appendChild(button);
  });
}

function resetQuiz() {
  createQuiz(currentSubject);
}
</script>

</body>
</html>

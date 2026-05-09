<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lexicon — Typing Mastery</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=DM+Mono:wght@300;400&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0c0c0e;
    --surface: #13131a;
    --border: #1e1e2e;
    --gold: #c9a96e;
    --gold-dim: #8a6e42;
    --cream: #f0ead8;
    --muted: #5a5a7a;
    --correct: #6eb89a;
    --wrong: #c9556e;
    --cursor: #c9a96e;
  }

  body {
    background: var(--bg);
    color: var(--cream);
    font-family: 'Cormorant Garamond', serif;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 2rem;
    overflow: hidden;
  }

  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.04'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 0;
  }

  body::after {
    content: '';
    position: fixed;
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    width: 700px; height: 400px;
    background: radial-gradient(ellipse, rgba(201,169,110,0.05) 0%, transparent 70%);
    pointer-events: none;
    z-index: 0;
  }

  .wrapper {
    position: relative; z-index: 1;
    width: 100%; max-width: 760px;
    display: flex; flex-direction: column;
    align-items: center; gap: 2.5rem;
  }

  header { text-align: center; animation: fadeDown 0.8s ease both; }

  .brand {
    font-size: 2.8rem; font-weight: 300;
    letter-spacing: 0.35em; color: var(--gold); text-transform: uppercase;
  }

  .brand-sub {
    font-size: 0.78rem; font-family: 'DM Mono', monospace;
    letter-spacing: 0.2em; color: var(--muted);
    text-transform: uppercase; margin-top: 0.2rem;
  }

  .stats { display: flex; gap: 3rem; animation: fadeDown 0.9s 0.1s ease both; }
  .stat { text-align: center; }

  .stat-value {
    font-size: 2.2rem; font-weight: 300; color: var(--gold);
    line-height: 1; font-variant-numeric: tabular-nums; transition: transform 0.15s;
  }

  .stat-label {
    font-size: 0.65rem; font-family: 'DM Mono', monospace;
    letter-spacing: 0.15em; color: var(--muted);
    text-transform: uppercase; margin-top: 0.3rem;
  }

  .divider { width: 1px; height: 40px; background: var(--border); }

  .modes {
    display: flex; gap: 0.5rem;
    background: var(--surface); border: 1px solid var(--border);
    border-radius: 2px; padding: 4px;
    animation: fadeDown 0.9s 0.15s ease both;
  }

  .mode-btn {
    font-family: 'DM Mono', monospace; font-size: 0.7rem;
    letter-spacing: 0.1em; padding: 0.45rem 1.1rem;
    border: none; background: transparent; color: var(--muted);
    cursor: pointer; border-radius: 1px; transition: all 0.2s; text-transform: uppercase;
  }

  .mode-btn.active { background: var(--gold); color: var(--bg); }

  .timer-bar-wrap {
    width: 100%; height: 2px; background: var(--border);
    border-radius: 1px; overflow: hidden;
    animation: fadeDown 0.9s 0.2s ease both;
  }

  .timer-bar {
    height: 100%;
    background: linear-gradient(90deg, var(--gold-dim), var(--gold));
    width: 100%; transition: width 0.25s linear;
  }

  .text-box {
    width: 100%; background: var(--surface);
    border: 1px solid var(--border); border-radius: 2px;
    padding: 2rem 2.2rem; position: relative;
    animation: fadeDown 0.9s 0.25s ease both; cursor: text;
  }

  .text-display {
    font-size: 1.45rem; font-weight: 300;
    line-height: 2; letter-spacing: 0.02em;
    user-select: none; word-break: break-word;
  }

  .char { position: relative; color: var(--muted); transition: color 0.05s; }
  .char.correct { color: var(--cream); }
  .char.wrong { color: var(--wrong); text-decoration: underline; text-decoration-color: var(--wrong); }

  .char.cursor::before {
    content: ''; position: absolute;
    left: -1px; top: 0.1em; bottom: 0.1em;
    width: 2px; background: var(--cursor);
    border-radius: 1px; animation: blink 1s step-end infinite;
  }

  @keyframes blink { 0%,100% { opacity:1; } 50% { opacity:0; } }

  #hidden-input {
    position: absolute; opacity: 0; pointer-events: none;
    top: 0; left: 0; width: 1px; height: 1px;
  }

  .result-overlay {
    position: absolute; inset: 0;
    background: rgba(12,12,14,0.96); border-radius: 2px;
    display: none; flex-direction: column;
    align-items: center; justify-content: center; gap: 1rem;
  }

  .result-overlay.visible { display: flex; animation: fadeIn 0.4s ease; }
  .result-wpm { font-size: 4rem; font-weight: 300; color: var(--gold); line-height: 1; }

  .result-label {
    font-family: 'DM Mono', monospace; font-size: 0.7rem;
    letter-spacing: 0.2em; color: var(--muted); text-transform: uppercase;
  }

  .result-details { font-family: 'DM Mono', monospace; font-size: 0.75rem; color: var(--muted); margin-top: 0.5rem; }

  .controls { display: flex; gap: 1rem; animation: fadeDown 0.9s 0.3s ease both; }

  .btn {
    font-family: 'DM Mono', monospace; font-size: 0.7rem;
    letter-spacing: 0.15em; text-transform: uppercase;
    padding: 0.6rem 1.6rem; border: 1px solid var(--border);
    background: transparent; color: var(--muted);
    cursor: pointer; border-radius: 1px; transition: all 0.2s;
  }

  .btn:hover { border-color: var(--gold); color: var(--gold); }
  .btn.primary { border-color: var(--gold); color: var(--gold-dim); background: rgba(201,169,110,0.06); }
  .btn.primary:hover { background: rgba(201,169,110,0.14); color: var(--gold); }

  .hint {
    font-family: 'DM Mono', monospace; font-size: 0.62rem;
    letter-spacing: 0.12em; color: var(--muted);
    opacity: 0.5; text-transform: uppercase;
    animation: fadeDown 0.9s 0.35s ease both;
  }

  @keyframes fadeDown { from { opacity:0; transform:translateY(-10px); } to { opacity:1; transform:translateY(0); } }
  @keyframes fadeIn { from { opacity:0; } to { opacity:1; } }
  @keyframes shake { 0%,100% { transform:translateX(0); } 25% { transform:translateX(-4px); } 75% { transform:translateX(4px); } }
  .shake { animation: shake 0.2s ease; }
</style>
</head>
<body>
<div class="wrapper">
  <header>
    <div class="brand">Lexicon</div>
    <div class="brand-sub">Typing Mastery</div>
  </header>

  <div class="stats">
    <div class="stat">
      <div class="stat-value" id="wpm-display">—</div>
      <div class="stat-label">WPM</div>
    </div>
    <div class="divider"></div>
    <div class="stat">
      <div class="stat-value" id="acc-display">—</div>
      <div class="stat-label">Accuracy</div>
    </div>
    <div class="divider"></div>
    <div class="stat">
      <div class="stat-value" id="time-display">30</div>
      <div class="stat-label">Seconds</div>
    </div>
  </div>

  <div class="modes">
    <button class="mode-btn active" data-time="15">15s</button>
    <button class="mode-btn" data-time="30">30s</button>
    <button class="mode-btn" data-time="60">60s</button>
    <button class="mode-btn" data-time="120">120s</button>
  </div>

  <div class="timer-bar-wrap">
    <div class="timer-bar" id="timer-bar"></div>
  </div>

  <div class="text-box" id="text-box" onclick="focusInput()">
    <div class="text-display" id="text-display"></div>
    <input id="hidden-input" type="text" autocomplete="off" autocorrect="off" autocapitalize="off" spellcheck="false">
    <div class="result-overlay" id="result-overlay">
      <div class="result-label">Final WPM</div>
      <div class="result-wpm" id="final-wpm">0</div>
      <div class="result-details" id="final-details"></div>
    </div>
  </div>

  <div class="controls">
    <button class="btn primary" id="restart-btn">↺ &nbsp;Restart</button>
  </div>

  <div class="hint">Click the text area or press Tab to focus · Tab+Enter to restart</div>
</div>

<script>
const WORDS = [
  "the","be","to","of","and","a","in","that","have","it","for","not","on","with",
  "he","as","you","do","at","this","but","his","by","from","they","we","say",
  "her","she","or","an","will","my","one","all","would","there","their","what",
  "so","up","out","if","about","who","get","which","go","me","when","make","can",
  "like","time","no","just","him","know","take","people","into","year","your",
  "good","some","could","them","see","other","than","then","now","look","only",
  "come","its","over","think","also","back","after","use","two","how","our","work",
  "first","well","way","even","new","want","because","any","these","give","day",
  "most","us","great","between","need","large","often","hand","high","place","hold",
  "turn","fact","though","less","public","next","early","keep","children","feet",
  "land","side","without","boy","once","animal","life","enough","took","four",
  "head","above","kind","began","almost","live","page","got","earth","light","hear",
  "story","point","city","play","small","number","off","always","move","try","kind",
  "hand","picture","again","change","off","play","spell","air","away","animal",
  "house","point","page","letter","mother","answer","found","study","still","learn",
  "plant","cover","food","sun","four","between","state","keep","eye","never","last"
];

let gameWords=[], typed='', correctChars=0, wrongChars=0;
let timer=null, timeLeft=30, totalTime=30, started=false, finished=false;

const textDisplay=document.getElementById('text-display');
const hiddenInput=document.getElementById('hidden-input');
const wpmDisplay=document.getElementById('wpm-display');
const accDisplay=document.getElementById('acc-display');
const timeDisplay=document.getElementById('time-display');
const timerBar=document.getElementById('timer-bar');
const resultOverlay=document.getElementById('result-overlay');
const finalWpm=document.getElementById('final-wpm');
const finalDetails=document.getElementById('final-details');
const textBox=document.getElementById('text-box');

function shuffle(arr) {
  const a=[...arr];
  for(let i=a.length-1;i>0;i--){const j=Math.floor(Math.random()*(i+1));[a[i],a[j]]=[a[j],a[i]];}
  return a;
}

function generateWords() {
  const pool=shuffle(WORDS), repeated=[];
  while(repeated.length<120) repeated.push(...pool);
  return repeated.slice(0,120).map(w=>w+' ');
}

function buildDisplay() {
  textDisplay.innerHTML='';
  const flat=gameWords.join('');
  for(let i=0;i<flat.length;i++){
    const span=document.createElement('span');
    span.className='char'+(i===0?' cursor':'');
    span.textContent=flat[i];
    span.dataset.index=i;
    textDisplay.appendChild(span);
  }
}

function getCharEl(i){return textDisplay.querySelector(`[data-index="${i}"]`);}

function updateDisplay() {
  const flat=gameWords.join('');
  textDisplay.querySelectorAll('.char').forEach(el=>{el.className='char';});
  for(let i=0;i<typed.length;i++){
    const el=getCharEl(i);
    if(el) el.className='char '+(typed[i]===flat[i]?'correct':'wrong');
  }
  const cursorEl=getCharEl(typed.length);
  if(cursorEl){cursorEl.classList.add('cursor');cursorEl.scrollIntoView({block:'nearest',behavior:'smooth'});}
}

function calcWpm(){const e=(totalTime-timeLeft)/60;return e===0?0:Math.round((correctChars/5)/e);}
function calcAcc(){const t=correctChars+wrongChars;return t===0?100:Math.round((correctChars/t)*100);}

function updateStats(){
  if(!started)return;
  wpmDisplay.textContent=calcWpm();
  accDisplay.textContent=calcAcc()+'%';
}

function startTimer(){
  if(timer)return;
  started=true;
  timer=setInterval(()=>{
    timeLeft--;
    timeDisplay.textContent=timeLeft;
    timerBar.style.width=(timeLeft/totalTime*100)+'%';
    updateStats();
    if(timeLeft<=0)endGame();
  },1000);
}

function endGame(){
  clearInterval(timer);timer=null;finished=true;hiddenInput.blur();
  const wpm=calcWpm(),acc=calcAcc();
  finalWpm.textContent=wpm;
  finalDetails.textContent=`${acc}% accuracy · ${correctChars} correct chars`;
  resultOverlay.classList.add('visible');
  wpmDisplay.textContent=wpm;accDisplay.textContent=acc+'%';
}

function init(){
  clearInterval(timer);timer=null;timeLeft=totalTime;
  started=false;finished=false;typed='';correctChars=0;wrongChars=0;
  hiddenInput.value='';gameWords=generateWords();buildDisplay();
  wpmDisplay.textContent='—';accDisplay.textContent='—';
  timeDisplay.textContent=totalTime;timerBar.style.width='100%';
  timerBar.style.transition='none';
  setTimeout(()=>timerBar.style.transition='width 0.25s linear',50);
  resultOverlay.classList.remove('visible');focusInput();
}

function focusInput(){hiddenInput.focus();}

hiddenInput.addEventListener('input',()=>{
  if(finished)return;
  const flat=gameWords.join(''),val=hiddenInput.value;
  if(!started&&val.length>0)startTimer();
  const oldLen=typed.length,newLen=val.length;
  if(newLen>oldLen){
    for(let i=oldLen;i<newLen;i++){
      if(val[i]===flat[i]){correctChars++;}
      else{wrongChars++;textBox.classList.remove('shake');void textBox.offsetWidth;textBox.classList.add('shake');}
    }
  }else if(newLen<oldLen){
    for(let i=newLen;i<oldLen;i++){
      if(typed[i]===flat[i])correctChars=Math.max(0,correctChars-1);
      else wrongChars=Math.max(0,wrongChars-1);
    }
  }
  typed=val;
  if(typed.length>=flat.length){typed=typed.slice(0,flat.length);hiddenInput.value=typed;endGame();return;}
  updateDisplay();updateStats();
});

hiddenInput.addEventListener('keydown',e=>{
  if(e.key==='Tab'){e.preventDefault();init();}
  if(e.key==='Escape')init();
});

document.addEventListener('keydown',e=>{
  if(e.key==='Tab'){e.preventDefault();init();}
  if(e.key===' '&&e.target!==hiddenInput)e.preventDefault();
});

document.querySelectorAll('.mode-btn').forEach(btn=>{
  btn.addEventListener('click',()=>{
    document.querySelectorAll('.mode-btn').forEach(b=>b.classList.remove('active'));
    btn.classList.add('active');totalTime=parseInt(btn.dataset.time);init();
  });
});

document.getElementById('restart-btn').addEventListener('click',init);
init();
</script>
</body>
</html>

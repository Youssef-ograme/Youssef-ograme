[inzo_game_intro.html](https://github.com/user-attachments/files/27185429/inzo_game_intro.html)

<style>
@keyframes scanline {
  0% { transform: translateY(-100%); }
  100% { transform: translateY(100vh); }
}
@keyframes glitch1 {
  0%,100% { clip-path: inset(0 0 95% 0); transform: translate(-4px); }
  50% { clip-path: inset(30% 0 50% 0); transform: translate(4px); }
}
@keyframes glitch2 {
  0%,100% { clip-path: inset(60% 0 10% 0); transform: translate(4px); }
  50% { clip-path: inset(10% 0 80% 0); transform: translate(-4px); }
}
@keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
@keyframes iconPop {
  0% { transform: scale(0) rotate(-10deg); opacity: 0; }
  70% { transform: scale(1.2) rotate(3deg); opacity: 1; }
  100% { transform: scale(1) rotate(0deg); opacity: 1; }
}
@keyframes flicker {
  0%,19%,21%,23%,25%,54%,56%,100% { opacity: 1; }
  20%,24%,55% { opacity: 0.4; }
}
.icon-item {
  display: inline-flex; flex-direction: column; align-items: center; gap: 6px;
  opacity: 0;
}
.icon-item img { width: 46px; height: 46px; transition: transform 0.3s; }
.icon-item:hover img { transform: translateY(-6px) scale(1.15); }
.icon-item span { font-size: 10px; color: #1D9E75; font-family: monospace; }
</style>

<div id="root" style="font-family: monospace; background: #0a0a0a; border-radius: 12px; overflow: hidden; position: relative; min-height: 420px; display: flex; flex-direction: column; align-items: center; justify-content: center; padding: 2rem;">

<div id="scanline" style="position: absolute; top: 0; left: 0; right: 0; height: 60px; background: linear-gradient(transparent, rgba(29,158,117,0.07), transparent); animation: scanline 3s linear infinite; pointer-events: none; z-index: 10;"></div>

<div id="phase1" style="text-align: center; width: 100%;">
  <div id="countdown" style="font-size: 72px; font-weight: 500; color: #1D9E75; letter-spacing: 8px; animation: flicker 2s infinite;">3</div>
  <div style="font-size: 12px; color: #5DCAA5; letter-spacing: 4px; margin-top: 8px;">INITIALIZING</div>
</div>

<div id="phase2" style="display:none; text-align: center; width: 100%;">
  <div style="position: relative; display: inline-block;">
    <div id="glitch-text" style="font-size: 42px; font-weight: 500; color: #1D9E75; letter-spacing: 6px;">INZO</div>
    <div id="glitch-a" style="position:absolute;top:0;left:0;font-size:42px;font-weight:500;color:#E24B4A;letter-spacing:6px;animation:glitch1 0.3s infinite;pointer-events:none;">INZO</div>
    <div id="glitch-b" style="position:absolute;top:0;left:0;font-size:42px;font-weight:500;color:#378ADD;letter-spacing:6px;animation:glitch2 0.3s infinite;pointer-events:none;">INZO</div>
  </div>
  <div style="font-size: 12px; color: #5DCAA5; letter-spacing: 4px; margin-top: 8px;">STUDENT @ 1337 — 42 NETWORK</div>
</div>

<div id="phase3" style="display:none; width: 100%; max-width: 400px; text-align: center;">
  <div style="font-size: 12px; color: #5DCAA5; letter-spacing: 3px; margin-bottom: 12px;">LOADING SKILLS</div>
  <div style="background: #111; border: 0.5px solid #1D9E75; border-radius: 4px; height: 10px; overflow: hidden;">
    <div id="loadbar" style="height: 100%; width: 0%; background: #1D9E75; transition: width 0.05s linear;"></div>
  </div>
  <div id="loadpct" style="font-size: 11px; color: #1D9E75; margin-top: 8px;">0%</div>
</div>

<div id="phase4" style="display:none; width: 100%; text-align: center;">
  <div style="font-size: 11px; color: #5DCAA5; letter-spacing: 3px; margin-bottom: 1.5rem;">LANGUAGES & TOOLS</div>
  <div style="display: flex; flex-wrap: wrap; gap: 20px; justify-content: center;" id="icons-container">
    <div class="icon-item"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg"/><span>C</span></div>
    <div class="icon-item"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg"/><span>C++</span></div>
    <div class="icon-item"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg"/><span>Python</span></div>
    <div class="icon-item"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bash/bash-original.svg"/><span>Bash</span></div>
    <div class="icon-item"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg"/><span>Linux</span></div>
    <div class="icon-item"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg"/><span>Git</span></div>
    <div class="icon-item"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vim/vim-original.svg"/><span>Vim</span></div>
  </div>
  <div id="final-text" style="display:none; margin-top: 1.5rem; font-size: 11px; color: #1D9E75; letter-spacing: 2px; animation: flicker 3s infinite;">[ CODING IN PROGRESS... ]</div>
  <div style="margin-top: 1rem; display: none;" id="btns">
    <button onclick="restart()" style="font-family: monospace; font-size: 12px; background: transparent; border: 0.5px solid #1D9E75; color: #1D9E75; padding: 6px 16px; cursor: pointer; border-radius: 4px; margin-right: 8px;">restart</button>
    <button onclick="copyReadme()" style="font-family: monospace; font-size: 12px; background: transparent; border: 0.5px solid #1D9E75; color: #1D9E75; padding: 6px 16px; cursor: pointer; border-radius: 4px;">copy README.md</button>
  </div>
</div>

</div>

<script>
let allTimeouts = [];
function T(fn, ms) { let t = setTimeout(fn, ms); allTimeouts.push(t); return t; }

function show(id) {
  ['phase1','phase2','phase3','phase4'].forEach(p => {
    document.getElementById(p).style.display = p === id ? 'block' : 'none';
  });
}

function restart() {
  allTimeouts.forEach(clearTimeout); allTimeouts = [];
  document.querySelectorAll('.icon-item').forEach(el => { el.style.opacity = 0; el.style.animation = ''; });
  document.getElementById('loadbar').style.width = '0%';
  document.getElementById('loadpct').textContent = '0%';
  document.getElementById('final-text').style.display = 'none';
  document.getElementById('btns').style.display = 'none';
  run();
}

function run() {
  show('phase1');
  const cd = document.getElementById('countdown');
  cd.textContent = '3';
  T(() => { cd.textContent = '2'; }, 1000);
  T(() => { cd.textContent = '1'; }, 2000);
  T(() => { cd.textContent = '0'; }, 3000);
  T(() => { show('phase2'); }, 3500);
  T(() => { show('phase3'); startLoad(); }, 5500);
}

function startLoad() {
  let pct = 0;
  const bar = document.getElementById('loadbar');
  const pctEl = document.getElementById('loadpct');
  function tick() {
    if (pct >= 100) { T(() => showIcons(), 300); return; }
    pct += Math.floor(Math.random() * 4) + 1;
    if (pct > 100) pct = 100;
    bar.style.width = pct + '%';
    pctEl.textContent = pct + '%';
    T(tick, 40);
  }
  tick();
}

function showIcons() {
  show('phase4');
  const icons = document.querySelectorAll('.icon-item');
  icons.forEach((el, i) => {
    T(() => {
      el.style.animation = 'iconPop 0.5s ease forwards';
      el.style.opacity = 1;
    }, i * 150);
  });
  T(() => { document.getElementById('final-text').style.display = 'block'; }, icons.length * 150 + 300);
  T(() => { document.getElementById('btns').style.display = 'block'; }, icons.length * 150 + 600);
}

function copyReadme() {
  const readme = `\`\`\`
  INZO — student @ 1337 (42 network)
  [ CODING IN PROGRESS... ]
\`\`\`

### languages & tools
<p align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" width="46"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg" width="46"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="46"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bash/bash-original.svg" width="46"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" width="46"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" width="46"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vim/vim-original.svg" width="46"/>
</p>`;
  navigator.clipboard.writeText(readme);
  event.target.textContent = 'copied!';
  setTimeout(() => event.target.textContent = 'copy README.md', 2000);
}

run();
</script>

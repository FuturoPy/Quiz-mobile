<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover" />
<meta name="apple-mobile-web-app-capable" content="yes" />
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent" />
<title>Quiz Escolar 🎓</title>
<style>
  :root{
    --bg:#000;
    --white: #ffffff;
    --accent: #00ffff;
    --panel: rgba(0,0,0,0.72);
    --btn-h: 56px;
    --safe-top: env(safe-area-inset-top);
    --safe-bottom: env(safe-area-inset-bottom);
  }

  /* Reset */
  *{box-sizing:border-box}
  html,body{height:100%;margin:0;background:var(--bg);-webkit-text-size-adjust:100%;-webkit-tap-highlight-color:transparent}
  body{font-family:"Comic Sans MS",Arial,Helvetica,sans-serif;color:var(--white);overflow:hidden;padding-top:var(--safe-top)}

  /* Tela inicial */
  #tela-inicial{
    position:fixed;inset:0;background-image:url('https://uploads.onecompiler.io/444jywmud/444jyqxv3/inico%20de%20tela.png');
    background-size:cover;background-position:center;display:flex;align-items:center;justify-content:center;transition:opacity .5s ease;
  }
  #particles{position:fixed;inset:0;pointer-events:none;z-index:1}

  /* Start button */
  #start-btn{
    position:fixed;left:50%;transform:translateX(-50%);bottom:calc(24px + var(--safe-bottom));
    font-size:18px;font-weight:700;color:var(--white);background:rgba(0,0,0,0.6);border:2px solid rgba(255,255,255,0.12);
    padding:12px 28px;border-radius:14px;z-index:10;min-height:var(--btn-h);display:flex;align-items:center;gap:12px;
    box-shadow:0 6px 20px rgba(0,0,0,0.6);
  }
  #start-btn:active{transform:translateX(-50%) scale(.98)}

  /* Container quiz (center) */
  .quiz-container{
    display:none; position:fixed; inset:0; padding:16px; align-items:center; justify-content:center;
    background-image:url('https://uploads.onecompiler.io/444jywmud/444jyqxv3/sala%20de%20aulas.png'); background-size:cover; background-position:center; transition:opacity .5s ease;
  }

  /* layout adaptável: mobile portrait: vertical stack; landscape/tablet: side-by-side */
  .area-jogo{
    width:100%;
    max-width:1100px;
    display:flex;
    gap:18px;
    align-items:center;
    justify-content:center;
    padding-bottom:calc(32px + var(--safe-bottom));
  }

  /* professor frame */
  .professor{
    width:38vw; max-width:300px; min-width:160px; height:auto;
    aspect-ratio: 3/4;
    background-size:contain; background-repeat:no-repeat; background-position:bottom center;
    animation: idle 3s ease-in-out infinite; display:none;
    flex-shrink:0;
  }

  /* quadro (onde ficam perguntas/respostas) */
  .quadro-fundo{
    flex:1;
    min-width:220px;
    background:linear-gradient(180deg, rgba(0,0,0,0.45), rgba(0,0,0,0.65));
    border-radius:18px; padding:18px; box-shadow: 0 8px 24px rgba(0,0,0,0.6);
    display:flex;flex-direction:column;align-items:center;justify-content:flex-start;
    gap:8px;
    max-height:80vh;
    overflow:auto;
  }
  #question{ font-size:clamp(18px, 4vw, 22px); text-align:center; margin:6px 6px 14px; line-height:1.3; }
  #answers{display:flex;flex-direction:column;gap:12px;width:100%;align-items:center;padding-bottom:8px}
  #answers button{
    width:92%; max-width:560px;
    padding:14px 18px; font-size:16px; border-radius:12px; border:2px solid rgba(255,255,255,0.12);
    background:transparent; color:var(--white); text-align:center; cursor:pointer;
    min-height:48px; display:flex; align-items:center; justify-content:center;
    transition:transform .15s ease, background .15s ease;
  }
  #answers button:active{transform:scale(.99)}
  #answers button:hover{ background: rgba(255,255,255,0.06) }
  .feedback{ font-size:18px; margin-top:8px; text-shadow:0 1px 4px rgba(0,0,0,0.8) }
  .feedback.correct{ color:#8ef5c9 }
  .feedback.wrong{ color:#ffb3b3 }

  /* Professor login and editor panel */
  #professor-login, #cadastro-perguntas{
    position:fixed; left:50%; transform:translateX(-50%); z-index:30;
    background:var(--panel); padding:12px; border-radius:14px; color:var(--white);
    width:calc(100% - 40px); max-width:760px; box-shadow:0 10px 30px rgba(0,0,0,0.6);
    margin-top:12px;
  }
  #professor-login input{ padding:10px 12px; border-radius:10px; border:none; width:60%; max-width:360px; margin-right:8px }
  #professor-login button{ padding:10px 12px; border-radius:10px; cursor:pointer; }

  #cadastro-perguntas h3{ margin:0 0 8px; font-size:16px }
  #cadastro-perguntas input, #cadastro-perguntas select{ width:100%; padding:10px 12px; margin:6px 0; border-radius:10px; border:none; }
  #cadastro-perguntas .row{display:flex;gap:8px}
  #cadastro-perguntas .row input{flex:1}
  #cadastro-perguntas button{ padding:10px 14px; border-radius:10px; cursor:pointer }

  /* Botão Sair edição */
  #btn-sair-edicao{
    position:fixed; top:calc(8px + var(--safe-top)); right:12px; z-index:40; display:none;
    background:#ff5252; color:white; border:none; padding:10px 12px; border-radius:10px; font-weight:700;
    box-shadow:0 6px 18px rgba(0,0,0,0.5);
  }

  /* tela final (overlay) */
  #tela-fim{
    position:fixed; inset:0; display:flex;align-items:center;justify-content:center; background:linear-gradient(180deg, rgba(0,0,0,0.45), rgba(0,0,0,0.8)); z-index:80;
    color:white; text-align:center; padding:20px;
  }

  /* Responsividade adicionais */
  @media(min-width:900px){
    .area-jogo{ padding:32px; gap:26px }
    .professor{ width:300px }
    #start-btn{ font-size:20px; padding:14px 34px}
  }
  @media(max-width:420px){
    #answers button{ font-size:15px; min-height:52px; border-radius:12px }
    .professor{ display:none } /* ocultar professora em telas muito pequenas para mais espaço */
  }

  /* animações */
  @keyframes idle{0%{transform:translateY(0)}50%{transform:translateY(-4px)}100%{transform:translateY(0)}}
</style>
</head>
<body>

<!-- Tela Inicial + partículas -->
<div id="tela-inicial">
  <canvas id="particles"></canvas>
</div>
<button id="start-btn" aria-label="Iniciar Quiz">START</button>

<!-- Login professor -->
<div id="professor-login" role="dialog" aria-label="Acesso do professor">
  <input id="senha-professor" type="password" placeholder="Senha professor (ex: 2702)" aria-label="Senha do professor" />
  <button onclick="entrarProfessor()">Entrar</button>
  <small style="display:block;opacity:.7;margin-top:6px">Somente professor pode editar. Toque START para os alunos iniciarem.</small>
</div>

<!-- Editor perguntas (visível só ao professor) -->
<div id="cadastro-perguntas" style="display:none">
  <h3>Adicionar / Editar Pergunta</h3>
  <input id="nova-pergunta" type="text" placeholder="Digite a pergunta" />
  <div class="row">
    <input id="alt1" type="text" placeholder="Alternativa 1" />
    <input id="alt2" type="text" placeholder="Alternativa 2" />
  </div>
  <input id="alt3" type="text" placeholder="Alternativa 3" />
  <select id="certa" aria-label="Alternativa correta">
    <option value="0">Alternativa 1</option>
    <option value="1">Alternativa 2</option>
    <option value="2">Alternativa 3</option>
  </select>
  <div style="display:flex;gap:8px;margin-top:8px">
    <button onclick="adicionarPergunta()">Adicionar Pergunta</button>
    <button onclick="exportarPerguntas()">Exportar (JSON)</button>
    <button onclick="importarPerguntas()">Importar (JSON)</button>
  </div>
  <div id="lista-perguntas" style="margin-top:10px"></div>
</div>

<!-- Botão Sair edição -->
<button id="btn-sair-edicao" onclick="sairEdicao()">SAIR</button>

<!-- Quiz -->
<div class="quiz-container" id="quiz-container" role="application" aria-label="Quiz">
  <div class="area-jogo">
    <div class="professor" id="professor" aria-hidden="true"></div>
    <div class="quadro-fundo" role="region" aria-live="polite">
      <div id="question" aria-label="Pergunta"></div>
      <div id="answers" role="list"></div>
      <div id="feedback" class="feedback" aria-atomic="true"></div>
    </div>
  </div>
</div>

<!-- tela final (criada dinamicamente) -->

<script>
/* ---------------- PARTICULAS (simples e leves) ---------------- */
const canvas = document.getElementById('particles'), ctx = canvas.getContext('2d');
function resizeCanvas(){ canvas.width = innerWidth; canvas.height = innerHeight; }
resizeCanvas(); addEventListener('resize', resizeCanvas);
let mouse={x:null,y:null}; addEventListener('touchmove', e=>{ const t=e.touches[0]; mouse.x=t.clientX; mouse.y=t.clientY }, {passive:true});
addEventListener('mousemove', e=>{ mouse.x=e.clientX; mouse.y=e.clientY });
class Particle{ constructor(){ this.x=Math.random()*canvas.width; this.y=Math.random()*canvas.height; this.size=Math.random()*1.8+0.8; this.base=this.size; this.vx=(Math.random()-0.5)*0.4; this.vy=(Math.random()-0.5)*0.4; this.o=Math.random()*0.6+0.2 } update(){ this.x+=this.vx; this.y+=this.vy; if(this.x<0||this.x>canvas.width)this.vx*=-1; if(this.y<0||this.y>canvas.height)this.vy*=-1; if(mouse.x&&mouse.y){ const dx=mouse.x-this.x, dy=mouse.y-this.y, d=Math.sqrt(dx*dx+dy*dy); if(d<80){ this.size=this.base+(80-d)/40; this.o=Math.min(1, this.o+(80-d)/200)} else{ this.size=this.base; this.o=this.o } } } draw(){ ctx.beginPath(); ctx.fillStyle='rgba(255,255,150,'+this.o+')'; ctx.arc(this.x,this.y,this.size,0,Math.PI*2); ctx.fill(); } }
const parts=[]; for(let i=0;i<60;i++) parts.push(new Particle());
(function loop(){ ctx.clearRect(0,0,canvas.width,canvas.height); parts.forEach(p=>{p.update();p.draw()}); requestAnimationFrame(loop) })();

/* ---------------- APP LOGIC ---------------- */
let imgFrames = [
  "https://uploads.onecompiler.io/444jywmud/444jyqxv3/professora%20frame%201.png",
  "https://uploads.onecompiler.io/444jywmud/444jyqxv3/professora%20frame%202.png",
  "https://uploads.onecompiler.io/444jywmud/444jyqxv3/professora%20frame%203.png"
];
let imgCerta = "https://uploads.onecompiler.io/444jywmud/444jyqxv3/joinhaa.png";
let imgErrada = "https://uploads.onecompiler.io/444jywmud/444jyqxv3/errada.png";

let perguntas = [], indice=0, pontuacao=0, escreverVelocidade=60;
const professorEl = document.getElementById('professor');
const feedbackEl = document.getElementById('feedback');
const quizContainer = document.getElementById('quiz-container');
const telaInicial = document.getElementById('tela-inicial');
const startBtn = document.getElementById('start-btn');
const btnSair = document.getElementById('btn-sair-edicao');
const listaPerguntasEl = document.getElementById('lista-perguntas');

/* Load from localStorage */
function salvarPerguntas(){ try{ localStorage.setItem('perguntasQuiz', JSON.stringify(perguntas)); }catch(e){ console.warn(e) } }
function carregarPerguntas(){ const d = localStorage.getItem('perguntasQuiz'); if(d){ try{ perguntas = JSON.parse(d) || []; atualizarCadastro(); }catch(e){ console.warn('JSON inválido') } } }
carregarPerguntas();

/* Editor / Professor */
function entrarProfessor(){
  const senha = document.getElementById('senha-professor').value.trim();
  if(senha === "2702"){ // sua senha
    document.getElementById('cadastro-perguntas').style.display = 'block';
    btnSair.style.display = 'block';
    document.getElementById('professor-login').style.display = 'none';
    atualizarCadastro();
    // mostrar professor visualmente (opcional)
    professorEl.style.display = 'block';
    professorEl.style.backgroundImage = `url(${imgFrames[0]})`;
  } else {
    alert('Senha incorreta');
  }
}
function sairEdicao(){
  document.getElementById('cadastro-perguntas').style.display = 'none';
  document.getElementById('professor-login').style.display = 'block';
  document.getElementById('senha-professor').value = '';
  btnSair.style.display = 'none';
}

/* Add / Edit / Remove */
function adicionarPergunta(){
  const pergunta = document.getElementById('nova-pergunta').value.trim();
  const op1 = document.getElementById('alt1').value.trim();
  const op2 = document.getElementById('alt2').value.trim();
  const op3 = document.getElementById('alt3').value.trim();
  const certa = parseInt(document.getElementById('certa').value,10);
  if(!pergunta || !op1 || !op2 || !op3) { alert('Preencha todos os campos'); return; }
  perguntas.push({pergunta, opcoes:[op1,op2,op3], certa});
  document.getElementById('nova-pergunta').value=''; document.getElementById('alt1').value=''; document.getElementById('alt2').value=''; document.getElementById('alt3').value='';
  salvarPerguntas(); atualizarCadastro();
}

/* update list with edit/delete actions */
function atualizarCadastro(){
  listaPerguntasEl.innerHTML = '';
  perguntas.forEach((p,i)=>{
    const item = document.createElement('div');
    item.style.display='flex'; item.style.justifyContent='space-between'; item.style.alignItems='center';
    item.style.padding='8px'; item.style.borderTop='1px dashed rgba(255,255,255,0.06)';
    const left = document.createElement('div');
    left.innerHTML = `<strong>${i+1}.</strong> ${p.pergunta}`;
    const right = document.createElement('div');
    right.style.display='flex'; right.style.gap='8px';
    const edit = document.createElement('button'); edit.textContent='Editar'; edit.style.padding='6px 8px'; edit.onclick = ()=>{ // populate editor then remove original
      document.getElementById('nova-pergunta').value = p.pergunta;
      document.getElementById('alt1').value = p.opcoes[0];
      document.getElementById('alt2').value = p.opcoes[1];
      document.getElementById('alt3').value = p.opcoes[2];
      document.getElementById('certa').value = p.certa;
      perguntas.splice(i,1);
      salvarPerguntas(); atualizarCadastro();
    };
    const del = document.createElement('button'); del.textContent='Remover'; del.style.padding='6px 8px'; del.onclick = ()=>{
      if(confirm('Remover pergunta?')){ perguntas.splice(i,1); salvarPerguntas(); atualizarCadastro(); }
    };
    right.appendChild(edit); right.appendChild(del);
    item.appendChild(left); item.appendChild(right);
    listaPerguntasEl.appendChild(item);
  });
}

/* Export / Import JSON (para você colocar no Github) */
function exportarPerguntas(){
  const data = JSON.stringify(perguntas, null, 2);
  // cria cópia para download
  const blob = new Blob([data], {type:'application/json'});
  const url = URL.createObjectURL(blob);
  const a = document.createElement('a'); a.href = url; a.download = 'perguntas-quiz.json';
  document.body.appendChild(a); a.click(); a.remove(); URL.revokeObjectURL(url);
}
function importarPerguntas(){
  const input = document.createElement('input'); input.type='file'; input.accept='application/json';
  input.onchange = e => {
    const f = e.target.files[0]; if(!f) return;
    const reader = new FileReader();
    reader.onload = ev => {
      try{
        const arr = JSON.parse(ev.target.result);
        if(Array.isArray(arr)){ perguntas = arr; salvarPerguntas(); atualizarCadastro(); alert('Importado com sucesso'); }
        else alert('JSON inválido');
      }catch(er){ alert('Não foi possível ler o arquivo'); }
    };
    reader.readAsText(f);
  };
  input.click();
}

/* START quiz */
startBtn.addEventListener('click', ()=>{
  if(perguntas.length===0){ alert('Adicione pelo menos uma pergunta antes de iniciar.'); return; }
  telaInicial.style.opacity = 0;
  setTimeout(()=>{ telaInicial.style.display='none'; document.getElementById('professor-login').style.display='none'; document.getElementById('cadastro-perguntas').style.display='none'; btnSair.style.display='none'; quizContainer.style.display='flex'; setTimeout(()=>quizContainer.style.opacity=1,50); professorEl.style.display = 'block'; professorEl.style.backgroundImage = `url(${imgFrames[0]})`; mostrarPergunta(); }, 450);
});

/* writing animation */
let escreverIntervalo = null;
function escreverNoQuadro(el, texto){
  el.textContent = '';
  if(escreverIntervalo) clearInterval(escreverIntervalo);
  return new Promise(resolve=>{
    let i=0, frame=0;
    escreverIntervalo = setInterval(()=>{
      el.textContent += texto[i] || '';
      professorEl.style.backgroundImage = `url(${imgFrames[frame]})`;
      frame = (frame+1)%imgFrames.length;
      i++;
      if(i >= texto.length){ clearInterval(escreverIntervalo); escreverIntervalo=null; professorEl.style.backgroundImage = `url(${imgFrames[0]})`; resolve(); }
    }, escreverVelocidade);
  });
}

async function mostrarPergunta(){
  if(!perguntas[indice]) { mostrarFim(); return; }
  const q = perguntas[indice];
  const respostasDiv = document.getElementById('answers'); respostasDiv.innerHTML = ''; feedbackEl.textContent='';
  await escreverNoQuadro(document.getElementById('question'), q.pergunta);
  q.opcoes.forEach((opt, i)=>{
    const b = document.createElement('button');
    b.textContent = opt;
    b.setAttribute('role','listitem');
    b.onclick = ()=> checkAnswer(i === q.certa, b);
    respostasDiv.appendChild(b);
  });
}

/* resposta */
function checkAnswer(certa, btnEl){
  professorEl.style.animation = '';
  if(certa){
    pontuacao++; feedbackEl.textContent = 'Muito bem!'; feedbackEl.className = 'feedback correct';
    professorEl.style.backgroundImage = `url(${imgCerta})`; professorEl.style.animation = 'jump 0.6s';
    setTimeout(()=>{ professorEl.style.animation = 'idle 3s ease-in-out infinite'; professorEl.style.backgroundImage = `url(${imgFrames[0]})`; indice++; if(indice < perguntas.length) mostrarPergunta(); else mostrarFim(); }, 600);
  } else {
    feedbackEl.textContent = 'Tente novamente!'; feedbackEl.className = 'feedback wrong';
    professorEl.style.backgroundImage = `url(${imgErrada})`; professorEl.style.animation = 'shake 0.5s';
    setTimeout(()=>{ professorEl.style.animation = 'idle 3s ease-in-out infinite'; professorEl.style.backgroundImage = `url(${imgFrames[0]})`; indice++; if(indice < perguntas.length) mostrarPergunta(); else mostrarFim(); }, 500);
  }
}

/* fim e reset */
function mostrarFim(){
  quizContainer.style.display = 'none';
  const fimDiv = document.createElement('div'); fimDiv.id='tela-fim';
  fimDiv.innerHTML = '';
  if(pontuacao === perguntas.length){
    const txt = document.createElement('div'); txt.innerHTML = `Parabéns! Você desbloqueou uma conquista: <b>Nota 10</b><br>`; txt.style.marginBottom='12px'; fimDiv.appendChild(txt);
    const img = document.createElement('img'); img.src='https://uploads.onecompiler.io/444jywmud/444jyqxv3/Captura%20de%20tela%202025-11-14%20003933.png'; img.style.width='160px'; img.style.borderRadius='12px'; fimDiv.appendChild(img);
  } else {
    const txt = document.createElement('div'); txt.innerHTML = `Fim do Quiz! Você acertou ${pontuacao} de ${perguntas.length}.`; txt.style.marginBottom='12px'; fimDiv.appendChild(txt);
  }
  const btn = document.createElement('button'); btn.textContent='Voltar'; btn.style.marginTop='18px'; btn.style.padding='12px 18px'; btn.onclick = ()=>{ fimDiv.remove(); resetarJogo(); };
  fimDiv.appendChild(btn);
  document.body.appendChild(fimDiv);
}

function resetarJogo(){
  telaInicial.style.display = 'flex'; telaInicial.style.opacity = 1;
  indice = 0; pontuacao = 0;
  quizContainer.style.display = 'none';
  document.getElementById('question').textContent=''; document.getElementById('answers').innerHTML=''; feedbackEl.textContent='';
  const fimExist = document.getElementById('tela-fim'); if(fimExist) fimExist.remove();
}

/* ESC para sair do modo professor (ou botão SAIR) */
document.addEventListener('keydown', (e)=>{ if(e.key === 'Escape') sairEdicao(); });

/* Accessibility: focus start button for easier keyboard users */
startBtn.focus();
</script>

</body>
</html>

<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Transformasi Geometri – Matematika Kelas 9</title>
<style>
:root{--bg:#f6f5ff;--card:#fff;--tx:#1d1b3a;--mut:#615f85;--pri:#6c4cf5;--pri2:#ff5c8a;--ok:#12a36b;--bad:#e5484d;--line:#e3e0f7;--grid:#e6e3f8;--axis:#8a86b5;
box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#13112a;--card:#1d1a3d;--tx:#f0eeff;--mut:#a9a6d3;--pri:#8f78ff;--pri2:#ff7aa2;--ok:#3ddc97;--bad:#ff6b70;--line:#332f66;--grid:#2a2655;--axis:#7f7bb8;color-scheme:dark}}
:root[data-theme="dark"]{--bg:#13112a;--card:#1d1a3d;--tx:#f0eeff;--mut:#a9a6d3;--pri:#8f78ff;--pri2:#ff7aa2;--ok:#3ddc97;--bad:#ff6b70;--line:#332f66;--grid:#2a2655;--axis:#7f7bb8;color-scheme:dark}
html{scroll-padding-top:env(safe-area-inset-top,0px);scroll-behavior:smooth}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--tx);font:16px/1.6 system-ui,-apple-system,"Segoe UI",Roboto,sans-serif}
.wrap{max-width:900px;margin:0 auto;padding:16px}
.hero{background:linear-gradient(135deg,var(--pri),var(--pri2));color:#fff;border-radius:24px;padding:32px 24px;margin:8px 0 20px}
.hero h1{margin:0 0 6px;font-size:clamp(1.6rem,5vw,2.4rem);line-height:1.2}
.hero p{margin:0;opacity:.95}
.badge{display:inline-block;background:rgba(255,255,255,.22);padding:2px 12px;border-radius:99px;font-size:.8rem;margin-bottom:10px}
nav{display:flex;gap:8px;margin-bottom:16px}
nav button{flex:1;padding:12px;border:2px solid var(--line);background:var(--card);color:var(--tx);border-radius:14px;font:inherit;font-weight:700;cursor:pointer}
nav button.on{background:var(--pri);border-color:var(--pri);color:#fff}
.card{background:var(--card);border:1px solid var(--line);border-radius:20px;padding:20px;margin-bottom:16px}
h2{margin:0 0 8px;font-size:1.3rem}
.tabs{display:flex;gap:6px;flex-wrap:wrap;margin-bottom:14px}
.tabs button{padding:8px 14px;border-radius:99px;border:1px solid var(--line);background:transparent;color:var(--tx);font:inherit;font-size:.9rem;cursor:pointer}
.tabs button.on{background:var(--pri2);border-color:var(--pri2);color:#fff;font-weight:700}
.lab{display:grid;gap:16px;grid-template-columns:1fr}
@media(min-width:720px){.lab{grid-template-columns:1.1fr 1fr}}
canvas{width:100%;aspect-ratio:1;border-radius:14px;background:var(--card);border:1px solid var(--line);display:block}
.ctl label{display:flex;justify-content:space-between;font-weight:600;margin-top:10px}
.ctl input[type=range]{width:100%;accent-color:var(--pri)}
.ctl select{width:100%;padding:10px;border-radius:10px;border:1px solid var(--line);background:var(--card);color:var(--tx);font:inherit}
.formula{background:var(--bg);border-left:4px solid var(--pri);border-radius:10px;padding:10px 14px;margin:12px 0;font-family:ui-monospace,Menlo,monospace;font-size:.92rem}
.coords{font-size:.9rem;color:var(--mut)}
.legend span{display:inline-block;margin-right:12px;font-size:.85rem}
.dot{display:inline-block;width:10px;height:10px;border-radius:3px;margin-right:4px}
/* quiz */
.top{display:flex;justify-content:space-between;align-items:center;font-weight:700;margin-bottom:8px}
.bar{height:10px;background:var(--line);border-radius:99px;overflow:hidden;margin-bottom:18px}
.bar i{display:block;height:100%;width:0;background:linear-gradient(90deg,var(--pri),var(--pri2));transition:width .4s}
.q{font-size:1.15rem;font-weight:700;margin-bottom:14px}
.opt{display:block;width:100%;text-align:left;padding:14px 16px;margin-bottom:10px;border-radius:14px;border:2px solid var(--line);background:var(--card);color:var(--tx);font:inherit;cursor:pointer;transition:transform .15s,border-color .15s}
.opt:hover:not(:disabled){transform:translateX(4px);border-color:var(--pri)}
.opt.ok{border-color:var(--ok);background:color-mix(in srgb,var(--ok) 18%,var(--card))}
.opt.bad{border-color:var(--bad);background:color-mix(in srgb,var(--bad) 18%,var(--card));animation:sh .3s}
@keyframes sh{25%{transform:translateX(-6px)}75%{transform:translateX(6px)}}
.fb{padding:12px 14px;border-radius:12px;background:var(--bg);margin:6px 0 12px;display:none}
.btn{padding:12px 22px;border:0;border-radius:14px;background:linear-gradient(90deg,var(--pri),var(--pri2));color:#fff;font:inherit;font-weight:700;cursor:pointer}
.res{text-align:center;padding:10px 0}
.res .big{font-size:4rem;line-height:1.1}
.res .score{font-size:2.4rem;font-weight:800;color:var(--pri)}
.hide{display:none}
.pop{animation:pop .5s}
@keyframes pop{0%{transform:scale(.6);opacity:0}100%{transform:scale(1);opacity:1}}
</style>
</head>
<body>
<div class="wrap">
  <header class="hero">
    <span class="badge">Matematika · Kelas 9</span>
    <h1>Transformasi Geometri</h1>
    <p>Geser, cerminkan, putar, dan perbesar bangun datar. Coba sendiri di laboratorium, lalu uji kemampuanmu di kuis.</p>
  </header>
  <nav>
    <button class="on" data-v="belajar">🔬 Belajar</button>
    <button data-v="kuis">🎮 Kuis</button>
  </nav>

  <section id="belajar">
    <div class="card">
      <h2>Laboratorium Transformasi</h2>
      <div class="tabs" id="tabs"></div>
      <div class="lab">
        <div><canvas id="cv"></canvas>
          <div class="legend" style="margin-top:8px"><span><i class="dot" style="background:#6c4cf5"></i>Bayangan awal ABC</span><span><i class="dot" style="background:#ff5c8a"></i>Bayangan A’B’C’</span></div></div>
        <div>
          <div class="ctl" id="ctl"></div>
          <div class="formula" id="fm"></div>
          <div class="coords" id="co"></div>
        </div>
      </div>
    </div>
    <div class="card" id="teori"></div>
  </section>

  <section id="kuis" class="hide">
    <div class="card" id="quiz"></div>
  </section>
</div>

<script>
const $=s=>document.querySelector(s);
/* ---------- navigasi ---------- */
document.querySelectorAll('nav button').forEach(b=>b.onclick=()=>{
  document.querySelectorAll('nav button').forEach(x=>x.classList.toggle('on',x===b));
  $('#belajar').classList.toggle('hide',b.dataset.v!=='belajar');
  $('#kuis').classList.toggle('hide',b.dataset.v!=='kuis');
  if(b.dataset.v==='belajar')draw();
});

/* ---------- laboratorium ---------- */
const P=[[1,1],[4,1],[1,3]],N=['A','B','C'],R=8;
const st={t:'translasi',a:3,b:-2,ref:'x',rot:90,k:2};
const TYPES={translasi:'Translasi (Pergeseran)',refleksi:'Refleksi (Pencerminan)',rotasi:'Rotasi (Perputaran)',dilatasi:'Dilatasi (Perkalian)'};
const REFS={x:['Sumbu x',([x,y])=>[x,-y],'(x, y) → (x, −y)'],y:['Sumbu y',([x,y])=>[-x,y],'(x, y) → (−x, y)'],yx:['Garis y = x',([x,y])=>[y,x],'(x, y) → (y, x)'],ynx:['Garis y = −x',([x,y])=>[-y,-x],'(x, y) → (−y, −x)']};
const rd=v=>Math.round(v*100)/100+0;
function rot([x,y],d){const r=d*Math.PI/180,c=Math.cos(r),s=Math.sin(r);return[rd(x*c-y*s),rd(x*s+y*c)]}
function tf(p){
  if(st.t==='translasi')return[p[0]+st.a,p[1]+st.b];
  if(st.t==='refleksi')return REFS[st.ref][1](p);
  if(st.t==='rotasi')return rot(p,st.rot);
  return[rd(p[0]*st.k),rd(p[1]*st.k)];
}
function formula(){
  if(st.t==='translasi')return`T = (${st.a}, ${st.b})<br>(x, y) → (x ${st.a<0?'−':'+'} ${Math.abs(st.a)}, y ${st.b<0?'−':'+'} ${Math.abs(st.b)})`;
  if(st.t==='refleksi')return`Cermin: ${REFS[st.ref][0]}<br>${REFS[st.ref][2]}`;
  if(st.t==='rotasi'){const f={90:'(x, y) → (−y, x)',180:'(x, y) → (−x, −y)',270:'(x, y) → (y, −x)',0:'(x, y) → (x, y)'}[st.rot];return`Rotasi ${st.rot}° berlawanan arah jarum jam, pusat O(0, 0)<br>${f}`}
  return`Dilatasi pusat O(0, 0), faktor skala k = ${st.k}<br>(x, y) → (${st.k}x, ${st.k}y)`;
}
function controls(){
  const c=$('#ctl');
  if(st.t==='translasi')c.innerHTML=`<label>Geser horizontal (a) <b id="va">${st.a}</b></label><input type="range" id="ra" min="-6" max="6" value="${st.a}"><label>Geser vertikal (b) <b id="vb">${st.b}</b></label><input type="range" id="rb" min="-6" max="6" value="${st.b}">`;
  else if(st.t==='refleksi')c.innerHTML=`<label>Pilih cermin</label><select id="sr">${Object.entries(REFS).map(([k,v])=>`<option value="${k}" ${k===st.ref?'selected':''}>${v[0]}</option>`).join('')}</select>`;
  else if(st.t==='rotasi')c.innerHTML=`<label>Sudut putar <b id="vr">${st.rot}°</b></label><input type="range" id="rr" min="0" max="270" step="90" value="${st.rot}">`;
  else c.innerHTML=`<label>Faktor skala (k) <b id="vk">${st.k}</b></label><input type="range" id="rk" min="-3" max="3" step="0.5" value="${st.k}">`;
  const on=(id,fn)=>{const e=$(id);if(e)e.oninput=()=>{fn(e.value);draw()}};
  on('#ra',v=>{st.a=+v;$('#va').textContent=v});on('#rb',v=>{st.b=+v;$('#vb').textContent=v});
  on('#sr',v=>st.ref=v);on('#rr',v=>{st.rot=+v;$('#vr').textContent=v+'°'});on('#rk',v=>{st.k=+v;$('#vk').textContent=v});
}
const TEORI={
  translasi:['Translasi menggeser setiap titik sejauh yang sama ke arah yang sama. Bentuk dan ukuran tidak berubah.','Titik (x, y) ditranslasi oleh (a, b) menjadi (x + a, y + b).'],
  refleksi:['Refleksi memindahkan bangun seperti bayangan di cermin. Jarak titik ke cermin sama dengan jarak bayangannya ke cermin.','Terhadap sumbu x: (x, −y). Sumbu y: (−x, y). Garis y = x: (y, x). Garis y = −x: (−y, −x).'],
  rotasi:['Rotasi memutar bangun terhadap titik pusat sejauh sudut tertentu. Sudut positif berarti berlawanan arah jarum jam.','Pusat O: 90° → (−y, x), 180° → (−x, −y), 270° → (y, −x).'],
  dilatasi:['Dilatasi memperbesar atau memperkecil bangun dengan faktor skala k. Bentuk tetap sebangun, ukuran berubah.','Pusat O dan faktor k: (x, y) → (kx, ky). Panjang sisi menjadi |k| kali, luas menjadi k² kali.']
};
const cv=$('#cv'),cx=cv.getContext('2d');
function col(n){return getComputedStyle(document.documentElement).getPropertyValue(n).trim()}
function draw(){
  const w=cv.clientWidth;if(!w)return;const dpr=devicePixelRatio||1;cv.width=w*dpr;cv.height=w*dpr;cx.setTransform(dpr,0,0,dpr,0,0);
  const u=w/(2*R),X=x=>(x+R)*u,Y=y=>(R-y)*u;cx.clearRect(0,0,w,w);
  cx.lineWidth=1;cx.font=`${Math.max(9,u*.5)}px system-ui`;cx.fillStyle=col('--mut');
  for(let i=-R;i<=R;i++){cx.strokeStyle=i===0?col('--axis'):col('--grid');cx.lineWidth=i===0?2:1;
    cx.beginPath();cx.moveTo(X(i),0);cx.lineTo(X(i),w);cx.stroke();cx.beginPath();cx.moveTo(0,Y(i));cx.lineTo(w,Y(i));cx.stroke();
    if(i&&i%2===0){cx.fillText(i,X(i)+2,Y(0)+u*.6);cx.fillText(i,X(0)+3,Y(i)-2)}}
  if(st.t==='refleksi'&&(st.ref==='yx'||st.ref==='ynx')){cx.setLineDash([6,5]);cx.strokeStyle=col('--pri2');cx.lineWidth=2;cx.beginPath();const s=st.ref==='yx'?1:-1;cx.moveTo(X(-R),Y(-R*s));cx.lineTo(X(R),Y(R*s));cx.stroke();cx.setLineDash([])}
  const shape=(pts,c,l)=>{cx.beginPath();pts.forEach((p,i)=>i?cx.lineTo(X(p[0]),Y(p[1])):cx.moveTo(X(p[0]),Y(p[1])));cx.closePath();cx.globalAlpha=.25;cx.fillStyle=c;cx.fill();cx.globalAlpha=1;cx.strokeStyle=c;cx.lineWidth=2.5;cx.stroke();
    cx.fillStyle=c;cx.font=`bold ${Math.max(11,u*.6)}px system-ui`;pts.forEach((p,i)=>{cx.beginPath();cx.arc(X(p[0]),Y(p[1]),4,0,7);cx.fill();cx.fillText(N[i]+l,X(p[0])+6,Y(p[1])-6)})};
  const Q=P.map(tf);shape(P,col('--pri'),'');shape(Q,col('--pri2'),'’');
  $('#fm').innerHTML=formula();
  $('#co').innerHTML=P.map((p,i)=>`${N[i]}(${p}) → ${N[i]}’(${Q[i]})`).join('<br>');
}
function setType(t){st.t=t;document.querySelectorAll('#tabs button').forEach(b=>b.classList.toggle('on',b.dataset.t===t));controls();
  $('#teori').innerHTML=`<h2>${TYPES[t]}</h2><p>${TEORI[t][0]}</p><div class="formula">${TEORI[t][1]}</div>`;draw()}
$('#tabs').innerHTML=Object.keys(TYPES).map(t=>`<button data-t="${t}">${TYPES[t].split(' ')[0]}</button>`).join('');
document.querySelectorAll('#tabs button').forEach(b=>b.onclick=()=>setType(b.dataset.t));
addEventListener('resize',draw);setType('translasi');

/* ---------- kuis ---------- */
const QS=[
 ['Titik A(3, 4) ditranslasi oleh (2, −5). Koordinat bayangannya adalah …',['(5, −1)','(1, 9)','(5, 9)','(1, −1)'],0,'(3 + 2, 4 + (−5)) = (5, −1).'],
 ['Titik (−2, 5) dicerminkan terhadap sumbu x. Bayangannya adalah …',['(2, 5)','(−2, −5)','(5, −2)','(2, −5)'],1,'Terhadap sumbu x, nilai y berubah tanda: (x, −y) = (−2, −5).'],
 ['Titik B(4, −3) dicerminkan terhadap sumbu y. Bayangannya adalah …',['(4, 3)','(−4, 3)','(−4, −3)','(−3, 4)'],2,'Terhadap sumbu y, nilai x berubah tanda: (−x, y) = (−4, −3).'],
 ['Titik P(2, 6) dicerminkan terhadap garis y = x. Bayangannya adalah …',['(6, 2)','(−6, −2)','(2, −6)','(−2, 6)'],0,'Terhadap y = x, koordinat bertukar: (y, x) = (6, 2).'],
 ['Titik (3, 2) dirotasi 90° berlawanan arah jarum jam dengan pusat O(0, 0). Bayangannya adalah …',['(2, −3)','(−3, −2)','(−2, 3)','(2, 3)'],2,'Rotasi 90°: (x, y) → (−y, x) = (−2, 3).'],
 ['Titik (−4, 1) dirotasi 180° dengan pusat O(0, 0). Bayangannya adalah …',['(4, −1)','(−4, −1)','(1, −4)','(4, 1)'],0,'Rotasi 180°: (x, y) → (−x, −y) = (4, −1).'],
 ['Titik (2, −1) didilatasi dengan pusat O dan faktor skala 3. Bayangannya adalah …',['(5, 2)','(6, −3)','(−6, 3)','(2/3, −1/3)'],1,'(3 · 2, 3 · (−1)) = (6, −3).'],
 ['Segitiga dengan luas 6 cm² didilatasi dengan faktor skala 2. Luas bayangannya adalah …',['12 cm²','18 cm²','24 cm²','36 cm²'],2,'Luas berubah k² kali: 6 × 2² = 24 cm².'],
 ['Titik A(1, 2) ditranslasi menjadi A’(4, 6). Vektor translasinya adalah …',['(5, 8)','(3, 4)','(−3, −4)','(4, 3)'],1,'(4 − 1, 6 − 2) = (3, 4).'],
 ['Titik (4, 1) dirotasi 90° searah jarum jam dengan pusat O(0, 0). Bayangannya adalah …',['(−1, 4)','(1, 4)','(1, −4)','(−4, −1)'],2,'Searah jarum jam 90° sama dengan 270°: (x, y) → (y, −x) = (1, −4).']
];
let qi,sc,streak,best,order,done;
const sh=a=>{a=a.slice();for(let i=a.length-1;i>0;i--){const j=Math.random()*(i+1)|0;[a[i],a[j]]=[a[j],a[i]]}return a};
function start(){qi=0;sc=0;streak=0;best=0;order=sh(QS.map((_,i)=>i));show()}
function show(){
  const q=QS[order[qi]];const opts=sh(q[1].map((t,i)=>[t,i]));done=false;
  $('#quiz').innerHTML=`<div class="top"><span>Soal ${qi+1}/${QS.length}</span><span>⭐ ${sc} &nbsp; 🔥 ${streak}</span></div>
  <div class="bar"><i style="width:${qi/QS.length*100}%"></i></div><div class="q">${q[0]}</div>
  ${opts.map(o=>`<button class="opt" data-c="${o[1]===q[2]?1:0}">${o[0]}</button>`).join('')}
  <div class="fb" id="fb"></div><button class="btn hide" id="nx">${qi===QS.length-1?'Lihat hasil 🏆':'Lanjut →'}</button>`;
  document.querySelectorAll('.opt').forEach(b=>b.onclick=()=>pick(b,q));
  $('#nx').onclick=()=>{qi++;qi<QS.length?show():finish()};
}
function pick(b,q){
  if(done)return;done=true;const ok=b.dataset.c==='1';
  document.querySelectorAll('.opt').forEach(o=>{o.disabled=true;if(o.dataset.c==='1')o.classList.add('ok')});
  if(ok){streak++;best=Math.max(best,streak);sc+=10+Math.min(streak-1,3)*2}else{b.classList.add('bad');streak=0}
  const f=$('#fb');f.style.display='block';f.innerHTML=(ok?'✅ <b>Benar!</b> ':'❌ <b>Belum tepat.</b> ')+q[3];
  $('#nx').classList.remove('hide');
}
function finish(){
  const max=QS.length*10,pct=sc/ (QS.length*16);const correct=Math.round(sc>=0?sc:0);
  const r=sc>=QS.length*10?['🏆','Master Transformasi!']:sc>=70?['🚀','Keren sekali!']:sc>=40?['👍','Bagus, terus berlatih!']:['📚','Ayo belajar lagi di laboratorium!'];
  $('#quiz').innerHTML=`<div class="res pop"><div class="big">${r[0]}</div><h2>${r[1]}</h2><div class="score">${sc} poin</div>
  <p>Rentetan benar terbaik: 🔥 ${best} soal berturut-turut</p><p class="coords">Setiap jawaban benar bernilai 10 poin, ditambah bonus untuk rentetan benar.</p>
  <button class="btn" id="re">Main lagi 🔁</button></div>`;
  $('#re').onclick=start;
}
start();
</script>
</body>
</html>

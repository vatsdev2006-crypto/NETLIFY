<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<meta name="theme-color" content="#14040a">
<title>For You, Beta ❤️</title>
<link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>❤️</text></svg>">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,600;1,400&family=Great+Vibes&display=swap" rel="stylesheet">
<style>
:root{color-scheme:dark;--rose:#ff8fab;--red:#e11d48;--burg:#4a0a1c;--ink:#14040a;--glass:rgba(255,255,255,.07)}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{background:radial-gradient(120% 80% at 50% 0%,#3a0716 0%,#1b0610 45%,#0b0206 100%) fixed;color:#ffe9ef;font-family:'Cormorant Garamond',Georgia,serif;font-size:clamp(19px,2.6vw,24px);line-height:1.65;overflow-x:hidden}
body.locked{overflow:hidden}
body.locked .after{display:none}
#bg{position:fixed;inset:0;width:100%;height:100%;z-index:0;pointer-events:none}
#petals{position:fixed;inset:0;z-index:1;pointer-events:none;overflow:hidden}
.petal{position:absolute;top:-8vh;width:14px;height:18px;background:linear-gradient(135deg,#ff9bb3,#d11a4a);border-radius:80% 0 80% 0;opacity:.8;animation:fall linear forwards;will-change:transform}
.petal.rose{background:none;width:auto;height:auto;font-size:20px}
@keyframes fall{to{transform:translate3d(var(--dx),112vh,0) rotate(var(--r))}}
.scr{position:relative;z-index:2;min-height:100svh;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:calc(10vh + env(safe-area-inset-top,0px)) 22px 10vh}
.hs{width:100%;height:34vh;max-height:300px;flex:none;position:relative}
.hs::before{content:"";position:absolute;inset:0;margin:auto;width:min(70vw,340px);aspect-ratio:1;background:radial-gradient(circle,rgba(255,40,90,.35),transparent 65%);animation:glow 3s ease-in-out infinite}
@keyframes glow{50%{opacity:.4;transform:scale(1.15)}}
.script{font-family:'Great Vibes','Cormorant Garamond',cursive;font-weight:400;line-height:1.15;background:linear-gradient(90deg,#ffd1dc,#ff5c8a,#ffd1dc);background-size:200% auto;-webkit-background-clip:text;background-clip:text;color:transparent;animation:sheen 6s linear infinite;filter:drop-shadow(0 0 18px rgba(255,60,110,.55))}
@keyframes sheen{to{background-position:200% center}}
h1.script{font-size:clamp(3.2rem,12vw,6.5rem)}
h2.script{font-size:clamp(2.4rem,8vw,4.4rem);margin-bottom:.6em}
.lead{max-width:620px;opacity:.92}
.card{max-width:680px;width:100%;padding:clamp(24px,5vw,48px);background:var(--glass);border:1px solid rgba(255,170,190,.22);border-radius:28px;backdrop-filter:blur(16px);-webkit-backdrop-filter:blur(16px);box-shadow:0 20px 60px rgba(0,0,0,.45),inset 0 0 40px rgba(255,80,120,.06);text-align:left}
.card p+p{margin-top:1.1em}
.btn{font:inherit;font-weight:600;color:#fff;border:0;cursor:pointer;padding:.85em 1.8em;border-radius:999px;background:linear-gradient(135deg,#ff4d79,#b0123d);box-shadow:0 0 28px rgba(255,60,110,.55);transition:transform .25s,box-shadow .25s;-webkit-tap-highlight-color:transparent}
.btn:hover{transform:translateY(-3px) scale(1.04);box-shadow:0 0 44px rgba(255,60,110,.85)}
.btn:active{transform:scale(.97)}
.btn.soft{background:var(--glass);border:1px solid rgba(255,170,190,.45);box-shadow:none;backdrop-filter:blur(8px)}
.btn.soft:hover{box-shadow:0 0 30px rgba(255,150,180,.35)}
.pulse{animation:pulse 2.2s ease-in-out infinite}
@keyframes pulse{50%{box-shadow:0 0 60px rgba(255,60,110,.95);transform:scale(1.05)}}
/* word reveal */
.w{display:inline-block;opacity:0;transform:translateY(14px);filter:blur(6px);transition:opacity .9s,transform .9s,filter .9s}
.in .w,.w.in{opacity:1;transform:none;filter:none}
.rv{opacity:0;transform:translateY(40px);transition:opacity 1s,transform 1s}
.rv.in{opacity:1;transform:none}
/* gallery */
.gal{display:flex;flex-wrap:wrap;justify-content:center;gap:34px 28px;margin-top:2.4em;perspective:1100px;max-width:1100px}
.pol{width:min(290px,82vw);padding:12px 12px 16px;border-radius:14px;background:linear-gradient(145deg,rgba(255,255,255,.16),rgba(255,255,255,.05));border:1px solid rgba(255,190,205,.35);backdrop-filter:blur(14px);-webkit-backdrop-filter:blur(14px);box-shadow:0 24px 50px rgba(0,0,0,.55),0 0 30px rgba(255,60,110,.18);opacity:0;transform:rotateY(55deg) translateY(50px);transition:opacity 1s,transform 1.1s cubic-bezier(.2,.8,.2,1)}
.pol.in{opacity:1;transform:rotate(var(--rot,0deg))}
.pol.tilt{transition:transform .12s linear}
.pol .ph{display:flex;align-items:center;justify-content:center;aspect-ratio:4/5;border-radius:8px;background:linear-gradient(135deg,#5a0f26,#240812);border:1px dashed rgba(255,170,190,.5);cursor:pointer;font-size:.85em;padding:14px;text-align:center;color:#ffc1d1}
.pol .ph input{display:none}
.pol img{display:none;width:100%;height:auto;border-radius:8px;transition:transform 1.6s}
.pol:hover img{transform:scale(1.04)}
.pol.has img{display:block}.pol.has .ph{display:none}
.pol .box{overflow:hidden;border-radius:8px}
.pol figcaption{font-family:'Great Vibes',cursive;font-size:1.55rem;margin-top:8px;color:#ffd1dc}
.float{animation:fl 6s ease-in-out infinite}
@keyframes fl{50%{translate:0 -10px}}
/* promises */
.plist{list-style:none;max-width:560px;margin:1.2em auto 1.6em;text-align:left}
.plist li{padding:.7em 1.1em;margin:.7em 0;background:var(--glass);border:1px solid rgba(255,170,190,.2);border-radius:18px;backdrop-filter:blur(10px)}
.plist li::before{content:"❤ ";color:#ff4d79}
.reply{min-height:7em;max-width:620px;margin-top:1.8em;font-size:1.15em;opacity:0}
.btns{display:flex;flex-wrap:wrap;gap:16px;justify-content:center;margin-top:1.6em}
#fin{margin-top:2.6em}
#audio{position:fixed;right:max(14px,env(safe-area-inset-right,0px));top:calc(14px + env(safe-area-inset-top,0px));z-index:20;width:48px;height:48px;border-radius:50%;border:1px solid rgba(255,170,190,.4);background:rgba(30,6,14,.6);backdrop-filter:blur(10px);color:#fff;font-size:20px;cursor:pointer}
#cover{position:fixed;inset:0;z-index:50;background:#000;pointer-events:none}
footer{position:relative;z-index:2;text-align:center;padding:30px 20px calc(40px + env(safe-area-inset-bottom,0px));opacity:.7;font-style:italic}
@media(prefers-reduced-motion:reduce){*{animation:none!important}.rv,.w,.pol{opacity:1!important;transform:none!important;filter:none!important}}
</style>
</head>
<body class="locked">
<canvas id="bg"></canvas>
<div id="petals"></div>
<div id="cover"></div>
<button id="audio" aria-label="Play music">♪</button>

<!-- SCREEN 1 -->
<section class="scr" id="s1">
  <div class="hs" data-s="1"></div>
  <h1 class="script" id="t1">Hey Betaaa... ❤️</h1>
  <p class="lead" id="t1p" style="margin:.8em 0 1.6em">I know things haven’t been right between us lately. But before anything else, there’s something I really want to tell you...</p>
  <button class="btn pulse" id="open">Open My Heart ❤️</button>
</section>

<!-- SCREEN 2 -->
<section class="scr after" id="s2">
  <h2 class="script">I’m Truly Sorry</h2>
  <div class="card words">
    <p>Beta, I’m really sorry for all the times I hurt you. I know saying sorry cannot undo what happened, and I don’t want to make excuses for my mistakes.</p>
    <p>I know I made mistakes, and I genuinely regret them. You mean so much to me, and the last thing I ever wanted was to become the reason behind your sadness.</p>
    <p>I wish I could go back and change those moments, but all I can do now is accept my mistakes and show you through my actions that I can do better.</p>
  </div>
</section>

<!-- SCREEN 3 -->
<section class="scr after" id="s3">
  <h2 class="script">Some Moments Will Always Be Special ❤️</h2>
  <p class="lead rv">Every picture holds a memory, and every memory reminds me how special you are to me.</p>
  <div class="gal" id="gal"></div>
</section>

<!-- SCREEN 4 -->
<section class="scr after" id="s4">
  <div class="hs" data-s=".7"></div>
  <h2 class="script">I Promise You...</h2>
  <ul class="plist" id="plist">
    <li class="rv">I’ll learn from my mistakes instead of repeating them.</li>
    <li class="rv">I’ll listen to you and understand your feelings.</li>
    <li class="rv">I’ll never take your love and efforts for granted.</li>
    <li class="rv">I’ll work on becoming a better person.</li>
    <li class="rv">I’ll show you through my actions, not just words.</li>
  </ul>
  <p class="lead words">I know promises mean nothing without actions. I don’t expect you to believe everything immediately. I just want the chance to prove that I can do better.</p>
</section>

<!-- SCREEN 5 -->
<section class="scr after" id="s5">
  <div class="hs" data-s="1.1"></div>
  <h2 class="script">One Last Thing... ❤️</h2>
  <div class="card words">
    <p>Beta, I really love you. More than I can explain through words.</p>
    <p>I don’t want to lose what we have. I know I cannot demand another chance, but if there’s still a little space in your heart for me, I’d be grateful for one more opportunity to make things right.</p>
    <p>I don’t promise to be perfect, but I promise to genuinely try, to understand, to improve, and to never knowingly repeat the mistakes that hurt you.</p>
  </div>
  <h2 class="script rv" style="margin-top:1.4em">Will You Give Me One More Chance? 🥺❤️</h2>
  <div class="btns rv">
    <button class="btn" id="yes">Yes, One More Chance ❤️</button>
    <button class="btn soft" id="time">I Need Some Time 💗</button>
  </div>
  <p class="reply" id="reply"></p>
  <div class="gal" id="fin"></div>
</section>
<footer class="after">Made with all my heart, just for you. ❤️</footer>

<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js"></script>
<script>
/* ============ 1) YOUR PHOTOS ============
   Paste DIRECT image links here (they end in .jpg / .png, e.g. https://i.ibb.co/xxxx/photo.jpg).
   Leave "" to show a "tap to add photo" placeholder. */
const IMAGES=[
"https://i.ibb.co/HLnfGRXK/IMG-6503.jpg",
"https://i.ibb.co/x8tGX75v/IMG-5002.jpg",
"https://i.ibb.co/5xgqWY11/IMG-4050.jpg",
"https://i.ibb.co/1Gx438Rg/IMG-3591.jpg",
"https://i.ibb.co/1fHM1W7D/IMG-4194.jpg"];
const CAPTIONS=["Us ❤️","Your smile","That day","Together","Always you"];

const $=s=>document.querySelector(s), $$=s=>[...document.querySelectorAll(s)];
const reduce=matchMedia('(prefers-reduced-motion:reduce)').matches;

/* ---------- sound ---------- */
let ac,music=false,mt,chordI=0;
const CH=[[261.6,329.6,392],[220,261.6,329.6],[174.6,220,261.6],[196,246.9,293.7]];
function ctx(){if(!ac)ac=new (window.AudioContext||window.webkitAudioContext)();if(ac.state==='suspended')ac.resume();return ac}
function tone(f,t0,dur,vol,type='sine',att=.05){const a=ctx(),o=a.createOscillator(),g=a.createGain();o.type=type;o.frequency.value=f;
  g.gain.setValueAtTime(0,t0);g.gain.linearRampToValueAtTime(vol,t0+att);g.gain.exponentialRampToValueAtTime(.0001,t0+dur);
  o.connect(g).connect(a.destination);o.start(t0);o.stop(t0+dur+.1)}
function blip(f=880){try{tone(f,ctx().currentTime,.25,.05)}catch(e){}}
function chord(){const t=ctx().currentTime,c=CH[chordI++%4];c.forEach((f,i)=>tone(f/2,t+i*.15,4,.035,'sine',1));tone(c[2]*2,t+1.2,2.5,.015,'triangle',.3)}
$('#audio').onclick=e=>{music=!music;e.target.textContent=music?'❚❚':'♪';clearInterval(mt);if(music){chord();mt=setInterval(chord,3400)}};
document.addEventListener('click',e=>{if(e.target.closest('.btn'))blip(e.target.id==='time'?660:988)});

/* ---------- text reveal ---------- */
function split(el){const walk=n=>{[...n.childNodes].forEach(c=>{if(c.nodeType===3){const f=document.createDocumentFragment();
  c.textContent.split(/(\s+)/).forEach(p=>{if(!p.trim()){f.append(p);return}const s=document.createElement('span');s.className='w';s.textContent=p;f.append(s)});c.replaceWith(f)}else walk(c)})};walk(el);
  el.querySelectorAll('.w').forEach((w,i)=>w.style.transitionDelay=Math.min(i*45,3000)+'ms')}
$$('.words').forEach(split);
const io=new IntersectionObserver(es=>es.forEach(e=>{if(e.isIntersecting){e.target.classList.add('in');io.unobserve(e.target)}}),{threshold:.25});
$$('.words,.rv').forEach(el=>{if(el.closest('li'))return;io.observe(el)});
$$('#plist li').forEach((li,i)=>{li.style.transitionDelay=(i*.7)+'s'});

/* ---------- photos ---------- */
function setImg(p,src){const im=p.querySelector('img');im.onload=()=>p.classList.add('has');im.src=src}
function polaroid(i,rot){const f=document.createElement('figure');f.className='pol';f.style.setProperty('--rot',rot+'deg');
  f.innerHTML=`<div class="box"><label class="ph"><input type="file" accept="image/*"><span>Tap to add photo ${i+1}<br><small>(or paste a direct URL in IMAGES)</small></span></label><img alt="Our memory ${i+1}" loading="lazy" decoding="async"></div><figcaption>${CAPTIONS[i]||''}</figcaption>`;
  f.querySelector('input').onchange=e=>{const fl=e.target.files[0];if(fl)setImg(f,URL.createObjectURL(fl))};
  if(IMAGES[i])setImg(f,IMAGES[i]);
  f.addEventListener('pointermove',e=>{if(e.pointerType==='touch')return;const r=f.getBoundingClientRect(),x=(e.clientX-r.left)/r.width-.5,y=(e.clientY-r.top)/r.height-.5;
    f.classList.add('tilt');f.style.transform=`rotateY(${x*22}deg) rotateX(${-y*22}deg) scale(1.04)`});
  f.addEventListener('pointerleave',()=>{f.style.transform='';f.classList.remove('tilt')});
  return f}
const rots=[-4,3,-2,4,-3];
IMAGES.forEach((_,i)=>{const p=polaroid(i,rots[i]);$('#gal').append(p);p.style.transitionDelay=(i%3*.15)+'s';
  io.observe(p);setTimeout(()=>p.classList.add('float'),1500+i*300);p.style.animationDelay=(i*-1.1)+'s'});
// final emotional photo: cycles through all five
const fin=polaroid(0,0);fin.style.width='min(340px,86vw)';$('#fin').append(fin);io.observe(fin);
let fi=0;setInterval(()=>{if(!IMAGES.some(Boolean))return;do{fi=(fi+1)%IMAGES.length}while(!IMAGES[fi]);
  gsap.to(fin.querySelector('img'),{opacity:0,duration:.6,onComplete(){setImg(fin,IMAGES[fi]);fin.querySelector('figcaption').textContent=CAPTIONS[fi];gsap.to(fin.querySelector('img'),{opacity:1,duration:.8})}})},4200);
if(!IMAGES.some(Boolean))fin.querySelector('span').innerHTML='Your favourite photo can go here ❤️';

/* ---------- petals ---------- */
function petal(rose){const p=document.createElement('div');p.className='petal'+(rose?' rose':'');if(rose)p.textContent='🌹';
  p.style.left=Math.random()*100+'vw';p.style.animationDuration=(9+Math.random()*9)+'s';
  p.style.setProperty('--dx',(Math.random()*160-80)+'px');p.style.setProperty('--r',(Math.random()*720-360)+'deg');
  if(!rose)p.style.transform=`scale(${.6+Math.random()})`;$('#petals').append(p);setTimeout(()=>p.remove(),19000)}
const small=innerWidth<700;
let pi=setInterval(()=>{if(!document.hidden)petal(Math.random()<.12)},small?1100:700);

/* ---------- Three.js ---------- */
const cv=$('#bg'),R=new THREE.WebGLRenderer({canvas:cv,alpha:true,antialias:!small});
R.setPixelRatio(Math.min(devicePixelRatio,small?1.5:2));
const scene=new THREE.Scene(),cam=new THREE.PerspectiveCamera(50,1,.1,100);cam.position.z=7;
scene.add(new THREE.AmbientLight(0xff9db4,.5));
const l1=new THREE.PointLight(0xff4d79,2.2,30);l1.position.set(3,3,5);scene.add(l1);
const l2=new THREE.PointLight(0xffb3c6,1.4,30);l2.position.set(-4,-2,4);scene.add(l2);
const pts=[];for(let t=0;t<Math.PI*2;t+=.04)pts.push(new THREE.Vector2(16*Math.pow(Math.sin(t),3),13*Math.cos(t)-5*Math.cos(2*t)-2*Math.cos(3*t)-Math.cos(4*t)));
const shape=new THREE.Shape(pts);
const hg=new THREE.ExtrudeGeometry(shape,{depth:5,bevelEnabled:true,bevelThickness:2,bevelSize:2,bevelSegments:4,curveSegments:24});
hg.center();hg.scale(.07,.07,.07);
const hm=new THREE.MeshStandardMaterial({color:0xe0184d,emissive:0x5c0018,metalness:.25,roughness:.28});
const heart=new THREE.Mesh(hg,hm);heart.scale.setScalar(0);scene.add(heart);
// particles
const N=small?140:320,pa=new Float32Array(N*3);for(let i=0;i<N;i++){pa[i*3]=(Math.random()-.5)*16;pa[i*3+1]=(Math.random()-.5)*14;pa[i*3+2]=(Math.random()-.5)*8-1}
const pg=new THREE.BufferGeometry();pg.setAttribute('position',new THREE.BufferAttribute(pa,3));
const dots=new THREE.Points(pg,new THREE.PointsMaterial({color:0xff9bb8,size:.06,transparent:true,opacity:.8,blending:THREE.AdditiveBlending,depthWrite:false}));scene.add(dots);
// floating small hearts
const fl=[];const fm=new THREE.MeshStandardMaterial({color:0xff5c8a,emissive:0x40001a,roughness:.4,transparent:true,opacity:.85});
for(let i=0;i<(small?7:14);i++){const m=new THREE.Mesh(hg,fm);const s=.07+Math.random()*.12;m.scale.setScalar(s);
  m.position.set((Math.random()-.5)*10,(Math.random()-.5)*10,-2-Math.random()*4);m.userData={sp:.2+Math.random()*.4,ph:Math.random()*6};scene.add(m);fl.push(m)}
// explosion
let burst=[];
function explode(){const o=heart.position.clone();const mat=new THREE.MeshStandardMaterial({color:0xff2d63,emissive:0x7a0025,roughness:.3,transparent:true});
  for(let i=0;i<(small?55:90);i++){const m=new THREE.Mesh(hg,mat);m.scale.setScalar(.04+Math.random()*.1);m.position.copy(o);
    const a=Math.random()*6.283,b=Math.random()*3.14,v=2+Math.random()*5;
    m.userData={v:new THREE.Vector3(Math.sin(b)*Math.cos(a)*v,Math.sin(b)*Math.sin(a)*v+1.5,(Math.random()-.3)*v),life:1,s:m.scale.x};
    m.rotation.set(Math.random()*3,Math.random()*3,Math.random()*3);scene.add(m);burst.push(m)}
  heart.userData.kick=1.6;for(let i=0;i<50;i++)setTimeout(()=>petal(Math.random()<.2),i*60)}
function size(){const w=innerWidth,h=innerHeight;R.setSize(w,h,false);cam.aspect=w/h;cam.updateProjectionMatrix()}
addEventListener('resize',size);size();
const hs=$$('.hs');let tgt={x:0,y:0,s:0},clock=new THREE.Clock();
function frame(){requestAnimationFrame(frame);if(document.hidden)return;
  const t=clock.getElapsedTime(),dt=Math.min(clock.getDelta(),.05)||.016,vh=2*Math.tan(cam.fov*Math.PI/360)*cam.position.z,vw=vh*cam.aspect;
  // find heart-space nearest viewport centre
  let best=null,bd=1e9;hs.forEach(e=>{if(e.offsetParent===null)return;const r=e.getBoundingClientRect(),c=r.top+r.height/2,d=Math.abs(c-innerHeight/2);if(d<bd&&r.bottom>0&&r.top<innerHeight){bd=d;best=[e,r,c]}});
  if(best&&bd<innerHeight*.75){const[e,r,c]=best,k=+e.dataset.s;let s=Math.min((r.height/innerHeight)*vh/2.1,vw*.62/2.2)*k;
    tgt={x:0,y:(innerHeight/2-c)/innerHeight*vh,s:s*Math.max(0,1-bd/(innerHeight*.75))**.5}}else tgt.s=0;
  heart.position.x+=(tgt.x-heart.position.x)*.1;heart.position.y+=(tgt.y-heart.position.y)*.1;
  const kick=heart.userData.kick||0;heart.userData.kick=kick*.94;
  const beat=1+.06*Math.pow(Math.max(0,Math.sin(t*3.2)),3)+kick*.3;
  heart.scale.setScalar(heart.scale.x+((tgt.s*beat)-heart.scale.x)*.12);
  heart.rotation.y=Math.sin(t*.7)*.7;heart.rotation.x=Math.sin(t*.5)*.12;
  dots.rotation.y=t*.02;dots.position.y=scrollY*.0016;
  fl.forEach(m=>{m.position.y+=m.userData.sp*.006;if(m.position.y>vh/2+1)m.position.y=-vh/2-1;m.rotation.y=t*m.userData.sp+m.userData.ph;m.rotation.z=Math.sin(t+m.userData.ph)*.3});
  burst=burst.filter(m=>{const u=m.userData;u.v.y-=3.2*.016;m.position.addScaledVector(u.v,.016);u.v.multiplyScalar(.985);u.life-=.006;m.rotation.x+=.04;m.rotation.y+=.05;
    m.scale.setScalar(Math.max(.001,u.s*u.life));if(u.life<=0){scene.remove(m);return false}return true});
  R.render(scene,cam)}
if(!reduce||true)frame();

/* ---------- interactions ---------- */
const tl=gsap.timeline();
split($('#t1p'));
tl.to('#cover',{opacity:0,duration:2.4,ease:'power2.inOut'})
  .from('#t1',{opacity:0,y:30,scale:.9,filter:'blur(14px)',duration:1.6,ease:'power3.out'},'-=1.2')
  .add(()=>$('#t1p').classList.add('in'),'-=.4')
  .from('#open',{opacity:0,y:20,duration:1},'+=1.2');
$('#open').onclick=()=>{document.body.classList.remove('locked');
  gsap.fromTo('#s2',{opacity:0},{opacity:1,duration:1.4});
  requestAnimationFrame(()=>$('#s2').scrollIntoView({behavior:'smooth'}));
  heart.userData.kick=.8;for(let i=0;i<8;i++)setTimeout(()=>petal(i%3===0),i*120)};
const reply=$('#reply');
function say(html){gsap.fromTo(reply,{opacity:0,y:16},{opacity:1,y:0,duration:1.2});reply.innerHTML=html;reply.scrollIntoView({behavior:'smooth',block:'center'})}
$('#yes').onclick=()=>{say('Thank You, Betaaa! ❤️<br>I’ll make sure my actions speak louder than my words. I love you so much!');explode();
  setTimeout(explode,700);if(!reduce)gsap.fromTo('#yes',{scale:1},{scale:1.12,yoyo:true,repeat:3,duration:.2})};
$('#time').onclick=()=>say('I understand, Beta. Take all the time you need. I don’t want to rush you. Your feelings matter to me, and I’ll respect your decision. ❤️');
</script>
</body>
</html>

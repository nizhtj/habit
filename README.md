<!DOCTYPE html>
<html lang="id"><head><meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<meta name="theme-color" content="#FFEFE3"><title>PeachHabit</title>
<link href="https://fonts.googleapis.com/css2?family=Nunito:wght@500;700;800&family=Caveat:wght@600;700&display=swap" rel="stylesheet">
<script>
// Manifest PWA sebagai Data URI
(function(){var m={name:"PeachHabit",short_name:"Habit",start_url:".",display:"standalone",background_color:"#FFEFE3",theme_color:"#FFB894",icons:[{src:"data:image/svg+xml,"+encodeURIComponent("<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect width='100' height='100' fill='#FFEFE3'/><text y='.85em' x='12' font-size='80'>🍑</text></svg>"),sizes:"512x512",type:"image/svg+xml",purpose:"any"}]};
var l=document.createElement('link');l.rel='manifest';l.href='data:application/manifest+json,'+encodeURIComponent(JSON.stringify(m));document.head.appendChild(l)})();
</script>
<style>
*{box-sizing:border-box;margin:0;-webkit-tap-highlight-color:transparent}
:root{--bg:#FFEFE3;--card:#FFF8F2;--pe:#FFB894;--ped:#F4956B;--mint:#BFE3D0;--lav:#D9D2F0;--sage:#8DB5A0;--tx:#5B4036;--mu:#A58B7E;--sh:0 8px 24px rgba(244,149,107,.18)}
body{font-family:Nunito,system-ui,sans-serif;font-weight:500;background:var(--bg) radial-gradient(circle at 0 0,#FFD9C2,transparent 45%) fixed;color:var(--tx);min-height:100dvh}
button,input,select,textarea{font:inherit;color:inherit}
button{border:0;cursor:pointer;background:none}
h1{font-size:22px;font-weight:800}h2{font-size:17px;font-weight:800}small,.mu{color:var(--mu);font-size:13px}
.card{background:var(--card);border-radius:24px;box-shadow:var(--sh);padding:18px}
main{padding:20px 16px 130px;max-width:720px;margin:auto}
section.in{animation:fade .45s ease both}
.row{display:grid;grid-template-columns:1fr 1fr;gap:14px;margin:14px 0}
.hd{display:flex;justify-content:space-between;align-items:center;margin:18px 2px 10px}
.lnk{color:var(--ped);font-weight:700}
.hero{display:flex;justify-content:space-between;align-items:center;gap:8px;background:linear-gradient(135deg,#FFE0CC,#FFF1E6)}
.masc{width:84px;flex:none;animation:flt 3.5s ease-in-out infinite}.eyes{transform-box:fill-box;transform-origin:center;animation:blink 4.5s infinite}
.ringc{position:relative;display:grid;place-items:center;padding:10px}.ringc svg{width:120px;transform:rotate(-90deg)}
.ringc b{position:absolute;font-size:22px}
.rb,.rf{fill:none;stroke-width:10}.rb{stroke:#FFE3D2}.rf{stroke:var(--ped);stroke-linecap:round;stroke-dasharray:264;transition:stroke-dashoffset 1s cubic-bezier(.3,.8,.3,1)}
.streak{display:flex;flex-direction:column;align-items:center;justify-content:center;gap:2px;background:var(--lav)}
.streak b{font-size:34px}.fl{font-size:38px;display:inline-block;animation:wig 1.6s ease-in-out infinite;transform-origin:50% 90%}
.it{display:flex;align-items:center;gap:12px;width:100%;background:var(--card);border-radius:20px;padding:12px 14px;margin-bottom:10px;box-shadow:var(--sh);text-align:left;min-height:60px;transition:transform .15s,background .3s}
.it:active{transform:scale(.97)}.it .ic{width:42px;height:42px;border-radius:14px;background:var(--c);display:grid;place-items:center;font-size:22px}
.it .nm{flex:1;font-weight:700}.ck{width:32px;height:32px;border-radius:50%;border:2.5px solid #F0D5C5;display:grid;place-items:center;color:#fff;font-weight:800;transition:.25s}
.it.on{background:#EAF6EF}.it.on .nm{text-decoration:line-through;color:var(--mu)}.it.on .ck{background:var(--sage);border-color:var(--sage)}.ck.pop{animation:pop .5s}
.act{display:flex;gap:6px}.act button{width:40px;height:40px;border-radius:12px;background:#FFE9DB}
.btn{background:var(--ped);color:#fff;font-weight:800;border-radius:18px;padding:14px 22px;box-shadow:0 6px 16px rgba(244,149,107,.4);transition:transform .15s;min-height:48px}.btn:active{transform:scale(.96)}
.btn.s{background:#FFE3D2;color:var(--ped);box-shadow:none}
input,select,textarea{width:100%;background:#fff;border:2px solid #FFE3D2;border-radius:16px;padding:12px 14px;margin:6px 0 10px;outline:0}input:focus,select:focus,textarea:focus{border-color:var(--pe)}
.bars{display:flex;justify-content:space-between;align-items:flex-end;height:140px;gap:8px}.bc{flex:1;display:flex;flex-direction:column;align-items:center;justify-content:flex-end;height:100%;gap:6px}
.bc i{width:100%;max-width:30px;background:linear-gradient(var(--pe),var(--ped));border-radius:10px 10px 6px 6px;min-height:6px;height:var(--h);animation:grow .9s cubic-bezier(.3,.8,.3,1) both}
.donut{width:130px;height:130px;border-radius:50%;flex:none;mask:radial-gradient(circle,transparent 38%,#000 40%);-webkit-mask:radial-gradient(circle,transparent 38%,#000 40%)}
.lg{display:flex;align-items:center;gap:6px;font-size:13px;margin:3px 0}.lg i{width:12px;height:12px;border-radius:4px}
.hm{display:grid;grid-template-columns:repeat(7,1fr);gap:6px}.hm div{aspect-ratio:1;border-radius:10px;font-size:11px;display:grid;place-items:center;color:var(--tx)}.hm .fut{opacity:.35}
.bdg{display:flex;gap:14px;align-items:center;margin-bottom:12px}.bdg .e{font-size:36px}.bdg.lock .e{filter:grayscale(1);opacity:.4}
.pb{height:8px;border-radius:8px;background:#FFE3D2;margin-top:6px;overflow:hidden}.pb i{display:block;height:100%;background:var(--sage);border-radius:8px;transition:width 1s}
.moods{display:flex;gap:8px;margin-bottom:10px}.moods button{flex:1;font-size:28px;padding:8px;border-radius:16px;background:#FFF1E6;transition:.2s}.moods .sel{background:var(--pe);transform:scale(1.1)}
.chips{display:flex;flex-wrap:wrap;gap:8px;margin:6px 0 12px}.chips button{min-width:44px;height:44px;border-radius:14px;background:#FFF1E6;font-size:18px;padding:0 10px}.chips .sel{background:var(--pe);color:#fff;font-weight:800}
.bd{position:fixed;inset:0;background:rgba(91,64,54,.35);z-index:20;animation:fade .2s}
.sheet{position:fixed;left:0;right:0;bottom:0;max-height:90dvh;overflow:auto;background:var(--card);border-radius:28px 28px 0 0;padding:22px 18px calc(22px + env(safe-area-inset-bottom));z-index:21;animation:up .35s cubic-bezier(.3,.8,.3,1);max-width:560px;margin:auto}
.toast{position:fixed;top:calc(14px + env(safe-area-inset-top));left:50%;transform:translateX(-50%);background:var(--tx);color:#fff;padding:12px 20px;border-radius:20px;z-index:40;animation:fade .3s;font-weight:700}
.petal{position:fixed;z-index:50;pointer-events:none;font-size:18px;animation:petal .9s ease-out forwards}
.tabs{display:flex;background:#FFE9DB;border-radius:18px;padding:4px;margin-bottom:14px}.tabs button{flex:1;padding:10px;border-radius:14px;font-weight:700;color:var(--mu)}.tabs .on{background:#fff;color:var(--ped);box-shadow:var(--sh)}
.login{max-width:380px;margin:auto;padding:36px 18px;text-align:center}.login .masc{width:110px}.err{color:#D9604A;font-weight:700;min-height:20px;font-size:14px}
.nav{position:fixed;left:12px;right:12px;bottom:calc(12px + env(safe-area-inset-bottom));display:flex;justify-content:space-around;align-items:center;background:rgba(255,248,242,.8);backdrop-filter:blur(14px);-webkit-backdrop-filter:blur(14px);border-radius:30px;padding:8px;box-shadow:var(--sh);z-index:10;max-width:520px;margin:auto}
.nav button{display:flex;flex-direction:column;align-items:center;gap:2px;font-size:11px;font-weight:700;color:var(--mu);min-width:56px;min-height:50px;border-radius:18px;justify-content:center;transition:.25s}.nav button span{font-size:20px}.nav .on{color:var(--ped);background:#FFE3D2}
.nav .fab{width:58px;height:58px;border-radius:50%;background:var(--ped);color:#fff;font-size:30px;margin-top:-30px;box-shadow:0 8px 20px rgba(244,149,107,.5);min-width:58px}.nav .fab:active{transform:scale(.92)}
.side{display:none}
@media(min-width:900px){.nav{display:none}.side{display:flex;flex-direction:column;gap:6px;position:fixed;inset:16px auto 16px 16px;width:210px;background:var(--sage);border-radius:30px;padding:22px 12px;color:#fff;z-index:10}
.side h2{margin:0 8px 16px}.side .n{color:#fff;text-align:left;padding:13px 14px;border-radius:16px;font-weight:700;transition:.2s}.side .n:hover,.side .n.on{background:rgba(255,255,255,.28)}
main{margin-left:246px;max-width:880px;padding-bottom:40px}}
@keyframes fade{from{opacity:0;transform:translateY(8px)}}@keyframes up{from{transform:translateY(100%)}}@keyframes grow{from{height:0}}
@keyframes flt{50%{transform:translateY(-6px)}}@keyframes blink{0%,92%,100%{transform:scaleY(1)}96%{transform:scaleY(.1)}}
@keyframes wig{0%,100%{transform:rotate(-6deg)}50%{transform:rotate(6deg) scale(1.08)}}
@keyframes pop{0%{transform:scale(.4)}60%{transform:scale(1.35)}100%{transform:scale(1)}}
@keyframes petal{to{transform:translate(var(--dx),var(--dy)) rotate(260deg);opacity:0}}
@media(prefers-reduced-motion:reduce){*{animation:none!important;transition:none!important}}
:root{--bg:#FFE9E4;--pk:#FFC9D0}
body{background:var(--bg) radial-gradient(circle at 100% 0,#FFD3DA,transparent 40%) fixed}
.hw{font-family:Caveat,cursive;font-size:32px;font-weight:700;line-height:1.05}
.page{position:relative;margin:18px 0 14px 14px;background:#FFF9EC radial-gradient(#E6D6C2 1px,transparent 1.2px) 0 0/16px 16px;border-radius:8px 24px 24px 8px;padding:22px 18px 20px 34px;box-shadow:var(--sh)}
.page::before{content:"";position:absolute;left:-14px;top:14px;bottom:14px;width:30px;background:radial-gradient(circle,#FFE9E4 0 5px,#B9A99C 5px 8px,transparent 8px) 0 0/30px 34px repeat-y}
.tape{position:absolute;top:-11px;left:44%;width:84px;height:24px;background:rgba(255,170,160,.65);transform:rotate(-3deg);box-shadow:0 1px 3px rgba(0,0,0,.12)}
.stk{position:absolute;font-size:34px;z-index:2;filter:drop-shadow(2px 0 0 #fff) drop-shadow(-2px 0 0 #fff) drop-shadow(0 2px 0 #fff) drop-shadow(0 -2px 0 #fff) drop-shadow(0 3px 4px rgba(0,0,0,.25));animation:flt 4s ease-in-out infinite}
.sec{margin-top:18px}.sec>b{font-family:Caveat,cursive;font-size:24px;color:#C97A6A;display:block;margin-bottom:4px}
.page .it{background:transparent;box-shadow:none;border-radius:0;border-bottom:1.5px dashed #EBD9C6;padding:8px 2px;margin:0;min-height:50px}
.page .it .ic{width:34px;height:34px;font-size:18px;border-radius:50%}
.stars{color:#F6B73C;font-size:28px;letter-spacing:3px}.stars span{display:inline-block;animation:pop .5s both;animation-delay:calc(var(--i)*.12s)}
.note{border:2px dashed #E8C9BD;border-radius:14px;padding:6px 8px;background:rgba(255,255,255,.7)}.note textarea{border:0;background:transparent;margin:0;padding:4px}
textarea{line-height:28px;background:#fff repeating-linear-gradient(transparent 0 27px,#F1E3D6 27px 28px)}
.dw{position:relative;width:100px;height:100px;flex:none}.dw .donut{width:100px;height:100px}.dw b{position:absolute;inset:0;display:grid;place-items:center;font-size:18px}
.tk{margin-bottom:12px;border-left:8px solid var(--c)}.tkh{display:flex;gap:12px;align-items:center}.tk .ic{width:46px;height:46px;border-radius:50%;background:var(--c);display:grid;place-items:center;font-size:22px}
.tk em{font-style:normal;font-size:11px;width:24px;height:24px;display:inline-grid;place-items:center;border-radius:50%;background:#F6EAE4;color:var(--mu);margin-right:3px}.tk em.on{background:var(--pk);color:var(--tx);font-weight:800}
.pbr{display:flex;align-items:center;gap:10px;margin-top:10px}.pbr .pb{flex:1;margin:0}
.tabs{background:#FFD9DE}.tabs .on{background:var(--pk);color:#B5475D;box-shadow:none}
.cal{display:grid;grid-template-columns:repeat(7,1fr);gap:3px}.wk{background:var(--pk);border-radius:8px;text-align:center;font-weight:800;font-size:11px;padding:6px 0}
.cd{min-height:58px;background:#fff;border-radius:8px;padding:3px;overflow:hidden;border:1px solid #F8E6E0}.cd small{font-size:11px;font-weight:700}.cd span{display:block;line-height:1.15;font-size:12px}.cd.td{outline:2px solid var(--ped)}.cd.fut{opacity:.45}
.bdg .e{background:#fff;border-radius:50%;width:66px;height:66px;display:grid;place-items:center;font-size:34px;box-shadow:0 0 0 4px #fff,0 4px 10px rgba(0,0,0,.18);transform:rotate(-8deg);flex:none}
.nav{background:rgba(255,255,255,.94);border-radius:24px}.nav .on{background:var(--pk);color:#B5475D}
section.in{animation:flip .55s cubic-bezier(.3,.8,.3,1) both;transform-origin:left center}
@keyframes flip{from{opacity:0;transform:perspective(1000px) rotateY(-14deg)}}
.stk.dr{animation:none;touch-action:none;cursor:grab;user-select:none;-webkit-user-select:none;z-index:3;font-size:36px}.stk.dr:active{cursor:grabbing;filter:drop-shadow(2px 0 0 #fff) drop-shadow(-2px 0 0 #fff) drop-shadow(0 2px 0 #fff) drop-shadow(0 -2px 0 #fff) drop-shadow(0 8px 8px rgba(0,0,0,.3))}
.page{transition:background .4s}
.page.t-cek{background-color:#F2FAF5;background-image:linear-gradient(#D5EBDD 1px,transparent 1px),linear-gradient(90deg,#D5EBDD 1px,transparent 1px);background-size:20px 20px}
.t-cek .tape{background:rgba(141,181,160,.65)}.t-cek .sec>b,.t-cek .hw{color:#5E9279}.t-cek .it{background:rgba(255,255,255,.75);border-radius:14px;border-bottom:0;margin-bottom:8px;padding:8px 10px}
.page.t-diary{background-color:#FFF6F0;background-image:repeating-linear-gradient(transparent 0 27px,#F0DACF 27px 28px);background-size:auto}
.t-diary .tape{background:rgba(190,180,230,.7)}.t-diary .hw{font-size:42px}.t-diary .sec>b{color:#8E7CC3}.t-diary .note{background:#fff}.t-diary .note textarea{min-height:190px}
.page.t-pink{background-color:#FFE6EC;background-image:radial-gradient(#FFB9C8 2px,transparent 2.4px);background-size:22px 22px}
.t-pink .tape{background:rgba(255,130,160,.6)}.t-pink .sec>b,.t-pink .hw{color:#D9667F}.t-pink .it{border-bottom-color:#FFC1CF}
.cv{position:absolute;inset:0;width:100%;height:100%;z-index:4;pointer-events:none;border-radius:inherit}.cv.on{pointer-events:auto;touch-action:none;cursor:crosshair}
.dtool{position:fixed;left:12px;right:12px;bottom:calc(12px + env(safe-area-inset-bottom));max-width:520px;margin:auto;background:#fff;border-radius:24px;box-shadow:0 8px 30px rgba(91,64,54,.25);padding:10px;display:flex;gap:7px;align-items:center;justify-content:center;flex-wrap:wrap;z-index:30;animation:up .3s cubic-bezier(.3,.8,.3,1)}
.dtool button{min-width:40px;height:40px;border-radius:50%;border:3px solid #fff;box-shadow:0 0 0 1.5px #EBD9C6;font-size:15px;font-weight:800}.dtool .sel{box-shadow:0 0 0 3px var(--ped)}
@media print{*{-webkit-print-color-adjust:exact;print-color-adjust:exact}.nav,.side,.noprint,.btn{display:none!important}body{background:#fff}main{margin:0;max-width:none;padding:0}.page{box-shadow:none}}
</style></head>
<body><div id="app"></div>
<script type="module">
// ===== KONFIGURASI APLIKASI =====
const IS_PREVIEW = false; // Set false JIKA SUDAH TERHUBUNG KE FIREBASE
// PASTE FIREBASE CONFIG ANDA DI SINI
const firebaseConfig = {
 apiKey: "AIzaSyCrmsjvWerDSX3j23QWbDkd4-PUoHgkM1c",
  authDomain: "my-habbit-7ba86.firebaseapp.com",
  projectId: "my-habbit-7ba86",
  storageBucket: "my-habbit-7ba86.firebasestorage.app",
  messagingSenderId: "903956031112",
  appId: "1:903956031112:web:581252f3e1c5c6904ee13d",
  measurementId: "G-WFQ4WPEYP4"

};

const $=(s,e=document)=>e.querySelector(s);
const dk=d=>new Date(d.getTime()-d.getTimezoneOffset()*6e4).toISOString().slice(0,10);
const addD=n=>{const d=new Date();d.setDate(d.getDate()+n);return dk(d)};
const today=()=>addD(0);
const esc=s=>String(s||'').replace(/[&<>"]/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;'}[c]));
const sha=async s=>[...new Uint8Array(await crypto.subtle.digest('SHA-256',new TextEncoder().encode(s)))].map(b=>b.toString(16).padStart(2,'0')).join('');
const CAT={Sehat:'#FFC9A8',Belajar:'#D9D2F0',Produktif:'#BFE3D0',Mindful:'#F9D5E5',Lainnya:'#FFE3A3'};
const ICONS=['💧','📚','🏃','🧘','🥗','😴','✍️','🎧','🧹','💊','🌱','🦷'];
const DN=['Min','Sen','Sel','Rab','Kam','Jum','Sab'];
const S={role:null,user:null,view:'home',habits:[],logs:{},users:[],tab:'user',lp:0,np:0,anim:true,pop:null,mood:'',hf:null};
let DB,Auth;

// ===== DATABASE (Preview = localStorage, Produksi = Firebase) =====
async function initDB(){
  if(IS_PREVIEW){
    const L=k=>JSON.parse(localStorage.getItem('ph_'+k)||'{}'),W=(k,o)=>localStorage.setItem('ph_'+k,JSON.stringify(o));
    DB={list:async(c,f,v)=>Object.values(L(c)).filter(x=>!f||x[f]===v),
      get:async(c,i)=>L(c)[i]||null,
      set:async(c,i,o)=>{const a=L(c);a[i]={...a[i],...o,id:i};W(c,a)},
      del:async(c,i)=>{const a=L(c);delete a[i];W(c,a)}};
    Auth={login:async(e,p)=>{if(e==='admin@demo.com'&&p==='admin123')return{email:e};throw 0},out:async()=>{}};
  }else{
    const B='https://www.gstatic.com/firebasejs/10.12.2/';
    const [A,F,U]=await Promise.all([import(B+'firebase-app.js'),import(B+'firebase-firestore.js'),import(B+'firebase-auth.js')]);
    const app=A.initializeApp(firebaseConfig),fs=F.getFirestore(app),au=U.getAuth(app);
    DB={list:async(c,f,v)=>(await F.getDocs(f?F.query(F.collection(fs,c),F.where(f,'==',v)):F.collection(fs,c))).docs.map(d=>({...d.data(),id:d.id})),
      get:async(c,i)=>{const s=await F.getDoc(F.doc(fs,c,i));return s.exists()?{...s.data(),id:i}:null},
      set:(c,i,o)=>F.setDoc(F.doc(fs,c,i),o,{merge:true}),
      del:(c,i)=>F.deleteDoc(F.doc(fs,c,i))};
    Auth={login:async(e,p)=>(await U.signInWithEmailAndPassword(au,e,p)).user,out:()=>U.signOut(au)};
  }
}
// Isi data contoh otomatis saat pertama kali dijalankan
async function autoSetupDatabase(){
  if(await DB.get('meta','setup'))return;
  await DB.set('users','mia',{username:'mia',nama:'Mia',passHash:await sha('1234'),createdAt:today()});
  const hs=[['💧','Minum 8 gelas air','Sehat'],['📚','Baca 15 menit','Belajar'],['🧘','Meditasi singkat','Mindful'],['🏃','Jalan pagi','Sehat'],['✍️','Tulis jurnal','Produktif']];
  const ids=[];
  for(let i=0;i<hs.length;i++){const id='h_seed'+i;ids.push(id);
    await DB.set('habits',id,{id,userId:'mia',ikon:hs[i][0],nama:hs[i][1],kat:hs[i][2],hariAktif:[0,1,2,3,4,5,6],createdAt:addD(-14),arsip:false})}
  for(let d=1;d<=13;d++){const sel=ids.filter((_,k)=>d<=4||(d*7+k*3)%5!==0);const t=addD(-d);
    await DB.set('logs','mia_'+t,{userId:'mia',tanggal:t,selesai:sel,mood:['😄','🙂','😐'][d%3],catatan:d%4===0?'Hari yang tenang dan produktif.':''})}
  await DB.set('meta','setup',{done:true});
}

// ===== LOGIKA HABIT =====
const sched=d=>{const w=new Date(d+'T00:00').getDay();return S.habits.filter(h=>!h.arsip&&h.createdAt<=d&&h.hariAktif.includes(w))};
const dayStat=d=>{const s=sched(d),l=(S.logs[d]||{}).selesai||[];return{t:s.length,d:s.filter(h=>l.includes(h.id)).length}};
const streak=()=>{let n=0,i=0;const st=dayStat(addD(0));if(st.t&&st.d<st.t)i=1;
  for(;i<365;i++){const s=dayStat(addD(-i));if(!s.t)continue;if(s.d===s.t)n++;else break}return n};
const bestStreak=()=>{let r=0,b=0;for(let i=364;i>=0;i--){const s=dayStat(addD(-i));if(!s.t)continue;if(s.d===s.t){r++;b=Math.max(b,r)}else r=0}return b};
const totalDone=()=>Object.values(S.logs).reduce((a,l)=>a+(l.selesai||[]).length,0);
const greet=()=>{const h=new Date().getHours();return h<11?'Selamat pagi':h<15?'Selamat siang':h<18?'Selamat sore':'Selamat malam'};
async function loadUser(){
  S.habits=await DB.list('habits','userId',S.user.id);
  S.logs={};(await DB.list('logs','userId',S.user.id)).forEach(l=>S.logs[l.tanggal]=l);
  S.view='home';S.lp=0;
}
async function loadAdmin(){S.users=await DB.list('users')}

// ===== AKSI =====
const toast=m=>{const t=document.createElement('div');t.className='toast';t.textContent=m;document.body.appendChild(t);setTimeout(()=>t.remove(),2200)};
function burst(ev){const x=ev.clientX||innerWidth/2,y=ev.clientY||innerHeight/2;
  for(let i=0;i<8;i++){const p=document.createElement('span'),a=i/8*6.28;p.className='petal';p.textContent=i%2?'🌸':'🍑';
    p.style.cssText=`left:${x}px;top:${y}px;--dx:${Math.cos(a)*70}px;--dy:${Math.sin(a)*70-20}px`;document.body.appendChild(p);setTimeout(()=>p.remove(),950)}}
async function tog(id,ev){
  const t=today(),l=S.logs[t]||{userId:S.user.id,tanggal:t,selesai:[],mood:'',catatan:''};
  const i=l.selesai.indexOf(id);
  if(i<0){l.selesai.push(id);burst(ev);S.pop=id}else l.selesai.splice(i,1);
  const cn=$('#cn');if(cn)l.catatan=cn.value.trim();S.logs[t]=l;render();S.pop=null;
  await DB.set('logs',S.user.id+'_'+t,l);
  if(i<0&&dayStat(t).t&&dayStat(t).d===dayStat(t).t)toast('Hebat! Semua habit hari ini selesai 🎉');
}
function go(v){S.view=v;S.anim=true;closeSheet();render();scrollTo(0,0)}
function closeSheet(){document.querySelectorAll('.bd,.sheet').forEach(e=>e.remove())}
function sheet(h){closeSheet();document.body.insertAdjacentHTML('beforeend','<div class="bd" id="bdp"></div><div class="sheet">'+h+'</div>');$('#bdp').onclick=closeSheet}
function hm(id){
  const h=S.habits.find(x=>x.id===id)||{nama:'',ikon:'💧',kat:'Sehat',hariAktif:[0,1,2,3,4,5,6]};
  S.hf={...h,hariAktif:[...h.hariAktif]};
  sheet(`<h2>${id?'Ubah habit':'Habit baru'}</h2><label class="mu">Nama habit</label><input id="hn" maxlength="40" placeholder="Contoh: Minum air putih" value="${esc(h.nama)}">
  <label class="mu">Ikon</label><div class="chips">${ICONS.map(e=>`<button class="${e===h.ikon?'sel':''}" onclick="S.hf.ikon='${e}';pick(this)">${e}</button>`).join('')}</div>
  <label class="mu">Kategori</label><select id="hk">${Object.keys(CAT).map(k=>`<option ${k===h.kat?'selected':''}>${k}</option>`).join('')}</select>
  <label class="mu">Hari aktif</label><div class="chips">${DN.map((n,i)=>`<button class="${h.hariAktif.includes(i)?'sel':''}" onclick="dayT(${i},this)">${n}</button>`).join('')}</div>
  <button class="btn" style="width:100%" onclick="hsave()">Simpan habit</button>`);
}
function pick(b){[...b.parentNode.children].forEach(c=>c.classList.remove('sel'));b.classList.add('sel')}
function dayT(i,b){const a=S.hf.hariAktif,k=a.indexOf(i);k<0?a.push(i):a.splice(k,1);b.classList.toggle('sel')}
async function hsave(){
  const f=S.hf;f.nama=$('#hn').value.trim();f.kat=$('#hk').value;
  if(!f.nama)return toast('Isi nama habit dulu');
  if(!f.hariAktif.length)return toast('Pilih minimal satu hari');
  const id=f.id||'h'+Date.now(),o={...f,id,userId:S.user.id,createdAt:f.createdAt||today(),arsip:false};
  const i=S.habits.findIndex(x=>x.id===id);i<0?S.habits.push(o):S.habits[i]=o;
  closeSheet();render();toast('Habit disimpan');await DB.set('habits',id,o);
}
async function hdel(id){
  if(!confirm('Hapus habit ini? Riwayat lama tetap tersimpan.'))return;
  S.habits.find(h=>h.id===id).arsip=true;render();toast('Habit dihapus');await DB.set('habits',id,{arsip:true});
}
async function saveNote(){
  const t=today(),l=S.logs[t]||{userId:S.user.id,tanggal:t,selesai:[]};
  l.mood=S.mood||l.mood||'';l.catatan=$('#cn').value.trim();S.logs[t]=l;
  await DB.set('logs',S.user.id+'_'+t,l);toast('Catatan tersimpan');render();
}
async function saveName(){const n=$('#pn').value.trim();if(!n)return toast('Nama tidak boleh kosong');S.user.nama=n;await DB.set('users',S.user.id,{nama:n});toast('Nama diperbarui');render()}
async function savePass(){const p=$('#pp').value;if(p.length<4)return toast('Password minimal 4 karakter');await DB.set('users',S.user.id,{passHash:await sha(p)});$('#pp').value='';toast('Password diperbarui')}
async function logout(){localStorage.removeItem('ph_sess');try{await Auth.out()}catch(e){}S.role=null;S.user=null;render()}
async function doLogin(){
  const u=$('#lu').value.trim(),p=$('#lp').value;
  try{
    if(S.tab==='admin'){await Auth.login(u,p);S.role='admin';await loadAdmin()}
    else{const d=await DB.get('users',u.toLowerCase());if(!d||d.passHash!==await sha(p))throw 0;S.role='user';S.user=d;localStorage.setItem('ph_sess',d.id);await loadUser()}
    S.anim=true;render();
  }catch(e){$('#er').textContent=S.tab==='admin'?'Email atau password admin salah.':'Username atau password salah.'}
}
async function addUser(){
  const u=$('#au').value.trim().toLowerCase(),n=$('#an').value.trim(),p=$('#ap').value;
  if(!/^[a-z0-9_]{3,20}$/.test(u))return toast('Username 3-20 huruf kecil/angka/_');
  if(!n||p.length<4)return toast('Lengkapi nama dan password (min 4)');
  if(await DB.get('users',u))return toast('Username sudah dipakai');
  await DB.set('users',u,{username:u,nama:n,passHash:await sha(p),createdAt:today()});await loadAdmin();render();toast('Pengguna ditambahkan');
}
async function delUser(u){if(!confirm('Hapus pengguna '+u+'?'))return;await DB.del('users',u);await loadAdmin();render();toast('Pengguna dihapus')}
async function resetPass(u){const p=prompt('Password baru untuk '+u+' (min 4 karakter):');if(!p||p.length<4)return;await DB.set('users',u,{passHash:await sha(p)});toast('Password direset')}
Object.assign(window,{S,tog,go,hm,pick,dayT,hsave,hdel,saveNote,saveName,savePass,logout,doLogin,addUser,delUser,resetPass,closeSheet,setTab:t=>{S.tab=t;render()},setMood:(m,b)=>{S.mood=m;pick(b)}});

// ===== TAMPILAN =====
const masc=()=>`<svg class="masc" viewBox="0 0 100 100"><ellipse cx="50" cy="56" rx="36" ry="34" fill="#FFB894"/><path d="M50 22c-2-9 6-14 14-12-2 8-6 12-14 12z" fill="#8DB5A0"/><g class="eyes"><ellipse cx="38" cy="55" rx="4" ry="5.5" fill="#5B4036"/><ellipse cx="62" cy="55" rx="4" ry="5.5" fill="#5B4036"/></g><circle cx="30" cy="66" r="6" fill="#FF9C8A" opacity=".5"/><circle cx="70" cy="66" r="6" fill="#FF9C8A" opacity=".5"/><path d="M43 68q7 7 14 0" stroke="#5B4036" stroke-width="3" fill="none" stroke-linecap="round"/></svg>`;
const item=(h,on)=>`<button class="it ${on?'on':''}" style="--c:${CAT[h.kat]||CAT.Lainnya}" onclick="tog('${h.id}',event)"><span class="ic">${h.ikon}</span><span class="nm">${esc(h.nama)}</span><span class="ck ${S.pop===h.id?'pop':''}">${on?'✓':''}</span></button>`;
const empty=(m,b)=>`<div class="card" style="text-align:center"><p class="mu" style="margin-bottom:12px">${m}</p>${b||''}</div>`;

const V={
home(){
  const t=today(),st=dayStat(t),l=(S.logs[t]||{}).selesai||[];S.np=st.t?st.d/st.t:0;
  return `<div class="card hero"><div><p class="mu">${new Date().toLocaleDateString('id-ID',{weekday:'long',day:'numeric',month:'long'})}</p><h1>${greet()}, ${esc(S.user.nama)}!</h1><p>${!st.t?'Belum ada habit untuk hari ini.':st.d===st.t?'Semua habit selesai. Kamu hebat! 🎉':`Tinggal ${st.t-st.d} lagi, semangat!`}</p></div>${masc()}</div>
  <div class="row"><div class="card ringc"><svg viewBox="0 0 100 100"><circle cx="50" cy="50" r="42" class="rb"/><circle id="ring" cx="50" cy="50" r="42" class="rf" style="stroke-dashoffset:${264*(1-S.lp)}"/></svg><b>${st.d}/${st.t}</b></div>
  <button class="card streak" onclick="go('ach')"><span class="fl">🔥</span><b>${streak()}</b><small>hari beruntun</small></button></div>
  <div class="hd"><h2>Hari ini</h2><button class="lnk" onclick="go('habits')">Kelola habit ›</button></div>
  ${sched(t).map(h=>item(h,l.includes(h.id))).join('')||empty('Tambahkan habit pertamamu.','<button class="btn" onclick="hm()">Tambah habit</button>')}`},
habits(){
  const hs=S.habits.filter(h=>!h.arsip);
  return `<div class="hd"><h1>Kebiasaan</h1><button class="btn" onclick="hm()">+ Baru</button></div>
  ${hs.map(h=>`<div class="it" style="--c:${CAT[h.kat]||CAT.Lainnya}"><span class="ic">${h.ikon}</span><span class="nm">${esc(h.nama)}<br><small>${h.kat} · ${h.hariAktif.length===7?'Setiap hari':h.hariAktif.map(i=>DN[i]).join(', ')}</small></span><span class="act"><button onclick="hm('${h.id}')" aria-label="Ubah">✏️</button><button onclick="hdel('${h.id}')" aria-label="Hapus">🗑️</button></span></div>`).join('')||empty('Belum ada habit.')}`},
stats(){
  const bars=[];for(let i=6;i>=0;i--){const d=addD(-i),s=dayStat(d),p=s.t?s.d/s.t:0;bars.push(`<div class="bc"><small>${Math.round(p*100)}%</small><i style="--h:${p*80}%"></i><small>${DN[new Date(d+'T00:00').getDay()]}</small></div>`)}
  const cnt={};for(let i=0;i<30;i++){((S.logs[addD(-i)]||{}).selesai||[]).forEach(id=>{const h=S.habits.find(x=>x.id===id);if(h)cnt[h.kat]=(cnt[h.kat]||0)+1})}
  const tot=Object.values(cnt).reduce((a,b)=>a+b,0);let acc=0;
  const seg=Object.entries(cnt).map(([k,v])=>{const a=acc/tot*100;acc+=v;return `${CAT[k]} ${a}% ${acc/tot*100}%`}).join(',');
  const n=new Date(),y=n.getFullYear(),m=n.getMonth(),dim=new Date(y,m+1,0).getDate(),off=(new Date(y,m,1).getDay()+6)%7;let cells='<div style="background:none"></div>'.repeat(off);
  for(let d=1;d<=dim;d++){const k=`${y}-${String(m+1).padStart(2,'0')}-${String(d).padStart(2,'0')}`,s=dayStat(k),p=s.t?s.d/s.t:0;
    cells+=`<div class="${k>today()?'fut':''}" style="background:${s.t&&k<=today()?`rgba(244,149,107,${.15+p*.85})`:'#FFF1E6'}">${d}</div>`}
  return `<h1>Statistik</h1><div class="card" style="margin:14px 0"><h2>7 hari terakhir</h2><div class="bars" style="margin-top:14px">${bars.join('')}</div></div>
  <div class="card" style="margin-bottom:14px"><h2>Habit selesai per kategori (30 hari)</h2><div style="display:flex;gap:18px;align-items:center;margin-top:14px">${tot?`<div class="donut" style="background:conic-gradient(${seg})"></div><div>${Object.entries(cnt).map(([k,v])=>`<div class="lg"><i style="background:${CAT[k]}"></i>${k}: ${v}</div>`).join('')}</div>`:'<p class="mu">Belum ada data.</p>'}</div></div>
  <div class="card"><h2>${n.toLocaleDateString('id-ID',{month:'long',year:'numeric'})}</h2><div class="hm" style="margin-top:12px">${['S','S','R','K','J','S','M'].map(x=>`<small style="text-align:center">${x}</small>`).join('')}${cells}</div></div>
  <button class="btn s" style="width:100%;margin-top:14px" onclick="go('ach')">Lihat pencapaian ›</button>`},
ach(){
  const b=bestStreak(),t=totalDone();
  const L=[['🌱','Langkah pertama','Centang 1 habit',t,1],['🔥','Konsisten 3 hari','Streak 3 hari',b,3],['⭐','Seminggu penuh','Streak 7 hari',b,7],['👑','Sebulan juara','Streak 30 hari',b,30],['🌸','50 centang','Total 50 centang',t,50],['🏆','100 centang','Total 100 centang',t,100]];
  return `<h1>Pencapaian</h1><p class="mu" style="margin:4px 0 14px">Streak saat ini ${streak()} hari · terbaik ${b} hari · total ${t} centang</p>
  ${L.map(x=>`<div class="card bdg ${x[3]>=x[4]?'':'lock'}" style="margin-bottom:12px"><span class="e">${x[0]}</span><div style="flex:1"><b>${x[1]}</b><br><small>${x[2]} · ${Math.min(x[3],x[4])}/${x[4]}</small><div class="pb"><i style="width:${Math.min(x[3]/x[4],1)*100}%"></i></div></div></div>`).join('')}`},
notes(){
  const t=today(),l=S.logs[t]||{};S.mood=l.mood||'';
  const past=Object.values(S.logs).filter(x=>x.catatan&&x.tanggal!==t).sort((a,b)=>b.tanggal.localeCompare(a.tanggal)).slice(0,7);
  return `<h1>Catatan harian</h1><div class="card" style="margin:14px 0"><p class="mu" style="margin-bottom:8px">Bagaimana perasaanmu hari ini?</p>
  <div class="moods">${['😄','🙂','😐','😔','😴'].map(m=>`<button class="${m===S.mood?'sel':''}" onclick="setMood('${m}',this)">${m}</button>`).join('')}</div>
  <textarea id="cn" rows="4" maxlength="400" placeholder="Tulis cerita singkat harimu...">${esc(l.catatan)}</textarea><button class="btn" style="width:100%" onclick="saveNote()">Simpan catatan</button></div>
  ${past.length?'<div class="hd"><h2>Catatan sebelumnya</h2></div>':''}${past.map(x=>`<div class="card" style="margin-bottom:10px"><small>${new Date(x.tanggal+'T00:00').toLocaleDateString('id-ID',{weekday:'long',day:'numeric',month:'short'})} ${x.mood||''}</small><p>${esc(x.catatan)}</p></div>`).join('')}`},
me(){
  return `<h1>Profil</h1><div class="card" style="margin:14px 0;text-align:center">${masc()}<h2>${esc(S.user.nama)}</h2><small>@${esc(S.user.id)}</small></div>
  <div class="card" style="margin-bottom:14px"><label class="mu">Nama tampilan</label><input id="pn" value="${esc(S.user.nama)}"><button class="btn s" onclick="saveName()">Simpan nama</button></div>
  <div class="card" style="margin-bottom:14px"><label class="mu">Password baru</label><input id="pp" type="password" placeholder="Minimal 4 karakter"><button class="btn s" onclick="savePass()">Ganti password</button></div>
  <button class="btn" style="width:100%" onclick="logout()">Keluar</button>`}
};
const STK=['🌸','⭐','🍓','🦋','🌿','☁️','🐱','🎀','☕','💌'];
const stkEl=(s,i)=>`<span class="stk dr" data-i="${i}" style="left:${s.x}%;top:${s.y}%;transform:rotate(${s.r}deg)">${s.e}</span>`;
const stkTray=()=>`<div class="sec noprint"><b>Tempel stiker</b><div class="chips">${STK.map(e=>`<button onclick="stkAdd('${e}')">${e}</button>`).join('')}<button onclick="stkClr()" aria-label="Hapus semua stiker">🧽</button></div><small>Geser untuk memindahkan, ketuk dua kali untuk menghapus.</small></div>`;
const curLog=()=>{const t=today();return S.logs[t]||(S.logs[t]={userId:S.user.id,tanggal:t,selesai:[]})};
const stkSave=l=>DB.set('logs',S.user.id+'_'+today(),l);
const keepNote=l=>{const c=$('#cn');if(c)l.catatan=c.value.trim()};
Object.assign(window,{stkAdd:e=>{const l=curLog();(l.stiker=l.stiker||[]).push({e,x:10+Math.floor(Math.random()*70),y:8+Math.floor(Math.random()*80),r:Math.floor(Math.random()*40-20)});keepNote(l);render();stkSave(l)},stkClr:()=>{const l=curLog();l.stiker=[];keepNote(l);render();stkSave(l)}});
let drg=null,lastTap={i:-1,t:0};
document.addEventListener('pointerdown',e=>{const el=e.target.closest('.dr');if(!el)return;drg={el,pg:el.closest('.page').getBoundingClientRect(),mv:false};el.setPointerCapture(e.pointerId);e.preventDefault()});
document.addEventListener('pointermove',e=>{if(!drg)return;drg.mv=true;const{el,pg}=drg;el.style.left=Math.min(92,Math.max(-2,(e.clientX-pg.left)/pg.width*100-5))+'%';el.style.top=Math.min(97,Math.max(-2,(e.clientY-pg.top)/pg.height*100-3))+'%'});
document.addEventListener('pointerup',()=>{if(!drg)return;const{el,mv}=drg;drg=null;const l=curLog(),i=+el.dataset.i,s=l.stiker[i];if(!s)return;
 if(mv){s.x=parseFloat(el.style.left);s.y=parseFloat(el.style.top);stkSave(l);lastTap={i:-1,t:0}}
 else if(lastTap.i===i&&Date.now()-lastTap.t<350){keepNote(l);l.stiker.splice(i,1);render();stkSave(l);lastTap={i:-1,t:0}}
 else lastTap={i,t:Date.now()}});
const TEMA=[['rutin','📓','Rutinitas'],['cek','🌿','Checklist'],['diary','🌸','Diary'],['pink','🎀','Pink']];
const temaPick=l=>`<div class="chips noprint" style="margin-top:12px">${TEMA.map(t=>`<button class="${(l.tema||'rutin')===t[0]?'sel':''}" onclick="setTema('${t[0]}')" style="font-size:14px">${t[1]} ${t[2]}</button>`).join('')}</div>`;
window.setTema=t=>{const l=curLog();l.tema=t;keepNote(l);S.anim=true;render();stkSave(l)};
S.draw=false;S.pc='#5B4036';S.pw=3;let cs=null;
const COL=['#5B4036','#F4956B','#E8688A','#6BA58B','#6C8FD6','#9C84D6'];
const dpr=()=>Math.min(devicePixelRatio||1,2);
function paint(){const c=$('#cv');if(!c)return;const x=c.getContext('2d'),d=dpr();x.clearRect(0,0,c.width,c.height);x.lineCap=x.lineJoin='round';
 (curLog().coret||[]).forEach(s=>{x.globalCompositeOperation=s.e?'destination-out':'source-over';x.strokeStyle=s.c;x.lineWidth=s.w*d*(s.e?5:1);x.beginPath();s.p.forEach((q,i)=>i?x.lineTo(q[0]*c.width,q[1]*c.height):x.moveTo(q[0]*c.width,q[1]*c.height));if(s.p.length===1)x.lineTo(s.p[0][0]*c.width+.1,s.p[0][1]*c.height);x.stroke()});x.globalCompositeOperation='source-over'}
const dtool=()=>`<div class="dtool noprint">${COL.map(c=>`<button class="${S.pc===c?'sel':''}" style="background:${c}" onclick="dwSet('pc','${c}')" aria-label="Warna"></button>`).join('')}<button class="${S.pc==='e'?'sel':''}" onclick="dwSet('pc','e')" aria-label="Penghapus">🧽</button>${[2,4,8].map(w=>`<button class="${S.pw===w?'sel':''}" onclick="dwSet('pw',${w})" aria-label="Ketebalan ${w}">${w}</button>`).join('')}<button onclick="dwUndo()" aria-label="Urungkan">↶</button><button onclick="dwClr()" aria-label="Hapus semua coretan">🗑️</button><button onclick="dwToggle()" aria-label="Selesai" style="background:var(--ped);color:#fff">✓</button></div>`;
Object.assign(window,{cvInit:()=>{const c=$('#cv'),p=$('.page');if(!c||!p)return;const d=dpr();c.width=p.clientWidth*d;c.height=p.clientHeight*d;paint()},
 dwToggle:()=>{keepNote(curLog());S.draw=!S.draw;render()},
 dwSet:(k,v)=>{keepNote(curLog());S[k]=v;render()},
 dwUndo:()=>{const l=curLog();(l.coret||[]).pop();paint();stkSave(l)},
 dwClr:()=>{if(!confirm('Hapus semua coretan hari ini?'))return;const l=curLog();l.coret=[];paint();stkSave(l)}});
document.addEventListener('pointerdown',e=>{const c=e.target;if(c.id!=='cv'||!S.draw)return;const r=c.getBoundingClientRect(),l=curLog();cs={c:S.pc==='e'?'#000':S.pc,w:S.pw,e:S.pc==='e',p:[[+((e.clientX-r.left)/r.width).toFixed(4),+((e.clientY-r.top)/r.height).toFixed(4)]]};(l.coret=l.coret||[]).push(cs);c.setPointerCapture(e.pointerId);e.preventDefault();paint()});
document.addEventListener('pointermove',e=>{if(!cs)return;const r=$('#cv').getBoundingClientRect();cs.p.push([+((e.clientX-r.left)/r.width).toFixed(4),+((e.clientY-r.top)/r.height).toFixed(4)]);paint()});
document.addEventListener('pointerup',()=>{if(!cs)return;cs=null;stkSave(curLog())});
const oldStats=V.stats;S.st='month';S.mo=0;
Object.assign(window,{setSt:s=>{S.st=s;render()},moNav:n=>{S.mo=n?S.mo+n:0;render()},moodSet:async(m,b)=>{S.mood=m;pick(b);const t=today(),l=S.logs[t]||{userId:S.user.id,tanggal:t,selesai:[]};l.mood=m;S.logs[t]=l;await DB.set('logs',S.user.id+'_'+t,l)}});
Object.assign(V,{
home(){
 const t=today(),st=dayStat(t),l=S.logs[t]||{},ls=l.selesai||[],p=st.t?st.d/st.t:0,sr=Math.round(p*5);S.mood=l.mood||'';S.np=p;
 return `<div class="page t-${l.tema||'rutin'}"><i class="tape"></i>${(l.stiker||[]).map(stkEl).join('')}<canvas class="cv ${S.draw?'on':''}" id="cv"></canvas>${S.draw?dtool():''}<img alt="" width="1" height="1" style="position:absolute;opacity:0" src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" onload="cvInit()"><span class="stk" style="right:12px;top:-18px;transform:rotate(12deg)">🍑</span>
 <p class="mu">${new Date().toLocaleDateString('id-ID',{weekday:'long',day:'numeric',month:'long'})}</p><h1 class="hw">${greet()}, ${esc(S.user.nama)}!</h1>
 ${temaPick(l)}<div class="chips noprint" style="margin-top:0"><button class="${S.draw?'sel':''}" onclick="dwToggle()" style="font-size:14px">✏️ ${S.draw?'Selesai menggambar':'Gambar di halaman'}</button></div><div class="sec"><b>Mood hari ini</b><div class="moods">${['😄','🙂','😐','😔','😴'].map(m=>`<button class="${m===S.mood?'sel':''}" onclick="moodSet('${m}',this)">${m}</button>`).join('')}</div></div>
 <div class="sec" style="display:flex;gap:16px;align-items:center"><div class="dw"><div class="donut" style="background:conic-gradient(var(--sage) 0 ${p*100}%,#FFD3C7 ${p*100}% 100%)"></div><b>${st.d}/${st.t}</b></div><div style="flex:1"><div class="lg"><i style="background:var(--sage)"></i>Selesai ${st.d}</div><div class="lg"><i style="background:#FFD3C7"></i>Belum ${st.t-st.d}</div><button class="lnk" onclick="go('ach')">🔥 ${streak()} hari beruntun ›</button></div></div>
 <div class="sec"><b>Daftar tugas</b>${sched(t).map(h=>item(h,ls.includes(h.id))).join('')||empty('Belum ada habit hari ini.','<button class="btn" onclick="hm()">Tambah habit</button>')}</div>
 <div class="sec"><b>Produktivitas</b><div class="stars">${[0,1,2,3,4].map(i=>`<span style="--i:${i}">${i<sr?'★':'☆'}</span>`).join('')}</div></div>
 ${stkTray()}<div class="sec"><b>Catatan</b><div class="note"><textarea id="cn" rows="3" maxlength="400" placeholder="Tulis sesuatu...">${esc(l.catatan)}</textarea></div><button class="btn s" style="margin-top:10px" onclick="saveNote()">Simpan catatan</button> <button class="btn s noprint" style="margin-top:10px" onclick="print()">📄 Ekspor PDF</button></div></div>`},
habits(){
 const hs=S.habits.filter(h=>!h.arsip);
 return `<div class="hd"><h1 class="hw">Daftar Tugas</h1><button class="btn" onclick="hm()">+ Baru</button></div>`+(hs.map(h=>{let d=0,t=0;for(let i=0;i<7;i++){const k=addD(-i);if(sched(k).some(x=>x.id===h.id)){t++;if(((S.logs[k]||{}).selesai||[]).includes(h.id))d++}}const p=t?Math.round(d/t*100):0;
  return `<div class="card tk" style="--c:${CAT[h.kat]||CAT.Lainnya}"><div class="tkh"><span class="ic">${h.ikon}</span><div style="flex:1"><b>${esc(h.nama)}</b><br><small>${h.kat}</small></div><span class="act"><button onclick="hm('${h.id}')" aria-label="Ubah">✏️</button><button onclick="hdel('${h.id}')" aria-label="Hapus">🗑️</button></span></div><div style="margin-top:10px">${DN.map((n,i)=>`<em class="${h.hariAktif.includes(i)?'on':''}">${n[0]}</em>`).join('')}</div><div class="pbr"><div class="pb"><i style="width:${p}%"></i></div><small>${p}% minggu ini</small></div></div>`}).join('')||empty('Belum ada habit.'))},
stats(){
 const tabs=`<div class="tabs"><button class="${S.st==='month'?'on':''}" onclick="setSt('month')">Bulan</button><button class="${S.st==='week'?'on':''}" onclick="setSt('week')">Minggu</button></div>`;
 if(S.st==='week')return tabs+oldStats();
 const n=new Date(),b=new Date(n.getFullYear(),n.getMonth()+S.mo,1),y=b.getFullYear(),m=b.getMonth(),dim=new Date(y,m+1,0).getDate(),off=(b.getDay()+6)%7;let c='<div></div>'.repeat(off);
 for(let d=1;d<=dim;d++){const k=`${y}-${String(m+1).padStart(2,'0')}-${String(d).padStart(2,'0')}`,e=((S.logs[k]||{}).selesai||[]).map(id=>S.habits.find(h=>h.id===id)).filter(Boolean).map(h=>h.ikon);
  c+=`<div class="cd ${k===today()?'td':''} ${k>today()?'fut':''}"><small>${d}</small><span>${e.slice(0,4).join('')}${e.length>4?'+':''}</span></div>`}
 return `${tabs}<div class="card"><div class="hd" style="margin-top:0"><button class="lnk" onclick="moNav(-1)" aria-label="Bulan sebelumnya">‹</button><h2>${b.toLocaleDateString('id-ID',{month:'long',year:'numeric'}).toUpperCase()}</h2><button class="lnk" onclick="moNav(1)" aria-label="Bulan berikutnya">›</button></div><div class="cal">${['SEN','SEL','RAB','KAM','JUM','SAB','MIN'].map(x=>`<div class="wk">${x}</div>`).join('')}${c}</div>${S.mo?'<button class="btn s" style="width:100%;margin-top:12px" onclick="moNav(0)">Kembali ke bulan ini</button>':''}</div>`}
});
const adminV=()=>`<div class="hd"><h1>Panel Admin</h1><button class="btn s" onclick="logout()">Keluar</button></div>
  <div class="row"><div class="card streak"><b>${S.users.length}</b><small>pengguna terdaftar</small></div><div class="card streak" style="background:var(--mint)"><span class="fl">🍑</span><small>PeachHabit</small></div></div>
  <div class="card" style="margin-bottom:14px"><h2>Tambah pengguna</h2><input id="au" placeholder="Username (huruf kecil)"><input id="an" placeholder="Nama"><input id="ap" type="password" placeholder="Password"><button class="btn" style="width:100%" onclick="addUser()">Tambah pengguna</button></div>
  ${S.users.map(u=>`<div class="it" style="--c:var(--lav)"><span class="ic">🧸</span><span class="nm">${esc(u.nama)}<br><small>@${esc(u.id)}</small></span><span class="act"><button onclick="resetPass('${u.id}')" aria-label="Reset password">🔑</button><button onclick="delUser('${u.id}')" aria-label="Hapus">🗑️</button></span></div>`).join('')}`;
const loginV=()=>`<div class="login">${masc()}<h1 style="margin:8px 0 4px">PeachHabit</h1><p class="mu" style="margin-bottom:20px">Satu centang kecil setiap hari.</p>
  <div class="tabs"><button class="${S.tab==='user'?'on':''}" onclick="setTab('user')">Pengguna</button><button class="${S.tab==='admin'?'on':''}" onclick="setTab('admin')">Admin</button></div>
  <div class="card"><input id="lu" autocomplete="username" placeholder="${S.tab==='admin'?'Email admin':'Username'}"><input id="lp" type="password" autocomplete="current-password" placeholder="Password" onkeydown="if(event.key==='Enter')doLogin()"><p class="err" id="er"></p><button class="btn" style="width:100%" onclick="doLogin()">Masuk</button></div>
  ${IS_PREVIEW?`<p class="mu" style="margin-top:14px">Mode preview — ${S.tab==='admin'?'admin@demo.com / admin123':'mia / 1234'}</p>`:''}</div>`;

function render(){
  const a=$('#app');
  if(!S.role){a.innerHTML=loginV();return}
  if(S.role==='admin'){a.innerHTML=`<main><section class="in">${adminV()}</section></main>`;return}
  const nav=[['home','📓','Jurnal'],['habits','✅','Planner'],['stats','🗓️','Kalender'],['ach','🌟','Stiker'],['notes','✍️','Catatan'],['me','🧸','Profil']];
  const mob=[nav[0],nav[2],null,nav[4],nav[5]];
  a.innerHTML=`<aside class="side"><h2>🍑 PeachHabit</h2>${nav.map(n=>`<button class="n ${S.view===n[0]?'on':''}" onclick="go('${n[0]}')">${n[1]}  ${n[2]}</button>`).join('')}<button class="n" onclick="hm()">＋  Habit baru</button></aside>
  <main><section class="${S.anim?'in':''}">${V[S.view]()}</section></main>
  <nav class="nav">${mob.map(n=>n?`<button class="${S.view===n[0]?'on':''}" onclick="go('${n[0]}')"><span>${n[1]}</span>${n[2]}</button>`:`<button class="fab" onclick="hm()" aria-label="Habit baru">+</button>`).join('')}</nav>`;
  S.anim=false;
  const r=$('#ring');if(r)requestAnimationFrame(()=>requestAnimationFrame(()=>{r.style.strokeDashoffset=264*(1-S.np);S.lp=S.np}));
}

// ===== PWA: Service Worker dibuat dinamis lewat Blob =====
try{if('serviceWorker' in navigator){const u=URL.createObjectURL(new Blob(["self.addEventListener('install',e=>self.skipWaiting());self.addEventListener('fetch',e=>{})"],{type:'text/javascript'}));navigator.serviceWorker.register(u).catch(()=>{})}}catch(e){}

// ===== MULAI =====
(async()=>{
  try{
    await initDB();await autoSetupDatabase();
    const id=localStorage.getItem('ph_sess');
    if(id){const u=await DB.get('users',id);if(u){S.role='user';S.user=u;await loadUser()}}
  }catch(e){console.error(e);document.getElementById('app').innerHTML='<div class="login"><p class="err">Gagal terhubung ke database. Periksa firebaseConfig dan Security Rules.</p></div>';return}
  render();
})();
</script></body></html>


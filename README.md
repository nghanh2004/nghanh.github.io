
lich-nhac-cong-viec.html

100%
<title>Sổ Hạn Thuế</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Be+Vietnam+Pro:wght@400;500;600;700&family=Literata:opsz,wght@7..72,600;7..72,700&family=JetBrains+Mono:wght@400;600&display=swap">
<style>
/* Layout: left rail navigation + working pane; tax-calendar ledger rows with severity stripes */
:root{
  --bg:#edf0f3; --surface:#ffffff; --surface2:#f4f6f8; --fg:#15202a; --muted:#5a6774; --line:#d8dee4;
  --accent:#0e5a6b; --accent-ink:#ffffff; --accent-soft:#d9ebef;
  --danger:#b3261e; --danger-soft:#fbe7e5; --warn:#9a5800; --warn-soft:#fcefd6;
  --ok:#1d7443; --ok-soft:#e0f2e7; --info:#3a5797; --info-soft:#e5ebf8;
  --shadow:0 1px 2px rgba(16,32,42,.06),0 4px 16px rgba(16,32,42,.06);
  --f-display:"Literata",Georgia,"Times New Roman",serif;
  --f-body:"Be Vietnam Pro",system-ui,-apple-system,"Segoe UI",Roboto,Arial,sans-serif;
  --f-mono:"JetBrains Mono",ui-monospace,"SFMono-Regular",Consolas,monospace;
}
@media (prefers-color-scheme: dark){:root:not([data-theme="light"]){
  --bg:#0e1418; --surface:#151d23; --surface2:#1b252c; --fg:#e2e8ed; --muted:#93a1ad; --line:#2a353e;
  --accent:#55b6c9; --accent-ink:#06161a; --accent-soft:#16343b;
  --danger:#f2867a; --danger-soft:#3a1b18; --warn:#eab25a; --warn-soft:#382912; --ok:#62c991; --ok-soft:#133022; --info:#93acea; --info-soft:#1b2440;
  --shadow:0 1px 2px rgba(0,0,0,.3); color-scheme:dark;}}
:root[data-theme="dark"]{
  --bg:#0e1418; --surface:#151d23; --surface2:#1b252c; --fg:#e2e8ed; --muted:#93a1ad; --line:#2a353e;
  --accent:#55b6c9; --accent-ink:#06161a; --accent-soft:#16343b;
  --danger:#f2867a; --danger-soft:#3a1b18; --warn:#eab25a; --warn-soft:#382912; --ok:#62c991; --ok-soft:#133022; --info:#93acea; --info-soft:#1b2440;
  --shadow:0 1px 2px rgba(0,0,0,.3); color-scheme:dark;}
*{box-sizing:border-box}
html,body{min-height:100%}
body{background:var(--bg);color:var(--fg);font-family:var(--f-body);font-size:14px;line-height:1.5}
button,input,select,textarea{font:inherit;color:inherit}
.mono{font-family:var(--f-mono);font-variant-numeric:tabular-nums}
.app{display:grid;grid-template-columns:232px minmax(0,1fr);min-height:100vh}
.rail{background:var(--surface);border-right:1px solid var(--line);padding:20px 14px;display:flex;flex-direction:column;gap:18px;position:sticky;top:env(safe-area-inset-top,0px);height:100vh}
.brand{display:flex;flex-direction:column;gap:2px;padding:0 8px}
.brand b{font-family:var(--f-display);font-size:21px;letter-spacing:-.01em}
.brand span{color:var(--muted);font-size:12px}
.nav{display:flex;flex-direction:column;gap:2px}
.nav button{display:flex;align-items:center;justify-content:space-between;gap:8px;background:none;border:0;border-radius:8px;padding:9px 10px;cursor:pointer;text-align:left;color:var(--muted);font-weight:500}
.nav button:hover{background:var(--surface2);color:var(--fg)}
.nav button[aria-current="page"]{background:var(--accent-soft);color:var(--accent);font-weight:600}
.badge{font-family:var(--f-mono);font-size:11px;min-width:22px;text-align:center;padding:1px 6px;border-radius:99px;background:var(--danger);color:var(--surface)}
.badge.w{background:var(--warn)}
.rail .foot{margin-top:auto;font-size:12px;color:var(--muted);padding:0 8px;display:flex;flex-direction:column;gap:4px}
.dot{display:inline-block;width:7px;height:7px;border-radius:50%;background:var(--muted);margin-right:6px;vertical-align:1px}
.dot.on{background:var(--ok)}
main{padding-block:24px 48px;padding-inline:28px;min-width:0;display:flex;flex-direction:column;gap:20px}
.head{display:flex;flex-wrap:wrap;align-items:flex-end;justify-content:space-between;gap:12px}
.head h1{font-family:var(--f-display);font-size:26px;line-height:1.2;margin:0;text-wrap:balance}
.head p{margin:2px 0 0;color:var(--muted)}
.row{display:flex;flex-wrap:wrap;gap:8px;align-items:center}
.btn{border:1px solid var(--line);background:var(--surface);border-radius:8px;padding:7px 12px;cursor:pointer;font-weight:500;display:inline-flex;align-items:center;gap:6px}
.btn:hover{border-color:var(--accent);color:var(--accent)}
.btn.pri{background:var(--accent);border-color:var(--accent);color:var(--accent-ink)}
.btn.pri:hover{filter:brightness(1.08);color:var(--accent-ink)}
.btn.sm{padding:3px 9px;font-size:12.5px}
.btn.danger{color:var(--danger)}
.btn.armed{background:var(--danger);border-color:var(--danger);color:var(--surface)}
:focus-visible{outline:2px solid var(--accent);outline-offset:2px}
.panel{background:var(--surface);border:1px solid var(--line);border-radius:12px;min-width:0}
.panel>h2{font-size:13px;text-transform:uppercase;letter-spacing:.06em;color:var(--muted);margin:0;padding:14px 16px 10px;font-weight:600;display:flex;justify-content:space-between;align-items:center;gap:8px}
.strip{display:grid;grid-template-columns:repeat(4,minmax(0,1fr));background:var(--surface);border:1px solid var(--line);border-radius:12px}
.strip>div{padding:14px 16px;border-left:1px solid var(--line);display:flex;flex-direction:column;gap:2px}
.strip>div:first-child{border-left:0}
.strip .n{font-family:var(--f-display);font-size:30px;line-height:1.1}
.strip .l{color:var(--muted);font-size:12.5px}
.strip .over .n{color:var(--danger)} .strip .soon .n{color:var(--warn)}
.grid2{display:grid;grid-template-columns:minmax(0,1.1fr) minmax(0,1fr);gap:20px;align-items:start}
.alerts{display:flex;flex-direction:column}
.al{display:grid;grid-template-columns:4px 92px minmax(0,1fr) auto;gap:12px;align-items:center;padding:10px 16px 10px 0;border-top:1px solid var(--line)}
.al .bar{align-self:stretch;border-radius:0 3px 3px 0}
.al.over .bar{background:var(--danger)} .al.soon .bar{background:var(--warn)} .al.up .bar{background:var(--line)} .al.done .bar{background:var(--ok)}
.al .dt{font-family:var(--f-mono);font-size:13px;display:flex;flex-direction:column;line-height:1.3}
.al .dt small{color:var(--muted);font-family:var(--f-body)}
.al .what{min-width:0}
.al .what b{font-weight:600}
.al .what div{color:var(--muted);font-size:12.5px;overflow-wrap:anywhere}
.chip{display:inline-flex;align-items:center;gap:4px;padding:2px 8px;border-radius:99px;font-size:12px;font-weight:600;white-space:nowrap;background:var(--surface2);color:var(--muted)}
.chip.over{background:var(--danger-soft);color:var(--danger)}
.chip.soon{background:var(--warn-soft);color:var(--warn)}
.chip.done{background:var(--ok-soft);color:var(--ok)}
.chip.info{background:var(--info-soft);color:var(--info)}
.chip.acc{background:var(--accent-soft);color:var(--accent)}
.form{font-family:var(--f-mono);font-size:12px;color:var(--accent);background:var(--accent-soft);padding:1px 6px;border-radius:4px;white-space:nowrap}
.tbl{overflow-x:auto}
table{border-collapse:collapse;width:100%;font-size:13.5px}
th{font-size:11.5px;text-transform:uppercase;letter-spacing:.05em;color:var(--muted);text-align:left;font-weight:600;padding:8px 12px;border-bottom:1px solid var(--line);white-space:nowrap;background:var(--surface2)}
td{padding:9px 12px;border-bottom:1px solid var(--line);vertical-align:middle}
tr:last-child td{border-bottom:0}
td.num,th.num{text-align:right;font-family:var(--f-mono);font-variant-numeric:tabular-nums}
.z{color:var(--muted)}
.empty{padding:28px 16px;text-align:center;color:var(--muted);display:flex;flex-direction:column;gap:10px;align-items:center}
.filters{display:flex;flex-wrap:wrap;gap:8px}
.filters select,.filters input{border:1px solid var(--line);background:var(--surface);border-radius:8px;padding:6px 10px;min-width:0;max-width:100%}
.month{font-family:var(--f-display);font-size:16px;padding:14px 16px 6px;display:flex;gap:10px;align-items:baseline}
.month small{font-family:var(--f-body);color:var(--muted);font-size:12.5px}
.ck{width:20px;height:20px;border-radius:6px;border:1.5px solid var(--line);background:var(--surface);cursor:pointer;display:grid;place-items:center;padding:0;flex:none}
.ck:hover{border-color:var(--ok)}
.ck.on{background:var(--ok);border-color:var(--ok);color:var(--surface)}
.ck svg{width:12px;height:12px}
.cal-row{display:grid;grid-template-columns:28px 104px 108px minmax(0,1fr) auto;gap:12px;align-items:center;padding:9px 16px;border-top:1px solid var(--line)}
.cal-row.done .what b{text-decoration:line-through;text-decoration-color:var(--muted)}
.cal-row .what{min-width:0}
.cal-row .what b{font-weight:600}
.cal-row .what div{font-size:12.5px;color:var(--muted);overflow-wrap:anywhere}
.board{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:16px;align-items:start}
.col{background:var(--surface2);border:1px solid var(--line);border-radius:12px;padding:10px;display:flex;flex-direction:column;gap:8px;min-width:0}
.col>h3{margin:2px 4px 4px;font-size:13px;display:flex;justify-content:space-between;color:var(--muted);text-transform:uppercase;letter-spacing:.05em}
.card{background:var(--surface);border:1px solid var(--line);border-radius:10px;padding:10px 12px;display:flex;flex-direction:column;gap:6px;min-width:0}
.card.late{border-left:3px solid var(--danger)}
.card b{font-weight:600;overflow-wrap:anywhere}
.card .meta{display:flex;flex-wrap:wrap;gap:6px;align-items:center;font-size:12.5px;color:var(--muted)}
.card .acts{display:flex;gap:6px;flex-wrap:wrap}
.pri-cao{color:var(--danger);font-weight:600}
.overlay{position:fixed;inset:0;background:rgba(10,20,26,.45);display:grid;place-items:center;padding:16px;z-index:50}
.dlg{background:var(--surface);border-radius:14px;width:min(560px,100%);max-height:calc(100vh - 32px);overflow:auto;box-shadow:0 20px 60px rgba(0,0,0,.25);border:1px solid var(--line)}
.dlg header{padding:16px 20px 4px;font-family:var(--f-display);font-size:19px}
.dlg .body{padding:8px 20px 4px;display:grid;grid-template-columns:1fr 1fr;gap:12px}
.dlg .body .full{grid-column:1/-1}
.dlg footer{padding:14px 20px 18px;display:flex;justify-content:space-between;gap:8px;flex-wrap:wrap}
.fld{display:flex;flex-direction:column;gap:4px;min-width:0}
.fld label{font-size:12px;color:var(--muted);font-weight:500}
.fld input,.fld select,.fld textarea{border:1px solid var(--line);background:var(--surface2);border-radius:8px;padding:7px 10px;width:100%}
.fld textarea{min-height:80px;resize:vertical}
.fld .hint{font-size:11.5px;color:var(--muted)}
.chk{display:flex;gap:8px;align-items:center}
.toast{position:fixed;left:50%;bottom:calc(20px + env(safe-area-inset-bottom,0px));transform:translateX(-50%);background:var(--fg);color:var(--bg);padding:9px 16px;border-radius:10px;font-size:13px;z-index:60;max-width:calc(100% - 32px)}
.note{background:var(--info-soft);color:var(--fg);border-radius:10px;padding:10px 14px;font-size:13px}
.note b{color:var(--info)}
.legal{font-size:12.5px;color:var(--muted);line-height:1.6;padding:0 16px 14px}
.legal li{margin-bottom:2px}
.sample{font-size:10.5px;text-transform:uppercase;letter-spacing:.06em;padding:1px 6px;border-radius:4px;background:var(--warn-soft);color:var(--warn);font-weight:600;margin-left:6px;vertical-align:1px}
.load{padding:40px;text-align:center;color:var(--muted)}
.bell{position:fixed;right:16px;bottom:calc(16px + env(safe-area-inset-bottom,0px));z-index:40;display:flex;align-items:center;gap:8px;border:0;border-radius:99px;padding:10px 16px 10px 12px;cursor:pointer;font-weight:600;box-shadow:0 6px 24px rgba(0,0,0,.18);background:var(--danger);color:var(--surface)}
.bell.w{background:var(--warn)}
.bell svg{width:18px;height:18px}
@media (prefers-reduced-motion:no-preference){.bell.ring svg{animation:ring 1.2s ease 2}@keyframes ring{0%,100%{transform:rotate(0)}20%{transform:rotate(16deg)}40%{transform:rotate(-14deg)}60%{transform:rotate(8deg)}80%{transform:rotate(-4deg)}}}
.dlg.wide{width:min(720px,100%)}
.dlg .body.one{grid-template-columns:1fr;gap:0;padding:0 0 4px}
.pop-sec{font-size:12px;text-transform:uppercase;letter-spacing:.06em;color:var(--muted);font-weight:600;padding:12px 20px 6px}
.pl-row{display:grid;grid-template-columns:30px 92px minmax(0,1fr) 150px auto;gap:12px;align-items:center;padding:9px 16px;border-top:1px solid var(--line)}
.pl-no{font-family:var(--f-mono);font-size:12px;color:var(--muted);text-align:right}
.lv{font-size:11.5px;font-weight:700;padding:2px 8px;border-radius:6px;text-align:center;white-space:nowrap}
.lv0{background:var(--danger);color:var(--surface)}.lv1{background:var(--danger-soft);color:var(--danger)}.lv2{background:var(--warn-soft);color:var(--warn)}.lv3{background:var(--info-soft);color:var(--info)}.lv4{background:var(--surface2);color:var(--muted)}
.pl-row .what{min-width:0}.pl-row .what b{font-weight:600;overflow-wrap:anywhere}.pl-row .what div{font-size:12.5px;color:var(--muted);overflow-wrap:anywhere}
.pl-row select{border:1px solid var(--line);background:var(--surface2);border-radius:6px;padding:4px 6px;width:100%;font-size:12.5px}
.people{display:grid;grid-template-columns:repeat(auto-fill,minmax(230px,1fr));gap:12px;padding:0 16px 16px}
.person{border:1px solid var(--line);border-radius:10px;padding:12px 14px;display:flex;flex-direction:column;gap:8px;background:var(--surface2)}
.person b{font-size:15px}
.person .k{display:flex;justify-content:space-between;font-size:12.5px;color:var(--muted)}
.person .k span:last-child{font-family:var(--f-mono);color:var(--fg)}
.load-bar{height:8px;border-radius:99px;background:var(--line);overflow:hidden}
.load-bar i{display:block;height:100%;background:var(--ok);border-radius:99px}
.load-bar i.w{background:var(--warn)}.load-bar i.o{background:var(--danger)}
@media (max-width:860px){.pl-row{grid-template-columns:30px minmax(0,1fr) auto;row-gap:6px}.pl-row .lvc{grid-column:2;grid-row:1}.pl-row .what{grid-column:2/-1}.pl-row .asg{grid-column:2}.pl-row .acts{grid-column:3;grid-row:1}.bell span.t{display:none}}
@media (max-width:1000px){.grid2{grid-template-columns:minmax(0,1fr)}.board{grid-template-columns:minmax(0,1fr)}}
@media (max-width:860px){
  .app{grid-template-columns:minmax(0,1fr)}
  .rail{position:sticky;top:env(safe-area-inset-top,0px);height:auto;z-index:10;flex-direction:row;align-items:center;padding:10px 16px;gap:12px;border-right:0;border-bottom:1px solid var(--line);overflow-x:auto}
  .brand span,.rail .foot{display:none}
  .brand b{font-size:17px;white-space:nowrap}
  .nav{flex-direction:row}
  .nav button{white-space:nowrap;padding:7px 10px}
  main{padding-inline:16px}
  .strip{grid-template-columns:repeat(2,minmax(0,1fr))}
  .strip>div:nth-child(3){border-left:0}
  .strip>div:nth-child(n+3){border-top:1px solid var(--line)}
  .cal-row{grid-template-columns:28px minmax(0,1fr) auto;row-gap:4px}
  .cal-row .dtc{grid-column:2}
  .cal-row .cd{grid-column:3;grid-row:1}
  .cal-row .what{grid-column:2/-1}
  .cal-row .asg{grid-column:2/-1}
  .al{grid-template-columns:4px 80px minmax(0,1fr)}
  .al .cd{grid-column:3}
  .dlg .body{grid-template-columns:1fr}
}
@media (prefers-reduced-motion:no-preference){.btn,.nav button,.ck{transition:background .15s,border-color .15s,color .15s}}
</style>

<div class="app">
  <aside class="rail">
    <div class="brand"><b>Sổ Hạn Thuế</b><span>Theo dõi hạn nộp &amp; công việc</span></div>
    <nav class="nav" id="nav"></nav>
    <div class="foot"><div id="conn"><span class="dot"></span>Đang kết nối…</div><div id="todayLbl" class="mono"></div></div>
  </aside>
  <main id="main"><div class="load">Đang tải dữ liệu…</div></main>
</div>
<div id="modal"></div>
<div id="toast" class="toast" hidden></div>
<button id="bell" class="bell" data-act="popup" hidden aria-label="Xem nhắc hạn"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M18 8a6 6 0 0 0-12 0c0 7-3 9-3 9h18s-3-2-3-9"/><path d="M13.7 21a2 2 0 0 1-3.4 0"/></svg><span id="bellTxt"></span></button>

<script>
(function(){
"use strict";
const $=(s,r=document)=>r.querySelector(s);
const esc=s=>String(s??"").replace(/[&<>"']/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"}[c]));
const pad=n=>String(n).padStart(2,"0");
const D=(y,m,d)=>new Date(y,m-1,d);
const iso=d=>d.getFullYear()+"-"+pad(d.getMonth()+1)+"-"+pad(d.getDate());
const P=s=>{if(!s)return null;const a=String(s).split("-").map(Number);return new Date(a[0],(a[1]||1)-1,a[2]||1)};
const lastDay=(y,m)=>new Date(y,m,0);
const addDays=(d,n)=>{const x=new Date(d);x.setDate(x.getDate()+n);return x};
const addMonths=(d,n)=>{const y=d.getFullYear(),m=d.getMonth()+n;const ld=new Date(y,m+1,0).getDate();return new Date(y,m,Math.min(d.getDate(),ld))};
const today=()=>{const t=new Date();return new Date(t.getFullYear(),t.getMonth(),t.getDate())};
const diff=(a,b)=>Math.round((a-b)/864e5);
const WD=["CN","T2","T3","T4","T5","T6","T7"];
const fmt=d=>pad(d.getDate())+"/"+pad(d.getMonth()+1)+"/"+d.getFullYear();
const fmtS=d=>pad(d.getDate())+"/"+pad(d.getMonth()+1);
const uid=p=>p+"-"+Date.now().toString(36)+Math.random().toString(36).slice(2,6);
const clone=o=>JSON.parse(JSON.stringify(o||{}));
const CHECK='<svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.2"><path d="M2 6.5l2.5 2.5L10 3.5"/></svg>';

const DEFAULT_SETTINGS={warnDays:7,horizon:100,leadDays:5,fileHours:1,capacity:40,planDays:21,staff:[],holidays:["2026-09-01","2026-09-02","2027-01-01","2027-04-30","2027-05-01","2027-09-01","2027-09-02"]};
const S={companies:{},tts:{},tasks:{},done:{},settings:clone(DEFAULT_SETTINGS)};
const loaded={companies:false,tts:false,tasks:false,done:false,settings:false};
let MODE="loading",DB=null,VIEW="dash";
const F={cal:{cid:"",st:"open",code:""},task:{cid:"",who:"",q:""},tts:{cid:""},plan:{who:""}};
let popupChecked=false;
const LS_KEY="so-han-thue-v1";

/* ---------- storage ---------- */
function loadLocal(){try{const raw=localStorage.getItem(LS_KEY);if(raw){const o=JSON.parse(raw);["companies","tts","tasks","done"].forEach(k=>S[k]=o[k]||{});S.settings=Object.assign(clone(DEFAULT_SETTINGS),o.settings||{});}}catch(e){}Object.keys(loaded).forEach(k=>loaded[k]=true)}
function saveLocal(){try{localStorage.setItem(LS_KEY,JSON.stringify({companies:S.companies,tts:S.tts,tasks:S.tasks,done:S.done,settings:S.settings}))}catch(e){toast("Không lưu được vào trình duyệt này.")}}
async function put(col,id,data){S[col]=Object.assign({},S[col],{[id]:data});render();
  if(MODE==="db"){try{await DB.collection(col).doc(id).set(data)}catch(e){toast(errMsg(e))}}else saveLocal()}
async function del(col,id){const o=Object.assign({},S[col]);delete o[id];S[col]=o;render();
  if(MODE==="db"){try{await DB.collection(col).doc(id).delete()}catch(e){toast(errMsg(e))}}else saveLocal()}
async function putSettings(data){S.settings=Object.assign(clone(DEFAULT_SETTINGS),data);render();
  if(MODE==="db"){try{await DB.doc("settings/main").set(data)}catch(e){toast(errMsg(e))}}else saveLocal()}
function errMsg(e){const c=e&&e.code;if(c==="invalid_argument")return "Bạn chỉ có quyền xem, không sửa được dữ liệu.";if(c==="quota_exceeded")return "Kho dữ liệu đã đầy. Hãy xóa bớt bản ghi cũ.";return "Lưu chưa thành công, thử lại sau ít phút."}
let rq=0;function scheduleRender(){if(rq)return;rq=requestAnimationFrame(()=>{rq=0;render()})}

async function init(){
  render();
  let db=null;
  try{db=(window.claude&&typeof window.claude.use==="function")?await window.claude.use("db"):null}catch(e){db=null}
  if(db){DB=db;MODE="db";
    ["companies","tts","tasks","done"].forEach(col=>{
      DB.collection(col).limit(1000).onSnapshot(snap=>{const o={};snap.docs.forEach(d=>{o[d.id]=d.data()});S[col]=o;loaded[col]=true;scheduleRender()},()=>{MODE="local";loadLocal();scheduleRender()});
    });
    DB.doc("settings/main").onSnapshot(d=>{S.settings=Object.assign(clone(DEFAULT_SETTINGS),d.exists?d.data():{});loaded.settings=true;scheduleRender()},()=>{});
  }else{MODE="local";loadLocal();render()}
}

/* ---------- deadline engine ---------- */
function workday(d){const hs=new Set(S.settings.holidays||[]);let x=new Date(d),sh=false;while(x.getDay()===0||x.getDay()===6||hs.has(iso(x))){x=addDays(x,1);sh=true}return{d:x,sh}}
let GEN=null;
function gen(){
  const out=[],t0=today(),hEnd=addDays(t0,+S.settings.horizon||100);
  const comp=S.companies;
  for(const cid in comp){const c=comp[cid];if(!c||c.active===false)continue;
    const from=P(c.trackFrom)||D(t0.getFullYear(),t0.getMonth()+1,1);
    const push=(code,label,form,period,plabel,raw,extra)=>{const w=workday(raw);if(w.d<from||w.d>hEnd)return;
      const key=cid+"."+code+"."+period;out.push(Object.assign({key,cid,code,label,form,period,plabel,due:w.d,raw,sh:w.sh,who:c.owner||"",done:S.done[key]||null},extra||{}))};
    for(let y=from.getFullYear()-1;y<=hEnd.getFullYear();y++){
      for(let m=1;m<=12;m++){const pk=y+"-"+pad(m),pl="T"+pad(m)+"/"+y;
        if(c.gtgt==="M")push("GTGT","Thuế GTGT","01/GTGT",pk,pl,D(y,m+1,20));
        if(c.tncn==="M")push("TNCN","Thuế TNCN khấu trừ","05/KK-TNCN",pk,pl,D(y,m+1,20));}
      for(let q=1;q<=4;q++){const pk=y+"-Q"+q,pl="Q"+q+"/"+y,due=q===4?lastDay(y+1,1):lastDay(y,q*3+1);
        if(c.gtgt==="Q")push("GTGT","Thuế GTGT","01/GTGT",pk,pl,due);
        if(c.tncn==="Q")push("TNCN","Thuế TNCN khấu trừ","05/KK-TNCN",pk,pl,due);
        if(c.tndn)push("TNDNTAM","Tạm nộp thuế TNDN","Nộp tiền",pk,pl,due);}
      if(c.qt){const pl="Năm "+y,due=lastDay(y+1,3);
        push("QTTNDN","Quyết toán thuế TNDN","03/TNDN",""+y,pl,due);
        push("QTTNCN","Quyết toán thuế TNCN","05/QTT-TNCN",""+y,pl,due);
        push("BCTC","Báo cáo tài chính năm","BCTC",""+y,pl,due);}
    }
  }
  for(const tid in S.tts){const k=S.tts[tid],c=comp[k.cid];if(!c||c.active===false||!k.start)continue;
    const from=P(c.trackFrom)||D(t0.getFullYear(),t0.getMonth()+1,1);
    const st=P(k.start),en=P(k.end)||addMonths(st,120),code="TTS-"+tid,lbl="Cho thuê tài sản · "+(k.lessor||"");
    const push=(period,plabel,raw)=>{const w=workday(raw);if(w.d<from||w.d>hEnd)return;const key=k.cid+"."+code+"."+period;
      out.push({key,cid:k.cid,code,label:lbl,form:"01/TTS",period,plabel,due:w.d,raw,sh:w.sh,who:c.owner||"",done:S.done[key]||null,tts:tid})};
    if(k.mode==="KY"){const n=Math.max(1,+k.pay||1);for(let i=0;i<600;i++){const s=addMonths(st,n*i);if(s>en)break;const e=addDays(addMonths(st,n*(i+1)),-1);
        push("K"+(i+1),"Kỳ "+(i+1)+": "+fmtS(s)+"–"+fmt(e>en?en:e),addDays(s,9))}}
    else if(k.mode==="M"){for(let x=D(st.getFullYear(),st.getMonth()+1,1);x<=en;x=addMonths(x,1)){const y=x.getFullYear(),m=x.getMonth()+1;push(y+"-"+pad(m),"T"+pad(m)+"/"+y,D(y,m+1,20))}}
    else if(k.mode==="Q"){let q0=Math.floor(st.getMonth()/3);for(let x=D(st.getFullYear(),q0*3+1,1);x<=en;x=addMonths(x,3)){const y=x.getFullYear(),q=Math.floor(x.getMonth()/3)+1;push(y+"-Q"+q,"Q"+q+"/"+y,q===4?lastDay(y+1,1):lastDay(y,q*3+1))}}
    else if(k.mode==="Y"){for(let y=st.getFullYear();y<=en.getFullYear();y++)push(""+y,"Năm "+y,lastDay(y+1,1))}
  }
  out.sort((a,b)=>a.due-b.due||(a.cid>b.cid?1:-1));
  return out;
}
function stOf(o){if(o.done)return"done";const n=diff(o.due,today());if(n<0)return"over";if(n<=(+S.settings.warnDays||7))return"soon";return"up"}
function cd(o){const s=stOf(o);if(s==="done")return'<span class="chip done">Đã nộp '+(o.done.date?fmtS(P(o.done.date)):"")+'</span>';const n=diff(o.due,today());
  if(n<0)return'<span class="chip over">Trễ '+(-n)+' ngày</span>';if(n===0)return'<span class="chip over">Hạn hôm nay</span>';return'<span class="chip '+(s==="soon"?"soon":"")+'">Còn '+n+' ngày</span>'}
function taskLate(t){return t.status!=="done"&&t.due&&P(t.due)<today()}
function cname(id){const c=S.companies[id];return c?c.name:"(đã xóa)"}

/* ---------- views ---------- */
const NAV=[["dash","Tổng quan"],["plan","Kế hoạch & Phân bổ"],["cal","Lịch hạn nộp"],["task","Công việc"],["tts","Thuê tài sản 01/TTS"],["co","Công ty"],["set","Cài đặt"]];
function render(){
  const ready=Object.values(loaded).every(Boolean);
  GEN=ready?gen():[];
  const over=GEN.filter(o=>stOf(o)==="over").length,soon=GEN.filter(o=>stOf(o)==="soon").length;
  const lateT=Object.values(S.tasks).filter(taskLate).length;
  $("#nav").innerHTML=NAV.map(([k,l])=>{let b="";if(k==="cal"&&over)b='<span class="badge">'+over+'</span>';else if(k==="cal"&&soon)b='<span class="badge w">'+soon+'</span>';if(k==="task"&&lateT)b='<span class="badge">'+lateT+'</span>';
    return'<button data-nav="'+k+'"'+(VIEW===k?' aria-current="page"':"")+'><span>'+l+'</span>'+b+'</button>'}).join("");
  $("#conn").innerHTML=MODE==="db"?'<span class="dot on"></span>Đã lưu trực tuyến':MODE==="local"?'<span class="dot"></span>Lưu trên trình duyệt này':'<span class="dot"></span>Đang kết nối…';
  const t=today();$("#todayLbl").textContent=WD[t.getDay()]+", "+fmt(t);
  const main=$("#main");
  if(!ready){main.innerHTML='<div class="load">Đang tải dữ liệu…</div>';return}
  main.innerHTML=({dash:vDash,plan:vPlan,cal:vCal,task:vTask,tts:vTts,co:vCo,set:vSet}[VIEW]||vDash)();
  const urgentT=Object.values(S.tasks).filter(x=>x.status!=="done"&&x.due&&diff(P(x.due),today())<=1).length;
  const total=over+soon+urgentT;
  document.title=(total?"("+total+") ":"")+"Sổ Hạn Thuế";
  const bell=$("#bell");
  if(total){bell.hidden=false;bell.classList.toggle("w",!over&&!lateT);$("#bellTxt").innerHTML='<span class="mono">'+total+'</span> <span class="t">'+(over?"quá hạn / sắp hạn":"việc cần nhắc")+'</span>'}else bell.hidden=true;
  if(!popupChecked){popupChecked=true;
    let seen="";try{seen=localStorage.getItem("sht-popup")||""}catch(e){}
    if(total&&seen!==iso(today())){showPopup();bell.classList.add("ring")}
    osNotifyDaily(over,soon,urgentT);
  }
}

/* ---------- reminders ---------- */
function showPopup(){
  const t=today();const items=GEN.filter(o=>{const s=stOf(o);return s==="over"||s==="soon"}).slice(0,10);
  const plan=planItems().filter(i=>i.kind==="t"&&i.lvl<=2).slice(0,6);
  const body='<div class="pop-sec">Hôm nay '+WD[t.getDay()]+', '+fmt(t)+'</div>'
   +(items.length?'<div class="pop-sec">Hạn nộp hồ sơ</div><div class="alerts">'+items.map(alRow).join("")+'</div>':"")
   +(plan.length?'<div class="pop-sec">Công việc cần ưu tiên</div>'+plan.map(i=>'<div class="al '+(i.lvl<=1?"over":"soon")+'"><span class="bar"></span><div class="dt">'+(i.due?fmtS(i.due):"—")+'<small>'+(i.due?WD[i.due.getDay()]:"")+'</small></div><div class="what"><b>'+esc(i.title)+'</b><div>'+esc(i.sub)+(i.who?" · "+esc(i.who):"")+'</div></div><div class="cd"><span class="lv lv'+i.lvl+'">'+LV[i.lvl]+'</span></div></div>').join(""):"")
   +(!items.length&&!plan.length?'<div class="empty">Không có hạn nào cần nhắc hôm nay.</div>':"");
  openModal("Nhắc hạn & việc cần làm",body,'<button class="btn" data-act="pop-mute">Không nhắc lại hôm nay</button><div class="row"><button class="btn" data-act="close">Đóng</button><button class="btn pri" data-act="pop-plan">Mở kế hoạch hôm nay</button></div>');
  const d=$("#modal .dlg");if(d){d.classList.add("wide");$("#modal .body").classList.add("one")}
}
function osNotifyDaily(over,soon,urgentT){
  try{if(!("Notification" in window)||Notification.permission!=="granted")return;
    const k="sht-os-"+iso(today());if(localStorage.getItem(k))return;
    if(!(over+soon+urgentT))return;
    new Notification("Sổ Hạn Thuế – nhắc hạn",{body:(over?over+" hồ sơ quá hạn. ":"")+(soon?soon+" hồ sơ đến hạn trong "+S.settings.warnDays+" ngày. ":"")+(urgentT?urgentT+" việc đến hạn trong 1 ngày.":""),tag:"sht-daily"});
    localStorage.setItem(k,"1");
  }catch(e){}
}
async function enableOs(){
  if(!("Notification" in window)){toast("Trình duyệt này không hỗ trợ thông báo.");return}
  let p="denied";try{p=await Notification.requestPermission()}catch(e){}
  if(p==="granted"){try{localStorage.removeItem("sht-os-"+iso(today()))}catch(e){}osNotifyDaily(GEN.filter(o=>stOf(o)==="over").length,GEN.filter(o=>stOf(o)==="soon").length,0);toast("Đã bật thông báo trên máy tính.")}
  else toast("Trang trực tuyến không được phép hiện thông báo hệ thống. Hãy mở bản file HTML trên máy để dùng tính năng này.")
}

/* ---------- planning ---------- */
const LV=["Quá hạn","Khẩn","Cao","Trung bình","Thấp"];
function lvlOf(n,pri){if(n<0)return 0;if(n<=2)return 1;if(pri==="cao"&&n<=7)return 1;if(n<=7)return 2;if(pri==="cao")return 2;if(n<=14)return 3;return pri==="thap"?4:3}
function planItems(){
  const t=today(),s=S.settings,lim=addDays(t,+s.planDays||21),lead=+s.leadDays||5,fh=+s.fileHours||1;const out=[];
  (GEN||[]).forEach(o=>{if(o.done||o.due>lim)return;const n=diff(o.due,t);let st=addDays(o.due,-lead);if(st<t)st=t;
    out.push({kind:"f",id:o.key,title:o.form+" · "+o.label,sub:cname(o.cid)+" · kỳ "+o.plabel,who:o.who,due:o.due,start:st,n,hours:fh,cid:o.cid,lvl:lvlOf(n,"tb")})});
  for(const id in S.tasks){const x=S.tasks[id];if(x.status==="done")continue;const due=x.due?P(x.due):null;if(due&&due>lim&&x.pri!=="cao")continue;
    const n=due?diff(due,t):99,h=+x.hours||1;let st=due?addDays(due,-Math.max(1,Math.ceil(h/6))):t;if(st<t)st=t;
    out.push({kind:"t",id,title:x.title,sub:cname(x.cid)+(x.status==="doing"?" · đang làm":""),who:x.who||"",due,start:st,n,hours:h,cid:x.cid,lvl:lvlOf(n,x.pri||"tb"),pri:x.pri})}
  out.sort((a,b)=>a.lvl-b.lvl||a.n-b.n||(a.kind===b.kind?0:a.kind==="f"?-1:1));
  return out;
}
function weekEnd(d,k){const x=new Date(d);const dow=(x.getDay()+6)%7;return addDays(x,6-dow+7*(k||0))}
function vPlan(){
  if(!Object.keys(S.companies).length)return header("Kế hoạch & Phân bổ","")+noCompanies();
  const t=today(),s=S.settings,who=F.plan.who;const all=planItems();const list=all.filter(i=>!who||(i.who||"(chưa giao)")===who);
  const we=weekEnd(t,0),we2=weekEnd(t,1);
  const B=[["Làm ngay hôm nay",i=>i.lvl<=1||i.start<=t],["Trong tuần này",i=>i.start<=we],["Tuần sau",i=>i.start<=we2],["Sau đó",()=>true]];
  const used=new Set();const groups=B.map(([n,f])=>{const it=list.filter(i=>!used.has(i)&&f(i));it.forEach(i=>used.add(i));return{n,it}});
  const names=[...new Set((s.staff||[]).concat(Object.values(S.companies).map(c=>c.owner),Object.values(S.tasks).map(x=>x.who)).filter(Boolean))];
  const whoSel=(i)=>'<select data-act="assign" data-kind="'+i.kind+'" data-id="'+esc(i.kind==="f"?i.cid:i.id)+'" aria-label="Người phụ trách"><option value="">Chưa giao</option>'+names.map(n=>'<option'+(n===i.who?" selected":"")+'>'+esc(n)+'</option>').join("")+'</select>';
  let no=0;
  const rows=groups.filter(g=>g.it.length).map(g=>'<div class="month">'+g.n+' <small>'+g.it.length+' việc · khoảng '+g.it.reduce((a,i)=>a+i.hours,0)+' giờ</small></div>'+g.it.map(i=>{no++;
    const dl=i.due?(i.n<0?'<span class="chip over">Trễ '+(-i.n)+' ngày</span>':i.n===0?'<span class="chip over">Hạn hôm nay</span>':'<span class="mono">'+WD[i.due.getDay()]+' '+fmtS(i.due)+'</span>'):'<span class="z">Không hạn</span>';
    return'<div class="pl-row"><span class="pl-no">'+no+'</span><span class="lvc"><span class="lv lv'+i.lvl+'">'+LV[i.lvl]+'</span></span><div class="what"><b>'+(i.kind==="f"?'<span class="form">Hồ sơ</span> ':"")+esc(i.title)+'</b><div>'+esc(i.sub)+' · hạn '+dl+(i.start>t?' · nên bắt đầu '+fmtS(i.start):"")+' · '+i.hours+' giờ</div></div><div class="asg">'+whoSel(i)+'</div><div class="acts row">'
      +(i.kind==="f"?'<button class="btn sm" data-act="toggle" data-key="'+esc(i.id)+'">Đã nộp ✓</button>':'<button class="btn sm" data-act="mv" data-id="'+i.id+'" data-to="done">Xong ✓</button><button class="btn sm" data-act="task-edit" data-id="'+i.id+'">Sửa</button>')+'</div></div>'}).join("")).join("");
  // workload
  const load=new Map();const ensure=w=>{if(!load.has(w))load.set(w,{co:0,h:0,n:0,over:0,urg:0});return load.get(w)};
  names.forEach(ensure);
  Object.values(S.companies).forEach(c=>{if(c.active!==false)ensure(c.owner||"(chưa giao)").co++});
  all.forEach(i=>{const p=ensure(i.who||"(chưa giao)");if(i.start<=we){p.h+=i.hours;p.n++}if(i.lvl===0)p.over++;if(i.lvl<=1)p.urg++});
  const cap=+s.capacity||40;
  const people=[...load.entries()].map(([w,p])=>{const pct=Math.round(p.h/cap*100);return'<div class="person"><div class="row" style="justify-content:space-between"><b>'+esc(w)+'</b>'+(p.over?'<span class="chip over">'+p.over+' quá hạn</span>':p.urg?'<span class="chip soon">'+p.urg+' khẩn</span>':'<span class="chip done">Ổn</span>')+'</div>'
    +'<div class="k"><span>Công ty phụ trách</span><span>'+p.co+'</span></div><div class="k"><span>Việc trong tuần này</span><span>'+p.n+'</span></div><div class="k"><span>Khối lượng tuần / định mức</span><span>'+p.h+' / '+cap+' giờ</span></div>'
    +'<div class="load-bar" title="'+pct+'%"><i class="'+(pct>100?"o":pct>80?"w":"")+'" style="width:'+Math.min(100,pct)+'%"></i></div>'
    +(w!=="(chưa giao)"?'<button class="btn sm" data-act="plan-who" data-who="'+esc(w)+'">Xem kế hoạch của '+esc(w)+'</button>':'<button class="btn sm" data-act="plan-who" data-who="(chưa giao)">Xem việc chưa giao</button>')+'</div>'}).join("");
  const cos=Object.entries(S.companies).filter(([,c])=>c.active!==false).sort((a,b)=>a[1].name.localeCompare(b[1].name,"vi"));
  return header("Kế hoạch & Phân bổ","Thứ tự ưu tiên tự sắp xếp theo hạn nộp, mức ưu tiên và thời gian cần chuẩn bị",'<button class="btn" data-act="popup">Xem nhắc hạn</button><button class="btn pri" data-act="task-new">+ Thêm việc</button>')
  +'<section class="panel"><h2>Phân bổ khối lượng theo người</h2><div class="people">'+people+'</div></section>'
  +'<div class="filters"><select id="f-plan-who" aria-label="Lọc theo người"><option value="">Kế hoạch của tất cả mọi người</option>'+names.concat(["(chưa giao)"]).map(n=>'<option'+(who===n?" selected":"")+'>'+esc(n)+'</option>').join("")+'</select></div>'
  +'<section class="panel"><h2>Thứ tự công việc cần làm<span class="z" style="text-transform:none;letter-spacing:0;font-weight:400">'+list.length+' việc trong '+(+s.planDays||21)+' ngày tới</span></h2>'+(rows||'<div class="empty">Không có việc nào trong khoảng kế hoạch.</div>')+'</section>'
  +'<section class="panel"><h2>Giao công ty cho người phụ trách</h2><div class="tbl"><table><thead><tr><th>Công ty</th><th>Người phụ trách</th><th class="num">Hồ sơ chưa nộp</th><th class="num">Việc mở</th></tr></thead><tbody>'
  +cos.map(([id,c])=>'<tr><td><b>'+esc(c.name)+'</b></td><td style="min-width:150px"><select data-act="assign" data-kind="c" data-id="'+id+'" style="border:1px solid var(--line);background:var(--surface2);border-radius:6px;padding:4px 6px;width:100%"><option value="">Chưa giao</option>'+names.map(n=>'<option'+(n===c.owner?" selected":"")+'>'+esc(n)+'</option>').join("")+'</select></td><td class="num">'+GEN.filter(o=>o.cid===id&&!o.done).length+'</td><td class="num">'+Object.values(S.tasks).filter(x=>x.cid===id&&x.status!=="done").length+'</td></tr>').join("")
  +'</tbody></table></div></section>'
  +'<section class="panel"><h2>Cách xếp thứ tự ưu tiên</h2><ul class="legal"><li><b>Quá hạn</b> luôn đứng đầu, tiếp theo là <b>Khẩn</b> (còn ≤ 2 ngày, hoặc ưu tiên cao còn ≤ 7 ngày), <b>Cao</b> (còn ≤ 7 ngày), <b>Trung bình</b> (≤ 14 ngày), <b>Thấp</b>.</li><li>Cùng mức thì việc có hạn sớm hơn làm trước; cùng hạn thì hồ sơ thuế đứng trước việc nội bộ.</li><li>Hồ sơ thuế nên bắt đầu chuẩn bị trước hạn '+(+s.leadDays||5)+' ngày, ước tính '+(+s.fileHours||1)+' giờ mỗi hồ sơ (chỉnh trong Cài đặt).</li><li>Thanh khối lượng so số giờ việc trong tuần với định mức '+cap+' giờ/người: vàng khi trên 80%, đỏ khi quá tải.</li></ul></section>';
}
function header(t,sub,acts){return'<div class="head"><div><h1>'+t+'</h1>'+(sub?'<p>'+sub+'</p>':"")+'</div><div class="row">'+(acts||"")+'</div></div>'}
function noCompanies(){return'<div class="panel"><div class="empty"><b style="color:var(--fg)">Chưa có công ty nào</b><span>Thêm công ty đầu tiên và chọn kỳ khai (tháng hoặc quý). Hạn nộp sẽ tự sinh và cảnh báo.</span><div class="row"><button class="btn pri" data-act="co-new">+ Thêm công ty</button><button class="btn" data-act="seed">Nạp dữ liệu mẫu</button></div></div></div>'}
function alRow(o){const s=stOf(o);return'<div class="al '+s+'"><span class="bar"></span><div class="dt">'+fmtS(o.due)+'<small>'+WD[o.due.getDay()]+'</small></div><div class="what"><b>'+esc(cname(o.cid))+'</b><div><span class="form">'+esc(o.form)+'</span> '+esc(o.label)+' · '+esc(o.plabel)+(o.who?' · '+esc(o.who):"")+'</div></div><div class="cd">'+cd(o)+'</div></div>'}

function vDash(){
  const cs=Object.entries(S.companies);
  if(!cs.length)return header("Tổng quan","")+noCompanies();
  const t=today(),openG=GEN.filter(o=>!o.done);
  const over=openG.filter(o=>stOf(o)==="over"),soon=openG.filter(o=>stOf(o)==="soon");
  const month=openG.filter(o=>o.due.getMonth()===t.getMonth()&&o.due.getFullYear()===t.getFullYear());
  const tasks=Object.values(S.tasks),openT=tasks.filter(x=>x.status!=="done"),lateT=openT.filter(taskLate);
  const alerts=over.concat(soon).slice(0,14);
  const next=openG.filter(o=>stOf(o)==="up").slice(0,6);
  const byCo=cs.filter(([,c])=>c.active!==false).map(([id,c])=>{const g=openG.filter(o=>o.cid===id);const nx=g[0];
    return{id,c,over:g.filter(o=>stOf(o)==="over").length,soon:g.filter(o=>stOf(o)==="soon").length,openT:openT.filter(x=>x.cid===id).length,lateT:lateT.filter(x=>x.cid===id).length,nx}}).sort((a,b)=>(b.over-a.over)||(b.lateT-a.lateT)||(b.soon-a.soon)||((a.nx?a.nx.due:9e15)-(b.nx?b.nx.due:9e15)));
  const staff=new Map();cs.forEach(([id,c])=>{if(c.active===false)return;const w=c.owner||"(chưa giao)";if(!staff.has(w))staff.set(w,{co:0,over:0,soon:0,openT:0,lateT:0});staff.get(w).co++});
  openG.forEach(o=>{const w=o.who||"(chưa giao)";if(!staff.has(w))staff.set(w,{co:0,over:0,soon:0,openT:0,lateT:0});const s=stOf(o);if(s==="over")staff.get(w).over++;if(s==="soon")staff.get(w).soon++});
  openT.forEach(x=>{const w=x.who||"(chưa giao)";if(!staff.has(w))staff.set(w,{co:0,over:0,soon:0,openT:0,lateT:0});staff.get(w).openT++;if(taskLate(x))staff.get(w).lateT++});
  const banner=over.length?'<div class="note" style="background:var(--danger-soft)"><b style="color:var(--danger)">Có '+over.length+' hồ sơ quá hạn chưa đánh dấu đã nộp.</b> Kiểm tra lại trên cổng thuế và đánh dấu trong Lịch hạn nộp, hoặc xử lý nộp bổ sung.</div>':
    soon.length?'<div class="note" style="background:var(--warn-soft)"><b style="color:var(--warn)">'+soon.length+' hồ sơ đến hạn trong '+S.settings.warnDays+' ngày tới.</b> Gần nhất: '+esc(cname(soon[0].cid))+' – '+esc(soon[0].form)+' '+esc(soon[0].plabel)+', hạn '+fmt(soon[0].due)+'.</div>':"";
  return header("Tổng quan","Hạn nộp và việc tồn của "+byCo.length+" đơn vị đang theo dõi",'<button class="btn" data-act="task-new">+ Giao việc</button><button class="btn pri" data-nav="cal">Mở lịch hạn nộp</button>')
  +banner
  +'<div class="strip"><div class="over"><span class="n mono">'+over.length+'</span><span class="l">Hồ sơ quá hạn</span></div><div class="soon"><span class="n mono">'+soon.length+'</span><span class="l">Đến hạn ≤ '+S.settings.warnDays+' ngày</span></div><div><span class="n mono">'+month.length+'</span><span class="l">Còn phải nộp tháng '+(t.getMonth()+1)+'</span></div><div><span class="n mono">'+openT.length+'</span><span class="l">Việc đang mở'+(lateT.length?' · <b style="color:var(--danger)">'+lateT.length+' trễ</b>':"")+'</span></div></div>'
  +'<div class="grid2"><section class="panel"><h2>Cần xử lý<button class="btn sm" data-nav="cal">Xem tất cả</button></h2><div class="alerts">'
  +(alerts.length?alerts.map(alRow).join(""):'<div class="empty">Không có hồ sơ quá hạn hay sắp đến hạn.</div>')
  +(next.length?'<div class="month"><small>Sắp tới</small></div>'+next.map(alRow).join(""):"")
  +'</div></section>'
  +'<section class="panel"><h2>Việc tồn theo đơn vị</h2><div class="tbl"><table><thead><tr><th>Công ty</th><th class="num">Quá hạn</th><th class="num">Sắp hạn</th><th class="num">Việc mở</th><th>Hạn gần nhất</th></tr></thead><tbody>'
  +byCo.map(r=>'<tr><td><b>'+esc(r.c.name)+'</b>'+(r.c.sample?'<span class="sample">Mẫu</span>':"")+'<div class="z" style="font-size:12px">'+esc(r.c.owner||"Chưa giao")+' · GTGT '+({M:"tháng",Q:"quý",none:"—"}[r.c.gtgt]||"—")+'</div></td><td class="num" style="'+(r.over?"color:var(--danger);font-weight:600":"")+'">'+r.over+'</td><td class="num" style="'+(r.soon?"color:var(--warn);font-weight:600":"")+'">'+r.soon+'</td><td class="num">'+r.openT+(r.lateT?' <span style="color:var(--danger)">('+r.lateT+' trễ)</span>':"")+'</td><td>'+(r.nx?'<span class="mono">'+fmtS(r.nx.due)+'</span> <span class="z">'+esc(r.nx.form)+'</span>':'<span class="z">—</span>')+'</td></tr>').join("")
  +'</tbody></table></div></section></div>'
  +'<section class="panel"><h2>Phân bổ theo người phụ trách</h2><div class="tbl"><table><thead><tr><th>Người phụ trách</th><th class="num">Số công ty</th><th class="num">Hồ sơ quá hạn</th><th class="num">Sắp đến hạn</th><th class="num">Việc mở</th><th class="num">Việc trễ</th></tr></thead><tbody>'
  +[...staff.entries()].map(([w,v])=>'<tr><td><b>'+esc(w)+'</b></td><td class="num">'+v.co+'</td><td class="num" style="'+(v.over?"color:var(--danger);font-weight:600":"")+'">'+v.over+'</td><td class="num">'+v.soon+'</td><td class="num">'+v.openT+'</td><td class="num" style="'+(v.lateT?"color:var(--danger);font-weight:600":"")+'">'+v.lateT+'</td></tr>').join("")
  +'</tbody></table></div></section>';
}

function coOptions(sel,all){return(all?'<option value="">Tất cả công ty</option>':"")+Object.entries(S.companies).sort((a,b)=>a[1].name.localeCompare(b[1].name,"vi")).map(([id,c])=>'<option value="'+id+'"'+(sel===id?" selected":"")+'>'+esc(c.name)+'</option>').join("")}
function vCal(){
  if(!Object.keys(S.companies).length)return header("Lịch hạn nộp","")+noCompanies();
  const f=F.cal;let list=GEN.filter(o=>(!f.cid||o.cid===f.cid)&&(!f.code||(f.code==="TTS"?o.form==="01/TTS":o.code===f.code)));
  if(f.st==="open")list=list.filter(o=>!o.done);else if(f.st)list=list.filter(o=>stOf(o)===f.st);
  const groups=[];list.forEach(o=>{const k=o.due.getFullYear()+"-"+pad(o.due.getMonth()+1);let g=groups[groups.length-1];if(!g||g.k!==k){g={k,y:o.due.getFullYear(),m:o.due.getMonth()+1,items:[]};groups.push(g)}g.items.push(o)});
  return header("Lịch hạn nộp","Tự sinh theo kỳ khai của từng công ty, hạn rơi vào thứ Bảy, Chủ nhật, ngày lễ được dời sang ngày làm việc kế tiếp")
  +'<div class="filters"><select id="f-cal-cid" aria-label="Công ty">'+coOptions(f.cid,true)+'</select>'
  +'<select id="f-cal-st" aria-label="Trạng thái">'+[["open","Chưa nộp"],["over","Quá hạn"],["soon","Sắp đến hạn"],["up","Chưa đến hạn"],["done","Đã nộp"],["","Tất cả"]].map(([v,l])=>'<option value="'+v+'"'+(f.st===v?" selected":"")+'>'+l+'</option>').join("")+'</select>'
  +'<select id="f-cal-code" aria-label="Loại hồ sơ">'+[["","Mọi loại hồ sơ"],["GTGT","01/GTGT"],["TNCN","05/KK-TNCN"],["TNDNTAM","Tạm nộp TNDN"],["TTS","01/TTS"],["QTTNDN","03/TNDN"],["QTTNCN","05/QTT-TNCN"],["BCTC","BCTC năm"]].map(([v,l])=>'<option value="'+v+'"'+(f.code===v?" selected":"")+'>'+l+'</option>').join("")+'</select></div>'
  +'<section class="panel">'+(groups.length?groups.map(g=>'<div class="month">Tháng '+g.m+'/'+g.y+' <small>'+g.items.length+' hồ sơ</small></div>'+g.items.map(o=>{const s=stOf(o);
    return'<div class="cal-row '+s+'"><button class="ck'+(o.done?" on":"")+'" data-act="toggle" data-key="'+esc(o.key)+'" aria-label="'+(o.done?"Bỏ đánh dấu đã nộp":"Đánh dấu đã nộp")+'">'+(o.done?CHECK:"")+'</button>'
    +'<div class="dtc mono">'+WD[o.due.getDay()]+' '+fmt(o.due)+(o.sh?'<div class="z" style="font-size:11px;font-family:var(--f-body)">dời từ '+fmtS(o.raw)+'</div>':"")+'</div>'
    +'<div class="cd">'+cd(o)+'</div><div class="what"><b>'+esc(cname(o.cid))+'</b><div><span class="form">'+esc(o.form)+'</span> '+esc(o.label)+' · kỳ '+esc(o.plabel)+'</div></div><div class="asg z">'+esc(o.who||"")+'</div></div>'}).join("")).join(""):'<div class="empty">Không có hồ sơ nào khớp bộ lọc.</div>')+'</section>'
  +'<section class="panel"><h2>Căn cứ thời hạn đang áp dụng</h2><ul class="legal"><li>Khai theo tháng: chậm nhất ngày 20 của tháng tiếp theo. Khai theo quý: ngày cuối cùng của tháng đầu quý tiếp theo (NĐ 252/2026/NĐ-CP, hiệu lực 01/7/2026).</li><li>Tạm nộp TNDN quý: ngày cuối cùng của tháng đầu quý sau.</li><li>Quyết toán TNDN, TNCN, BCTC năm: ngày cuối cùng của tháng thứ 3 kể từ khi kết thúc năm (năm tài chính theo năm dương lịch).</li><li>01/TTS theo kỳ thanh toán: ngày thứ 10 kể từ ngày bắt đầu kỳ thanh toán; khai theo năm: ngày cuối cùng tháng 01 năm sau.</li><li>Thời hạn nộp tiền thuế trùng hạn nộp tờ khai. Kiểm tra lại khi có văn bản mới.</li></ul></section>';
}

function vTask(){
  const f=F.task;const all=Object.entries(S.tasks).filter(([,t])=>(!f.cid||t.cid===f.cid)&&(!f.who||(t.who||"")===f.who)&&(!f.q||(t.title+" "+(t.note||"")).toLowerCase().includes(f.q.toLowerCase())));
  const who=[...new Set(Object.values(S.tasks).map(t=>t.who).concat(S.settings.staff||[]).filter(Boolean))];
  const order=t=>(t.status==="done"?1:0)*1e15+(t.due?P(t.due).getTime():9e14);
  const col=(st,title)=>{const items=all.filter(([,t])=>t.status===st).sort((a,b)=>st==="done"?((b[1].doneAt||"")>(a[1].doneAt||"")?1:-1):order(a[1])-order(b[1]));const shown=st==="done"?items.slice(0,15):items;
    return'<div class="col"><h3><span>'+title+'</span><span class="mono">'+items.length+'</span></h3>'+(shown.length?shown.map(([id,t])=>{const late=taskLate(t);const n=t.due?diff(P(t.due),today()):null;
      return'<div class="card'+(late?" late":"")+'"><b>'+esc(t.title)+'</b><div class="meta"><span class="chip acc">'+esc(cname(t.cid))+'</span>'+(t.who?'<span>'+esc(t.who)+'</span>':"")
      +(t.due?(st==="done"?'<span class="mono">hạn '+fmtS(P(t.due))+'</span>':late?'<span class="chip over">Trễ '+(-n)+' ngày</span>':'<span class="chip'+(n<=S.settings.warnDays?" soon":"")+'">'+(n===0?"Hôm nay":"Còn "+n+" ngày")+'</span>'):"")
      +(t.pri==="cao"?'<span class="pri-cao">Ưu tiên cao</span>':"")+'</div>'+(t.note?'<div class="z" style="font-size:12.5px;overflow-wrap:anywhere">'+esc(t.note)+'</div>':"")
      +'<div class="acts">'+(st!=="todo"?'<button class="btn sm" data-act="mv" data-id="'+id+'" data-to="'+(st==="done"?"doing":"todo")+'">← '+(st==="done"?"Mở lại":"Cần làm")+'</button>':"")
      +(st!=="done"?'<button class="btn sm" data-act="mv" data-id="'+id+'" data-to="'+(st==="todo"?"doing":"done")+'">'+(st==="todo"?"Bắt đầu →":"Xong ✓")+'</button>':"")
      +'<button class="btn sm" data-act="task-edit" data-id="'+id+'">Sửa</button></div></div>'}).join(""):'<div class="z" style="padding:8px 4px;font-size:12.5px">Không có việc.</div>')+'</div>'};
  return header("Công việc","Giao việc cho từng đơn vị, theo dõi việc tồn và việc trễ hạn",'<button class="btn pri" data-act="task-new">+ Thêm việc</button>')
  +'<div class="filters"><select id="f-task-cid" aria-label="Công ty">'+coOptions(f.cid,true)+'</select><select id="f-task-who" aria-label="Người phụ trách"><option value="">Mọi người phụ trách</option>'+who.map(w=>'<option'+(f.who===w?" selected":"")+'>'+esc(w)+'</option>').join("")+'</select><input id="f-task-q" type="search" placeholder="Tìm việc…" value="'+esc(f.q)+'"></div>'
  +'<div class="board">'+col("todo","Cần làm")+col("doing","Đang làm")+col("done","Hoàn thành")+'</div>';
}

function vTts(){
  const f=F.tts;const list=Object.entries(S.tts).filter(([,k])=>!f.cid||k.cid===f.cid);
  const ML={KY:"Theo kỳ thanh toán",M:"Theo tháng",Q:"Theo quý",Y:"Một lần theo năm"};
  return header("Thuê tài sản 01/TTS","Hợp đồng thuê tài sản của cá nhân mà công ty khai thay, nộp thay. Hạn khai sinh theo phương thức khai của từng hợp đồng.",'<button class="btn pri" data-act="tts-new">+ Thêm hợp đồng</button>')
  +'<div class="filters"><select id="f-tts-cid" aria-label="Công ty">'+coOptions(f.cid,true)+'</select></div>'
  +'<section class="panel">'+(list.length?'<div class="tbl"><table><thead><tr><th>Công ty / Bên cho thuê</th><th>Tài sản</th><th>Phương thức khai</th><th>Thời hạn thuê</th><th>Kỳ khai tới</th><th></th></tr></thead><tbody>'
  +list.map(([id,k])=>{const g=GEN.filter(o=>o.tts===id&&!o.done);const nx=g[0];const over=g.filter(o=>stOf(o)==="over").length;
    return'<tr><td><b>'+esc(cname(k.cid))+'</b><div class="z" style="font-size:12.5px">'+esc(k.lessor||"")+'</div></td><td>'+esc(k.asset||"")+'</td><td>'+ML[k.mode]+(k.mode==="KY"?' <span class="z">('+(k.pay||1)+' tháng/kỳ)</span>':"")+'</td><td class="mono" style="white-space:nowrap">'+(k.start?fmt(P(k.start)):"")+' – '+(k.end?fmt(P(k.end)):"…")+'</td><td>'+(nx?'<span class="mono">'+fmt(nx.due)+'</span> '+cd(nx)+'<div class="z" style="font-size:12px">'+esc(nx.plabel)+'</div>':'<span class="z">—</span>')+(over>1?'<div style="color:var(--danger);font-size:12px">'+over+' kỳ quá hạn</div>':"")+'</td><td><button class="btn sm" data-act="tts-edit" data-id="'+id+'">Sửa</button></td></tr>'}).join("")
  +'</tbody></table></div>':'<div class="empty">Chưa có hợp đồng thuê tài sản nào.<button class="btn pri" data-act="tts-new">+ Thêm hợp đồng</button></div>')+'</section>';
}

function vCo(){
  const cs=Object.entries(S.companies).sort((a,b)=>a[1].name.localeCompare(b[1].name,"vi"));
  const L={M:"Tháng",Q:"Quý",none:"—"};
  return header("Công ty","Kỳ khai thuế và người phụ trách của từng đơn vị",'<button class="btn pri" data-act="co-new">+ Thêm công ty</button>')
  +(cs.length?'<section class="panel"><div class="tbl"><table><thead><tr><th>Công ty</th><th>MST</th><th>GTGT</th><th>TNCN</th><th>Tạm nộp TNDN</th><th>Quyết toán năm</th><th>Phụ trách</th><th>Theo dõi từ</th><th></th></tr></thead><tbody>'
  +cs.map(([id,c])=>'<tr style="'+(c.active===false?"opacity:.55":"")+'"><td><b>'+esc(c.name)+'</b>'+(c.sample?'<span class="sample">Mẫu</span>':"")+(c.active===false?' <span class="chip">Ngừng theo dõi</span>':"")+'</td><td class="mono">'+esc(c.mst||"")+'</td><td>'+L[c.gtgt||"none"]+'</td><td>'+L[c.tncn||"none"]+'</td><td>'+(c.tndn?"Có":"—")+'</td><td>'+(c.qt?"Có":"—")+'</td><td>'+esc(c.owner||"")+'</td><td class="mono">'+(c.trackFrom?fmt(P(c.trackFrom)):"")+'</td><td><button class="btn sm" data-act="co-edit" data-id="'+id+'">Sửa</button></td></tr>').join("")
  +'</tbody></table></div></section>':noCompanies());
}

function vSet(){
  const s=S.settings;const hasSample=Object.values(S.companies).some(c=>c.sample);
  return header("Cài đặt","")
  +'<section class="panel"><h2>Cảnh báo</h2><div style="padding:0 16px 16px;display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:12px">'
  +'<div class="fld"><label for="s-warn">Cảnh báo trước hạn (ngày)</label><input id="s-warn" type="number" min="1" max="60" value="'+(+s.warnDays||7)+'"></div>'
  +'<div class="fld"><label for="s-hz">Hiển thị hạn nộp trước (ngày)</label><input id="s-hz" type="number" min="30" max="400" value="'+(+s.horizon||100)+'"></div>'
  +'<div class="fld"><label for="s-lead">Bắt đầu chuẩn bị hồ sơ trước hạn (ngày)</label><input id="s-lead" type="number" min="0" max="30" value="'+(+s.leadDays||5)+'"></div>'
  +'<div class="fld"><label for="s-fh">Thời gian ước tính mỗi hồ sơ (giờ)</label><input id="s-fh" type="number" min="0.5" step="0.5" value="'+(+s.fileHours||1)+'"></div>'
  +'<div class="fld"><label for="s-cap">Định mức mỗi người (giờ/tuần)</label><input id="s-cap" type="number" min="1" max="80" value="'+(+s.capacity||40)+'"></div>'
  +'<div class="fld"><label for="s-pd">Lập kế hoạch cho (ngày tới)</label><input id="s-pd" type="number" min="7" max="90" value="'+(+s.planDays||21)+'"></div>'
  +'<div class="fld full" style="grid-column:1/-1"><label for="s-staff">Danh sách người phụ trách (mỗi dòng một tên)</label><textarea id="s-staff">'+esc((s.staff||[]).join("\n"))+'</textarea></div>'
  +'<div class="fld full" style="grid-column:1/-1"><label for="s-hol">Ngày nghỉ lễ, Tết (mỗi dòng một ngày YYYY-MM-DD)</label><textarea id="s-hol" class="mono">'+esc((s.holidays||[]).join("\n"))+'</textarea><span class="hint">Hạn nộp rơi vào ngày nghỉ sẽ dời sang ngày làm việc kế tiếp. Bổ sung lịch nghỉ Tết Nguyên đán 2027 khi có thông báo chính thức.</span></div>'
  +'<div><button class="btn pri" data-act="save-set">Lưu cài đặt</button></div></div></section>'
  +'<section class="panel"><h2>Nhắc hạn</h2><div style="padding:0 16px 16px;display:flex;flex-direction:column;gap:10px"><span class="z">Mỗi ngày, lần đầu mở trang sẽ hiện cửa sổ nhắc hạn; chuông góc phải màn hình và tiêu đề tab trình duyệt luôn hiện số việc cần xử lý. Khi mở bản file HTML trên máy tính, có thể bật thêm thông báo của Windows/macOS.</span><div class="row"><button class="btn" data-act="popup">Xem cửa sổ nhắc hạn</button><button class="btn" data-act="os-on">Bật thông báo trên máy tính</button><button class="btn" data-act="pop-reset">Nhắc lại khi mở trang hôm nay</button></div></div></section>'
  +'<section class="panel" id="backup"><h2>Sao lưu &amp; chuyển dữ liệu</h2><div style="padding:0 16px 16px;display:flex;flex-direction:column;gap:12px">'
  +'<span class="z">Lưu toàn bộ công ty, hợp đồng 01/TTS, công việc, trạng thái đã nộp và cài đặt thành một file <span class="mono">.json</span>. Mang file này sang trình duyệt hoặc máy khác, mở Sổ Hạn Thuế ở đó rồi chọn "Khôi phục từ file".</span>'
  +'<div class="row"><button class="btn pri" data-act="file-save">Tải file sao lưu</button><button class="btn" data-act="file-pick">Khôi phục từ file…</button><input id="s-file" type="file" accept=".json,application/json" hidden>'+(hasSample?'<button class="btn danger" data-act="unseed">Xóa dữ liệu mẫu</button>':"")+'</div>'
  +(PENDING?'<div class="note"><b>File sao lưu ngày '+esc(PENDING.at?fmt(new Date(PENDING.at)):"không rõ")+':</b> '+cnt(PENDING.companies)+' công ty, '+cnt(PENDING.tts)+' hợp đồng 01/TTS, '+cnt(PENDING.tasks)+' công việc, '+cnt(PENDING.done)+' hồ sơ đã nộp.'
    +'<label class="chk" style="margin-top:8px"><input type="checkbox" id="s-replace"> Xóa dữ liệu đang có ở đây trước khi khôi phục (nếu không chọn: gộp, bản ghi trùng sẽ được ghi đè)</label>'
    +'<div class="row" style="margin-top:8px"><button class="btn pri" data-act="file-apply">Khôi phục</button><button class="btn" data-act="file-cancel">Hủy</button></div></div>':"")
  +'<details><summary class="z" style="cursor:pointer">Cách khác: sao chép/dán dạng văn bản</summary><div style="display:flex;flex-direction:column;gap:10px;margin-top:10px"><textarea id="s-json" class="mono" style="min-height:110px;border:1px solid var(--line);border-radius:8px;padding:8px;background:var(--surface2);width:100%" placeholder="Dán nội dung sao lưu vào đây để khôi phục"></textarea><div class="row"><button class="btn" data-act="export">Xuất ra ô văn bản</button><button class="btn" data-act="copy">Sao chép</button><button class="btn" data-act="import">Khôi phục từ nội dung đã dán</button></div></div></details>'
  +'</div></section>'
  +'<div class="note"><b>Nơi lưu dữ liệu:</b> '+(MODE==="db"?"dữ liệu lưu trực tuyến cùng trang này, mở trên máy khác vẫn thấy.":"dữ liệu đang lưu trong trình duyệt của máy này. Nên xuất sao lưu định kỳ.")+'</div>';
}

/* ---------- modals ---------- */
function openModal(title,body,foot){$("#modal").innerHTML='<div class="overlay" data-act="close-bg"><div class="dlg" role="dialog" aria-modal="true" aria-label="'+esc(title)+'"><header>'+esc(title)+'</header><div class="body">'+body+'</div><footer>'+foot+'</footer></div></div>';const f=$("#modal input,#modal select");if(f)f.focus()}
function closeModal(){$("#modal").innerHTML=""}
const fld=(id,label,input,full,hint)=>'<div class="fld'+(full?" full":"")+'"><label for="'+id+'">'+label+'</label>'+input+(hint?'<span class="hint">'+hint+'</span>':"")+'</div>';
const sel=(id,opts,v)=>'<select id="'+id+'">'+opts.map(([a,b])=>'<option value="'+a+'"'+(v===a?" selected":"")+'>'+b+'</option>').join("")+'</select>';
const staffList=()=>'<datalist id="dl-staff">'+(S.settings.staff||[]).map(n=>'<option value="'+esc(n)+'">').join("")+'</datalist>';
let EDIT=null;
function coForm(id){EDIT=id;const t=today();const c=id?S.companies[id]:{gtgt:"Q",tncn:"none",tndn:true,qt:true,active:true,trackFrom:iso(D(t.getFullYear(),t.getMonth()+1,1))};
  openModal(id?"Sửa công ty":"Thêm công ty",
    fld("m-name","Tên công ty",'<input id="m-name" value="'+esc(c.name||"")+'">',true)
    +fld("m-mst","Mã số thuế",'<input id="m-mst" class="mono" value="'+esc(c.mst||"")+'">')
    +fld("m-owner","Người phụ trách",'<input id="m-owner" list="dl-staff" value="'+esc(c.owner||"")+'">'+staffList())
    +fld("m-gtgt","Kỳ khai thuế GTGT",sel("m-gtgt",[["M","Theo tháng"],["Q","Theo quý"],["none","Không khai"]],c.gtgt||"Q"))
    +fld("m-tncn","Kỳ khai thuế TNCN khấu trừ",sel("m-tncn",[["M","Theo tháng"],["Q","Theo quý"],["none","Không phát sinh"]],c.tncn||"none"))
    +'<label class="chk full"><input type="checkbox" id="m-tndn"'+(c.tndn?" checked":"")+'> Tạm nộp thuế TNDN theo quý</label>'
    +'<label class="chk full"><input type="checkbox" id="m-qt"'+(c.qt?" checked":"")+'> Quyết toán TNDN, TNCN và BCTC năm</label>'
    +fld("m-from","Theo dõi hạn nộp từ ngày",'<input id="m-from" type="date" value="'+esc(c.trackFrom||"")+'">',false,"Hạn trước ngày này không hiện, tránh báo quá hạn cho kỳ cũ.")
    +'<label class="chk" style="align-self:end"><input type="checkbox" id="m-active"'+(c.active!==false?" checked":"")+'> Đang theo dõi</label>'
    +fld("m-note","Ghi chú",'<textarea id="m-note">'+esc(c.note||"")+'</textarea>',true),
    '<div>'+(id?'<button class="btn danger" data-act="co-del">Xóa công ty</button>':"")+'</div><div class="row"><button class="btn" data-act="close">Hủy</button><button class="btn pri" data-act="co-save">Lưu</button></div>')}
function taskForm(id,preset){EDIT=id;const t=id?S.tasks[id]:Object.assign({status:"todo",pri:"tb",cid:F.task.cid||Object.keys(S.companies)[0]||""},preset||{});
  if(!Object.keys(S.companies).length){toast("Hãy thêm công ty trước.");return}
  if(!id&&!t.who&&S.companies[t.cid])t.who=S.companies[t.cid].owner||"";
  openModal(id?"Sửa công việc":"Giao việc mới",
    fld("m-title","Nội dung công việc",'<input id="m-title" value="'+esc(t.title||"")+'" placeholder="Ví dụ: Đối chiếu công nợ quý 3">',true)
    +fld("m-cid","Công ty",'<select id="m-cid">'+coOptions(t.cid,false)+'</select>')
    +fld("m-who","Người phụ trách",'<input id="m-who" list="dl-staff" value="'+esc(t.who||"")+'">'+staffList())
    +fld("m-due","Hạn hoàn thành",'<input id="m-due" type="date" value="'+esc(t.due||"")+'">')
    +fld("m-pri","Mức ưu tiên",sel("m-pri",[["cao","Cao"],["tb","Bình thường"],["thap","Thấp"]],t.pri||"tb"))
    +fld("m-status","Trạng thái",sel("m-status",[["todo","Cần làm"],["doing","Đang làm"],["done","Hoàn thành"]],t.status||"todo"))
    +fld("m-hours","Thời gian ước tính (giờ)",'<input id="m-hours" type="number" min="0.5" step="0.5" value="'+(+t.hours||1)+'">',false,"Dùng để tính khối lượng trong tab Kế hoạch & Phân bổ.")
    +fld("m-note","Ghi chú",'<textarea id="m-note">'+esc(t.note||"")+'</textarea>',true),
    '<div>'+(id?'<button class="btn danger" data-act="task-del">Xóa việc</button>':"")+'</div><div class="row"><button class="btn" data-act="close">Hủy</button><button class="btn pri" data-act="task-save">Lưu</button></div>')}
function ttsForm(id){EDIT=id;const k=id?S.tts[id]:{mode:"KY",pay:3,cid:F.tts.cid||Object.keys(S.companies)[0]||""};
  if(!Object.keys(S.companies).length){toast("Hãy thêm công ty trước.");return}
  openModal(id?"Sửa hợp đồng thuê":"Thêm hợp đồng thuê tài sản",
    fld("m-cid","Công ty đi thuê (khai thay)",'<select id="m-cid">'+coOptions(k.cid,false)+'</select>',true)
    +fld("m-lessor","Bên cho thuê (cá nhân)",'<input id="m-lessor" value="'+esc(k.lessor||"")+'">')
    +fld("m-asset","Tài sản thuê",'<input id="m-asset" value="'+esc(k.asset||"")+'" placeholder="Nhà, kho, xe…">')
    +fld("m-mode","Phương thức khai 01/TTS",sel("m-mode",[["KY","Theo từng kỳ thanh toán"],["M","Theo tháng"],["Q","Theo quý"],["Y","Một lần theo năm"]],k.mode||"KY"),true,"Theo kỳ thanh toán: hạn ngày thứ 10 kể từ ngày bắt đầu kỳ. Theo năm: hạn ngày cuối tháng 01 năm sau.")
    +fld("m-pay","Kỳ thanh toán (số tháng/kỳ)",'<input id="m-pay" type="number" min="1" max="60" value="'+(+k.pay||1)+'">')
    +fld("m-rent","Tiền thuê / tháng (đồng)",'<input id="m-rent" type="number" min="0" step="1000" value="'+esc(k.rent||"")+'">')
    +fld("m-start","Ngày bắt đầu thuê",'<input id="m-start" type="date" value="'+esc(k.start||"")+'">')
    +fld("m-end","Ngày kết thúc thuê",'<input id="m-end" type="date" value="'+esc(k.end||"")+'">')
    +fld("m-note","Ghi chú",'<textarea id="m-note">'+esc(k.note||"")+'</textarea>',true),
    '<div>'+(id?'<button class="btn danger" data-act="tts-del">Xóa hợp đồng</button>':"")+'</div><div class="row"><button class="btn" data-act="close">Hủy</button><button class="btn pri" data-act="tts-save">Lưu</button></div>')}
const v=id=>{const e=$("#"+id);return e?(e.type==="checkbox"?e.checked:e.value.trim()):""};

/* ---------- sample data ---------- */
async function seed(){const t=today(),y=t.getFullYear(),m=t.getMonth()+1;const from=iso(D(y,m-1,1));
  const cos={"co-mau-a":{name:"Công ty Mẫu An Bình",mst:"0100000001",owner:"Lan",gtgt:"M",tncn:"M",tndn:true,qt:true,trackFrom:from,active:true,sample:true},
    "co-mau-b":{name:"Công ty Mẫu Hưng Thịnh",mst:"0100000002",owner:"Huy",gtgt:"Q",tncn:"Q",tndn:true,qt:true,trackFrom:from,active:true,sample:true},
    "co-mau-c":{name:"Công ty Mẫu Minh Phát",mst:"0100000003",owner:"Lan",gtgt:"Q",tncn:"none",tndn:true,qt:true,trackFrom:from,active:true,sample:true}};
  for(const id in cos)await put("companies",id,cos[id]);
  await put("tts","tts-mau-1",{cid:"co-mau-b",lessor:"Ông Nguyễn Văn A",asset:"Nhà mặt phố làm văn phòng",mode:"KY",pay:3,rent:25000000,start:iso(D(y,1,1)),end:iso(D(y+1,12,31)),sample:true});
  await put("tasks","task-mau-1",{cid:"co-mau-a",title:"Đối chiếu hóa đơn đầu vào tháng "+(m-1||12),who:"Lan",due:iso(addDays(t,2)),pri:"cao",status:"doing",sample:true});
  await put("tasks","task-mau-2",{cid:"co-mau-c",title:"Bổ sung hợp đồng lao động mới",who:"Huy",due:iso(addDays(t,-3)),pri:"tb",status:"todo",sample:true});
  if(!(S.settings.staff||[]).length)await putSettings(Object.assign({},S.settings,{staff:["Huy","Lan"]}));
  toast("Đã nạp dữ liệu mẫu.")}
async function unseed(){for(const col of ["companies","tts","tasks"])for(const id of Object.keys(S[col]))if(S[col][id].sample)await del(col,id);
  for(const id of Object.keys(S.done))if(id.startsWith("co-mau-"))await del("done",id);toast("Đã xóa dữ liệu mẫu.")}

/* ---------- backup file ---------- */
let PENDING=null;
const cnt=o=>Object.keys(o||{}).length;
function backupText(){return JSON.stringify({app:"so-han-thue",v:2,at:new Date().toISOString(),companies:S.companies,tts:S.tts,tasks:S.tasks,done:S.done,settings:S.settings},null,1)}
function parseBackup(txt){let o;try{o=JSON.parse(txt)}catch(e){toast("File không đúng định dạng sao lưu (.json).");return null}
  if(!o||o.app!=="so-han-thue"){toast("Đây không phải file sao lưu của Sổ Hạn Thuế.");return null}return o}
async function saveBackupFile(){
  const t=today(),name="so-han-thue_"+t.getFullYear()+pad(t.getMonth()+1)+pad(t.getDate())+".json",txt=backupText();
  let dl=null;try{dl=(window.claude&&typeof window.claude.use==="function")?await window.claude.use("downloads"):null}catch(e){dl=null}
  if(dl){try{await dl.save({filename:name,data:txt});toast("Đã lưu file "+name+".")}catch(e){if(e&&e.code==="declined")toast("Đã hủy lưu file.");else{fallbackText(txt);toast("Không tải được file ở đây, nội dung đã đặt sẵn trong ô văn bản để sao chép.")}}return}
  if(!window.claude){try{const u=URL.createObjectURL(new Blob([txt],{type:"application/json"}));const a=document.createElement("a");a.href=u;a.download=name;document.body.appendChild(a);a.click();a.remove();setTimeout(()=>URL.revokeObjectURL(u),2000);toast("Đã tải file "+name+".");return}catch(e){}}
  fallbackText(txt);toast("Không tải được file ở đây, nội dung đã đặt sẵn trong ô văn bản để sao chép.");
}
function fallbackText(txt){const d=$("#backup details");if(d)d.open=true;const ta=$("#s-json");if(ta){ta.value=txt;ta.focus();ta.select()}}
async function applyBackup(o,replace){
  if(replace)for(const col of ["companies","tts","tasks","done"])for(const id of Object.keys(S[col]))if(!(o[col]&&o[col][id]))await del(col,id);
  for(const col of ["companies","tts","tasks","done"])for(const id in (o[col]||{}))await put(col,id,o[col][id]);
  if(o.settings)await putSettings(o.settings);
  toast("Đã khôi phục "+cnt(o.companies)+" công ty, "+cnt(o.tasks)+" công việc.");
}
document.addEventListener("change",e=>{if(e.target.id!=="s-file")return;const f=e.target.files&&e.target.files[0];if(!f)return;
  const r=new FileReader();r.onload=()=>{const o=parseBackup(String(r.result||""));if(o){PENDING=o;render();const s=$("#backup");if(s)s.scrollIntoView({block:"start"})}};
  r.onerror=()=>toast("Không đọc được file.");r.readAsText(f,"utf-8")});

/* ---------- events ---------- */
let armed=null;
function toast(msg){const t=$("#toast");t.textContent=msg;t.hidden=false;clearTimeout(toast._t);toast._t=setTimeout(()=>{t.hidden=true},2600)}
function arm(btn,key){if(armed===key)return true;armed=key;btn.classList.add("armed");btn.textContent="Bấm lần nữa để xóa";setTimeout(()=>{if(armed===key)armed=null},3000);return false}
document.addEventListener("click",async e=>{
  const n=e.target.closest("[data-nav]");if(n){VIEW=n.dataset.nav;closeModal();render();window.scrollTo(0,0);return}
  const b=e.target.closest("[data-act]");if(!b)return;const a=b.dataset.act;
  if(a==="close-bg"&&e.target!==b)return;
  switch(a){
    case"close":case"close-bg":closeModal();break;
    case"popup":$("#bell").classList.remove("ring");showPopup();break;
    case"pop-mute":try{localStorage.setItem("sht-popup",iso(today()))}catch(err){}closeModal();toast("Hôm nay sẽ không tự hiện lại.");break;
    case"pop-reset":try{localStorage.removeItem("sht-popup")}catch(err){}toast("Lần mở trang tiếp theo sẽ hiện nhắc hạn.");break;
    case"pop-plan":closeModal();VIEW="plan";F.plan.who="";render();window.scrollTo(0,0);break;
    case"plan-who":F.plan.who=b.dataset.who;render();break;
    case"os-on":await enableOs();break;
    case"seed":await seed();break;
    case"unseed":await unseed();break;
    case"co-new":coForm(null);break;
    case"co-edit":coForm(b.dataset.id);break;
    case"co-save":{const name=v("m-name");if(!name){toast("Nhập tên công ty.");return}const old=EDIT?S.companies[EDIT]:{};
      const d=Object.assign(clone(old),{name,mst:v("m-mst"),owner:v("m-owner"),gtgt:v("m-gtgt"),tncn:v("m-tncn"),tndn:v("m-tndn"),qt:v("m-qt"),trackFrom:v("m-from"),active:v("m-active"),note:v("m-note")});
      closeModal();await put("companies",EDIT||uid("co"),d);toast("Đã lưu công ty.");break}
    case"co-del":if(!arm(b,"co"+EDIT))return;{const id=EDIT;closeModal();await del("companies",id);toast("Đã xóa công ty.")}break;
    case"task-new":taskForm(null);break;
    case"task-edit":taskForm(b.dataset.id);break;
    case"task-save":{const title=v("m-title");if(!title){toast("Nhập nội dung công việc.");return}const old=EDIT?S.tasks[EDIT]:{created:iso(today())};
      const st=v("m-status");const d=Object.assign(clone(old),{title,cid:v("m-cid"),who:v("m-who"),due:v("m-due"),pri:v("m-pri"),status:st,hours:Math.max(.5,+v("m-hours")||1),note:v("m-note")});
      if(st==="done"&&!d.doneAt)d.doneAt=new Date().toISOString();if(st!=="done")delete d.doneAt;
      closeModal();await put("tasks",EDIT||uid("task"),d);toast("Đã lưu công việc.");break}
    case"task-del":if(!arm(b,"t"+EDIT))return;{const id=EDIT;closeModal();await del("tasks",id);toast("Đã xóa công việc.")}break;
    case"mv":{const id=b.dataset.id,d=clone(S.tasks[id]);d.status=b.dataset.to;if(d.status==="done")d.doneAt=new Date().toISOString();else delete d.doneAt;await put("tasks",id,d);break}
    case"tts-new":ttsForm(null);break;
    case"tts-edit":ttsForm(b.dataset.id);break;
    case"tts-save":{if(!v("m-start")){toast("Nhập ngày bắt đầu thuê.");return}const old=EDIT?S.tts[EDIT]:{};
      const d=Object.assign(clone(old),{cid:v("m-cid"),lessor:v("m-lessor"),asset:v("m-asset"),mode:v("m-mode"),pay:+v("m-pay")||1,rent:v("m-rent"),start:v("m-start"),end:v("m-end"),note:v("m-note")});
      closeModal();await put("tts",EDIT||uid("tts"),d);toast("Đã lưu hợp đồng.");break}
    case"tts-del":if(!arm(b,"k"+EDIT))return;{const id=EDIT;closeModal();await del("tts",id);toast("Đã xóa hợp đồng.")}break;
    case"toggle":{const key=b.dataset.key;if(S.done[key]){await del("done",key);toast("Đã bỏ đánh dấu.")}else{const o=GEN.find(x=>x.key===key);await put("done",key,{key,cid:o?o.cid:"",date:iso(today())});toast("Đã đánh dấu đã nộp.")}break}
    case"save-set":{const w=Math.max(1,+v("s-warn")||7),hz=Math.max(30,+v("s-hz")||100);
      const staff=v("s-staff").split(/\n+/).map(x=>x.trim()).filter(Boolean);
      const hol=v("s-hol").split(/[\n,;\s]+/).map(x=>x.trim()).filter(x=>/^\d{4}-\d{2}-\d{2}$/.test(x));
      await putSettings({warnDays:w,horizon:hz,leadDays:Math.max(0,+v("s-lead")||0),fileHours:Math.max(.5,+v("s-fh")||1),capacity:Math.max(1,+v("s-cap")||40),planDays:Math.max(7,+v("s-pd")||21),staff,holidays:[...new Set(hol)].sort()});toast("Đã lưu cài đặt.");break}
    case"file-save":await saveBackupFile();break;
    case"file-pick":{const inp=$("#s-file");if(inp){inp.value="";inp.click()}break}
    case"file-apply":if(PENDING){const rep=v("s-replace");if(rep&&!arm(b,"rep"))return;await applyBackup(PENDING,rep);PENDING=null;render()}break;
    case"file-cancel":PENDING=null;render();break;
    case"export":$("#s-json").value=backupText();toast("Đã xuất. Bấm Sao chép để lưu lại.");break;
    case"copy":{const ta=$("#s-json");if(!ta.value)ta.value=backupText();
      try{await navigator.clipboard.writeText(ta.value);toast("Đã sao chép.")}catch(err){ta.focus();ta.select();toast("Đã chọn sẵn nội dung, nhấn Ctrl+C để sao chép.")}break}
    case"import":{const o=parseBackup($("#s-json").value);if(o){PENDING=o;render()}break}
  }
});
document.addEventListener("change",async e=>{const id=e.target.id;
  const a=e.target.dataset&&e.target.dataset.act;
  if(a==="assign"){const k=e.target.dataset.kind,rid=e.target.dataset.id,val=e.target.value;
    if(k==="t"){const d=clone(S.tasks[rid]);d.who=val;await put("tasks",rid,d)}
    else{const d=clone(S.companies[rid]);d.owner=val;await put("companies",rid,d)}
    toast(val?"Đã giao cho "+val+".":"Đã bỏ người phụ trách.");return}
  if(id==="f-plan-who"){F.plan.who=e.target.value;render();return}
  if(id==="f-cal-cid")F.cal.cid=e.target.value;else if(id==="f-cal-st")F.cal.st=e.target.value;else if(id==="f-cal-code")F.cal.code=e.target.value;
  else if(id==="f-task-cid")F.task.cid=e.target.value;else if(id==="f-task-who")F.task.who=e.target.value;else if(id==="f-tts-cid")F.tts.cid=e.target.value;
  else if(id==="m-cid"&&!EDIT&&$("#m-who")&&S.companies[e.target.value]){$("#m-who").value=S.companies[e.target.value].owner||"";return}
  else return;render()});
let qT;document.addEventListener("input",e=>{if(e.target.id==="f-task-q"){F.task.q=e.target.value;clearTimeout(qT);qT=setTimeout(()=>{render();const i=$("#f-task-q");if(i){i.focus();i.setSelectionRange(i.value.length,i.value.length)}},250)}});
document.addEventListener("keydown",e=>{if(e.key==="Escape"&&$("#modal").innerHTML)closeModal()});
setInterval(()=>{const t=iso(today());if(t!==render._d){render._d=t;popupChecked=false;render()}},60000);render._d=iso(today());

window.__SHT={gen,S,loadLocal};
init();
})();
</script>
Đang hiển thị lich-nhac-cong-viec.html.

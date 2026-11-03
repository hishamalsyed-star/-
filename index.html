<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>محول وحدات القياس</title>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap">
<style>
:root{--bg:#f4f6fb;--card:#fff;--text:#1b2233;--muted:#5a647a;--accent:#2563eb;--on:#fff;--border:#d9deea;--hl:#e8efff;color-scheme:light;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#0e131f;--card:#171d2d;--text:#e8ecf6;--muted:#9aa5bd;--accent:#6b95ff;--on:#0a1022;--border:#2b3350;--hl:#22304f;color-scheme:dark}}
:root[data-theme="dark"]{--bg:#0e131f;--card:#171d2d;--text:#e8ecf6;--muted:#9aa5bd;--accent:#6b95ff;--on:#0a1022;--border:#2b3350;--hl:#22304f;color-scheme:dark}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--text);font-family:Cairo,Tajawal,"Segoe UI",Tahoma,sans-serif;line-height:1.7}
main{max-width:900px;margin:0 auto;padding:16px 14px 40px;display:grid;gap:14px}
header{display:flex;align-items:center;justify-content:space-between;gap:10px}
h1{font-size:1.35rem;margin:0}
h2{font-size:1rem;margin:0 0 8px}
.card{background:var(--card);border:1px solid var(--border);border-radius:18px;box-shadow:0 2px 12px rgba(0,0,0,.06);padding:16px}
button,select,input{font:inherit;color:var(--text)}
button{border:1px solid var(--border);background:var(--card);border-radius:12px;padding:8px 14px;min-height:44px;cursor:pointer}
button.pri{background:var(--accent);color:var(--on);border-color:var(--accent);font-weight:700}
:focus-visible{outline:3px solid var(--accent);outline-offset:2px}
input,select{width:100%;min-height:50px;border:1px solid var(--border);border-radius:12px;padding:8px 12px;background:var(--bg)}
input.n{font-size:1.4rem;font-weight:700}
.cats{display:flex;gap:8px;overflow-x:auto;padding-bottom:6px}
.cats button{white-space:nowrap}
.cats button[aria-pressed="true"]{background:var(--accent);color:var(--on);border-color:var(--accent);font-weight:700}
.conv{display:grid;gap:10px;grid-template-columns:1fr;align-items:end}
.g{display:grid;gap:6px}
.g label{color:var(--muted);font-size:.85rem}
#swap{font-size:1.4rem;justify-self:center;width:52px}
.row{display:flex;gap:10px;flex-wrap:wrap;align-items:end;margin-top:12px}
.row>*{flex:1 1 140px}
.tw{overflow-x:auto}
table{width:100%;border-collapse:collapse}
td{padding:8px 10px;border-bottom:1px solid var(--border)}
tr[data-u]{cursor:pointer}
tr.cur{background:var(--hl);font-weight:700}
td.v{text-align:end;direction:ltr;font-variant-numeric:tabular-nums}
.list{display:flex;flex-wrap:wrap;gap:8px}
.list button{font-size:.9rem}
.sr{display:grid;gap:6px;margin-top:8px}
.sr button{text-align:start}
.muted{color:var(--muted)}
@media(min-width:640px){.conv{grid-template-columns:1fr auto 1fr}#swap{margin-bottom:0}}
</style>
</head>
<body>
<main>
<header>
  <h1 data-i="title"></h1>
  <div class="list">
    <button id="lang" type="button" aria-label="Language">EN</button>
    <button id="theme" type="button" aria-label="Theme">🌓</button>
  </div>
</header>

<section class="card">
  <input id="q" type="search" data-ip="search" aria-label="search">
  <div id="sr" class="sr"></div>
</section>

<nav id="cats" class="cats" aria-label="categories"></nav>

<section class="card">
  <div class="conv">
    <div class="g"><label for="a" data-i="from"></label><input id="a" class="n" dir="ltr" autocomplete="off"><select id="fa" aria-label="from unit"></select></div>
    <button id="swap" type="button" data-ia="swap">⇄</button>
    <div class="g"><label for="b" data-i="to"></label><input id="b" class="n" dir="ltr" autocomplete="off"><select id="fb" aria-label="to unit"></select></div>
  </div>
  <div class="row">
    <div class="g"><label for="d" data-i="prec"></label><select id="d"></select></div>
    <button id="copy" class="pri" type="button" data-i="copy"></button>
    <button id="pin" type="button" data-i="pin"></button>
  </div>
</section>

<section class="card">
  <h2 data-i="all"></h2>
  <div class="tw"><table><tbody id="tb"></tbody></table></div>
</section>

<section class="card">
  <h2 data-i="favs"></h2>
  <div id="pins" class="list"></div>
  <h2 style="margin-top:14px" data-i="hist"></h2>
  <div id="hist" class="list"></div>
</section>
<p class="muted" data-i="note"></p>
</main>

<script>
/* ===== بيانات الوحدات: كل فئة لها وحدة أساسية (المعامل = كم وحدة أساسية في الوحدة) ===== */
/* To add a unit: add a line L('عربي','English',factor) to the category. */
const L=(a,e,k)=>({n:[a,e],t:x=>x*k,f:x=>x/k});
const D={
 len:{n:['الطول','Length'],u:{m:L('متر','Meter',1),km:L('كيلومتر','Kilometer',1000),cm:L('سنتيمتر','Centimeter',.01),mm:L('مليمتر','Millimeter',.001),mi:L('ميل','Mile',1609.344),yd:L('ياردة','Yard',.9144),ft:L('قدم','Foot',.3048),in:L('بوصة','Inch',.0254),nmi:L('ميل بحري','Nautical mile',1852)}},
 mass:{n:['الوزن','Mass'],u:{kg:L('كيلوجرام','Kilogram',1),g:L('جرام','Gram',.001),mg:L('ملجرام','Milligram',1e-6),t:L('طن','Tonne',1000),lb:L('رطل','Pound',.45359237),oz:L('أونصة','Ounce',.028349523125),ct:L('قيراط','Carat',.0002)}},
 vol:{n:['الحجم','Volume'],u:{l:L('لتر','Liter',1),ml:L('مليلتر','Milliliter',.001),m3:L('متر مكعب','Cubic meter',1000),gus:L('جالون أمريكي','US gallon',3.785411784),guk:L('جالون بريطاني','UK gallon',4.54609),cup:L('كوب','Cup',.2365882365),tbsp:L('ملعقة كبيرة','Tablespoon',.01478676478),tsp:L('ملعقة صغيرة','Teaspoon',.00492892159),bbl:L('برميل','Barrel (oil)',158.987294928)}},
 area:{n:['المساحة','Area'],u:{m2:L('متر مربع','Square meter',1),km2:L('كيلومتر مربع','Square km',1e6),ha:L('هكتار','Hectare',1e4),ac:L('فدان','Acre',4046.8564224),fd:L('فدان مصري','Egyptian feddan',4200.83),ft2:L('قدم مربعة','Square foot',.09290304),mi2:L('ميل مربع','Square mile',2589988.110336)}},
 temp:{n:['الحرارة','Temperature'],u:{c:{n:['مئوية','Celsius'],t:x=>x,f:x=>x},f:{n:['فهرنهايت','Fahrenheit'],t:x=>(x-32)*5/9,f:x=>x*9/5+32},k:{n:['كلفن','Kelvin'],t:x=>x-273.15,f:x=>x+273.15}}},
 spd:{n:['السرعة','Speed'],u:{kmh:L('كم/ساعة','km/h',1/3.6),ms:L('م/ث','m/s',1),mph:L('ميل/ساعة','mph',.44704),kn:L('عقدة','Knot',1852/3600)}},
 time:{n:['الوقت','Time'],u:{s:L('ثانية','Second',1),min:L('دقيقة','Minute',60),h:L('ساعة','Hour',3600),d:L('يوم','Day',86400),w:L('أسبوع','Week',604800),mo:L('شهر','Month',2629800),y:L('سنة','Year',31557600)}},
 pres:{n:['الضغط','Pressure'],u:{pa:L('باسكال','Pascal',1),bar:L('بار','Bar',1e5),psi:L('psi','psi',6894.757293168),atm:L('atm','atm',101325),mmhg:L('mmHg','mmHg',133.322387415)}},
 en:{n:['الطاقة','Energy'],u:{j:L('جول','Joule',1),kj:L('كيلوجول','Kilojoule',1000),cal:L('سعرة حرارية','Calorie',4.184),kwh:L('كيلووات ساعة','kWh',3.6e6),btu:L('BTU','BTU',1055.05585262)}},
 pow:{n:['القدرة','Power'],u:{w:L('وات','Watt',1),kw:L('كيلووات','Kilowatt',1000),hp:L('حصان','Horsepower',745.69987158)}},
 data:{n:['البيانات','Data'],u:{bit:L('بت','Bit',1),B:L('بايت','Byte',8),KB:L('كيلوبايت','Kilobyte',8192),MB:L('ميجابايت','Megabyte',8388608),GB:L('جيجابايت','Gigabyte',8589934592),TB:L('تيرابايت','Terabyte',8796093022208)}},
 ang:{n:['الزاوية','Angle'],u:{deg:L('درجة','Degree',1),rad:L('راديان','Radian',180/Math.PI)}},
 fuel:{n:['الوقود','Fuel'],u:{kml:L('كم/لتر','km/L',1),mpg:L('ميل/جالون','mpg (US)',0.425143707),l100:{n:['لتر/100كم','L/100km'],t:x=>100/x,f:x=>100/x}}}
};
const T={
 ar:{title:'محول وحدات القياس',from:'من',to:'إلى',swap:'تبديل',prec:'الدقة (خانات عشرية)',copy:'نسخ النتيجة',copied:'تم النسخ ✓',pin:'☆ تثبيت التحويل',all:'التحويل لجميع الوحدات',favs:'المفضلة',hist:'آخر 10 تحويلات',search:'ابحث عن وحدة...',none:'لا شيء بعد',note:'ملاحظة: وحدات البيانات ثنائية (1 كيلوبايت = 1024 بايت)، والشهر = 30.4375 يوم.'},
 en:{title:'Unit Converter',from:'From',to:'To',swap:'Swap',prec:'Precision (decimals)',copy:'Copy result',copied:'Copied ✓',pin:'☆ Pin conversion',all:'Convert to all units',favs:'Favorites',hist:'Last 10 conversions',search:'Search for a unit...',none:'Nothing yet',note:'Note: data units are binary (1 KB = 1024 bytes); a month = 30.4375 days.'}
};

/* ===== الحالة والتخزين ===== */
const $=id=>document.getElementById(id);
const s={cat:'len',from:'m',to:'ft',lang:'ar',d:6,theme:'',hist:[],pins:[]};
try{Object.assign(s,JSON.parse(localStorage.getItem('uc')||'{}'))}catch(e){}
const save=()=>{try{localStorage.setItem('uc',JSON.stringify({lang:s.lang,d:s.d,theme:s.theme,hist:s.hist,pins:s.pins}))}catch(e){}};
const li=()=>s.lang==='ar'?0:1, tr=k=>T[s.lang][k];
const U=()=>D[s.cat].u, nm=(c,u)=>D[c].u[u].n[li()];

/* ===== التحويل: عبر الوحدة الأساسية ===== */
const conv=(x,fu,tu)=>U()[tu].f(U()[fu].t(x));
const num=v=>{v=String(v).trim().replace(/[٠-٩]/g,d=>'٠١٢٣٤٥٦٧٨٩'.indexOf(d)).replace(/[٫,]/g,'.');return(v===''||v==='-'||v==='.')?NaN:Number(v)};
const plain=v=>{if(!isFinite(v))return'';const a=Math.abs(v);if(a>=1e15||(a>0&&a<1e-6))return v.toExponential(Math.min(s.d,10));const r=String(+v.toFixed(s.d));return r==='-0'?'0':r};
const disp=v=>{if(!isFinite(v))return'—';const a=Math.abs(v);if(v===0)return'0';if(a>=1e12||a<1e-4)return v.toExponential(Math.min(s.d,6));return v.toLocaleString('en-US',{maximumFractionDigits:s.d})};

/* ===== الواجهة ===== */
function text(){
  document.documentElement.lang=s.lang;document.documentElement.dir=s.lang==='ar'?'rtl':'ltr';
  document.title=tr('title');$('lang').textContent=s.lang==='ar'?'EN':'ع';
  document.querySelectorAll('[data-i]').forEach(e=>e.textContent=tr(e.dataset.i));
  document.querySelectorAll('[data-ip]').forEach(e=>e.placeholder=tr(e.dataset.ip));
  document.querySelectorAll('[data-ia]').forEach(e=>e.setAttribute('aria-label',tr(e.dataset.ia)));
}
function cats(){
  $('cats').innerHTML='';
  for(const k in D){const b=document.createElement('button');b.type='button';b.textContent=D[k].n[li()];b.setAttribute('aria-pressed',k===s.cat);b.onclick=()=>{s.cat=k;const ks=Object.keys(U());s.from=ks[0];s.to=ks[1]||ks[0];render()};$('cats').append(b)}
}
function selects(){
  const o=Object.keys(U()).map(k=>`<option value="${k}">${nm(s.cat,k)}</option>`).join('');
  $('fa').innerHTML=o;$('fb').innerHTML=o;$('fa').value=s.from;$('fb').value=s.to;
  $('d').innerHTML=[0,1,2,3,4,5,6,8,10].map(n=>`<option ${n===s.d?'selected':''}>${n}</option>`).join('');
  const m=s.cat==='temp'?'text':'decimal';$('a').inputMode=m;$('b').inputMode=m;
}
function table(){
  const x=num($('a').value);
  $('tb').innerHTML=Object.keys(U()).map(k=>`<tr data-u="${k}" class="${k===s.to?'cur':''}"><td>${nm(s.cat,k)}</td><td class="v">${isNaN(x)?'—':disp(conv(x,s.from,k))}</td></tr>`).join('');
  $('tb').querySelectorAll('tr').forEach(r=>r.onclick=()=>{s.to=r.dataset.u;$('fb').value=s.to;calc('a')});
}
function lists(){
  $('pins').innerHTML=s.pins.length?'':`<span class="muted">${tr('none')}</span>`;
  s.pins.forEach((p,i)=>{const b=document.createElement('button');b.type='button';b.textContent=`★ ${nm(p.c,p.f)} → ${nm(p.c,p.t)}`;b.onclick=()=>{s.cat=p.c;s.from=p.f;s.to=p.t;render()};b.oncontextmenu=e=>{e.preventDefault();s.pins.splice(i,1);save();lists()};b.title=s.lang==='ar'?'كليك يمين/ضغط مطول للحذف':'Right-click / long-press to remove';$('pins').append(b)});
  $('hist').innerHTML=s.hist.length?'':`<span class="muted">${tr('none')}</span>`;
  s.hist.forEach(h=>{const x=num(h.v);const r=D[h.c].u[h.t].f(D[h.c].u[h.f].t(x));const b=document.createElement('button');b.type='button';b.textContent=`${h.v} ${nm(h.c,h.f)} = ${plain(r)} ${nm(h.c,h.t)}`;b.onclick=()=>{s.cat=h.c;s.from=h.f;s.to=h.t;render($('a').value=h.v,calc('a'))};$('hist').append(b)});
}
function calc(src){
  const A=$('a'),B=$('b');
  if(src==='a'){const x=num(A.value);B.value=isNaN(x)?'':plain(conv(x,s.from,s.to))}
  else{const x=num(B.value);A.value=isNaN(x)?'':plain(conv(x,s.to,s.from))}
  table();clearTimeout(calc.t);calc.t=setTimeout(addHist,900);
}
function addHist(){
  const x=num($('a').value);if(isNaN(x)||!isFinite(conv(x,s.from,s.to)))return;
  const h={c:s.cat,f:s.from,t:s.to,v:$('a').value.trim()},p=s.hist[0];
  if(p&&p.c===h.c&&p.f===h.f&&p.t===h.t&&p.v===h.v)return;
  s.hist.unshift(h);s.hist=s.hist.slice(0,10);save();lists();
}
function render(){text();cats();selects();lists();calc('a')}

/* ===== الأحداث ===== */
$('a').oninput=()=>calc('a');$('b').oninput=()=>calc('b');
$('fa').onchange=e=>{s.from=e.target.value;calc('a')};
$('fb').onchange=e=>{s.to=e.target.value;calc('a')};
$('d').onchange=e=>{s.d=+e.target.value;save();calc('a')};
$('swap').onclick=()=>{[s.from,s.to]=[s.to,s.from];$('fa').value=s.from;$('fb').value=s.to;const v=$('b').value;if(v)$('a').value=v;calc('a')};
$('copy').onclick=async()=>{
  const t=`${$('a').value} ${nm(s.cat,s.from)} = ${$('b').value} ${nm(s.cat,s.to)}`,b=$('copy');
  try{await navigator.clipboard.writeText(t)}catch(e){const r=document.createElement('textarea');r.value=t;document.body.append(r);r.select();try{document.execCommand('copy')}catch(_){}r.remove()}
  b.textContent=tr('copied');setTimeout(()=>b.textContent=tr('copy'),1800);
};
$('pin').onclick=()=>{if(!s.pins.some(p=>p.c===s.cat&&p.f===s.from&&p.t===s.to)){s.pins.unshift({c:s.cat,f:s.from,t:s.to});save();lists()}};
$('lang').onclick=()=>{s.lang=s.lang==='ar'?'en':'ar';save();render()};
$('theme').onclick=()=>{const dark=s.theme?s.theme==='dark':matchMedia('(prefers-color-scheme:dark)').matches;s.theme=dark?'light':'dark';document.documentElement.dataset.theme=s.theme;save()};
$('q').oninput=e=>{
  const q=e.target.value.trim().toLowerCase(),box=$('sr');box.innerHTML='';if(!q)return;let n=0;
  for(const c in D)for(const u in D[c].u){
    const un=D[c].u[u].n;if(n<8&&(un[0].includes(q)||un[1].toLowerCase().includes(q))){
      n++;const b=document.createElement('button');b.type='button';b.textContent=`${un[li()]} — ${D[c].n[li()]}`;
      b.onclick=()=>{s.cat=c;s.from=u;s.to=Object.keys(D[c].u).find(k=>k!==u);box.innerHTML='';$('q').value='';render()};box.append(b)}}
};
if(s.theme)document.documentElement.dataset.theme=s.theme;
$('a').value='1';
render();
</script>
</body>
</html>

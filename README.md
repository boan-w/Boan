
<style>
@import url('https://fonts.googleapis.com/css2?family=Segoe+UI:wght@300;400;600;700&display=swap');
*{box-sizing:border-box;margin:0;padding:0}
:root{--sb:#1a1a2e;--sbw:176px;--f:'Segoe UI',system-ui,sans-serif}
html,body{font-family:var(--f)}
.shell{display:flex;min-height:820px;border-radius:8px;overflow:hidden;border:1px solid #d0d0d0}
.sb{width:var(--sbw);background:var(--sb);display:flex;flex-direction:column;flex-shrink:0}
.sb-hdr{padding:.75rem 1rem .6rem;border-bottom:0.5px solid rgba(255,255,255,.08);display:flex;align-items:center;gap:6px}
.sb-icon{width:20px;height:20px;background:#e84393;border-radius:3px;display:flex;align-items:center;justify-content:center;flex-shrink:0}
.sb-title{font-size:11px;font-weight:700;color:#fff;letter-spacing:.02em}
.ni{display:flex;align-items:center;cursor:pointer;position:relative}
.ni-bar{width:3px;background:transparent;align-self:stretch;flex-shrink:0;transition:background .15s;min-height:32px}
.ni.active .ni-bar{background:#e84393}
.ni-inner{flex:1;display:flex;align-items:center;gap:7px;padding:7px 1rem 7px .75rem;transition:background .15s}
.ni:hover .ni-inner{background:rgba(255,255,255,.05)}
.ni.active .ni-inner{background:rgba(232,67,147,.1)}
.ni-lbl{font-size:11px;color:rgba(255,255,255,.4);font-weight:400}
.ni.active .ni-lbl,.ni:hover .ni-lbl{color:#fff}
.ni.active .ni-lbl{font-weight:600}
.ni svg{width:12px;height:12px;opacity:.3;flex-shrink:0}
.ni.active svg,.ni:hover svg{opacity:.75}
.sb-grp-lbl{font-size:9px;font-weight:700;color:rgba(255,255,255,.25);letter-spacing:.1em;text-transform:uppercase;padding:.6rem 1rem .3rem}
.sb-foot{margin-top:auto;padding:.6rem 1rem;border-top:0.5px solid rgba(255,255,255,.06);font-size:8px;color:rgba(255,255,255,.2);line-height:1.6}
.main{flex:1;background:#f4f6fb;display:flex;flex-direction:column;min-width:0;overflow:hidden}
.topbar{background:#fff;border-bottom:1px solid #e8eaf0;padding:.45rem 1.25rem;display:flex;align-items:center;justify-content:space-between;flex-shrink:0}
.tb-title{font-size:14px;font-weight:700;color:#1a1a2e}
.tb-r{display:flex;gap:10px;align-items:center}
.tb-ctrl{display:flex;align-items:center;gap:4px;font-size:10px;color:#888}
.tb-ctrl select{font-size:10px;padding:2px 5px;border:1px solid #ddd;border-radius:3px;background:#fff;color:#333;outline:none}
.tb-btn{font-size:10px;padding:3px 10px;border:1px solid #ddd;border-radius:3px;background:#fff;color:#333;cursor:pointer;display:flex;align-items:center;gap:4px}
.page{display:none;overflow-y:auto;padding:1rem 1.1rem}
.page.active{display:block}
.page::-webkit-scrollbar{width:4px}
.page::-webkit-scrollbar-thumb{background:#ccc;border-radius:2px}
.sec-hdr{font-size:13px;font-weight:700;color:#1a1a2e;margin-bottom:.65rem;margin-top:.1rem}
.kpi-row{display:grid;gap:10px;margin-bottom:.9rem}
.kpi-4{grid-template-columns:repeat(4,minmax(0,1fr))}
.kpi-card{background:#fff;border:1px solid #e8eaf0;border-radius:6px;padding:.8rem 1rem}
.kpi-label{font-size:11px;color:#555;margin-bottom:.4rem}
.kpi-val{font-size:26px;font-weight:300;color:#1a1a2e;line-height:1;margin-bottom:.4rem}
.kpi-sep{border-top:1px solid #e8eaf0;margin:.4rem 0}
.kpi-sub{display:flex;gap:12px;font-size:9px;color:#888}
.kpi-sub-item{display:flex;flex-direction:column;gap:1px}
.kpi-sub-num{font-size:10px;font-weight:600;color:#1a1a2e}
.chart-card{background:#fff;border:1px solid #e8eaf0;border-radius:6px;padding:.8rem 1rem}
.chart-title{font-size:11px;font-weight:600;color:#333;margin-bottom:.5rem}
.g2{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-bottom:.9rem}
.leg{display:flex;flex-wrap:wrap;gap:8px;margin-bottom:6px;font-size:9px;color:#666}
.li{display:flex;align-items:center;gap:3px}
.ls{width:8px;height:8px;border-radius:1px;flex-shrink:0;display:inline-block}
.delay-bar{display:flex;height:28px;border-radius:3px;overflow:hidden;margin:.4rem 0}
.delay-seg{display:flex;align-items:center;justify-content:center;font-size:10px;font-weight:700;color:#fff}
.sup-donuts{display:grid;grid-template-columns:repeat(4,1fr);gap:10px;margin-bottom:.9rem}
.sup-donut-card{background:#fff;border:1px solid #e8eaf0;border-radius:6px;padding:.75rem .6rem;text-align:center}
.sup-donut-title{font-size:10px;color:#555;margin-bottom:.4rem}
.sup-donut-val{font-size:12px;font-weight:700;margin-top:.3rem}
.hmap-wrap{overflow-x:auto}
.hmap{width:100%;border-collapse:collapse;font-size:10px}
.hmap th{font-size:9px;font-weight:600;color:#888;text-align:center;padding:4px 6px;border-bottom:1px solid #e8eaf0;white-space:nowrap;background:#fafafa}
.hmap th:first-child{text-align:left}
.hmap td{padding:5px 6px;text-align:center;border-bottom:0.5px solid #f0f0f0;font-weight:600;font-size:10px}
.hmap td:first-child{text-align:left;font-weight:400;color:#333}
.hmap tr:last-child td{border-bottom:none}
</style>

<div class="shell">
<div class="sb">
  <div class="sb-hdr">
    <div class="sb-icon"><svg viewBox="0 0 12 12" fill="white"><rect x="1" y="1" width="4" height="4" rx=".5"/><rect x="7" y="1" width="4" height="4" rx=".5"/><rect x="1" y="7" width="4" height="4" rx=".5"/><rect x="7" y="7" width="4" height="4" rx=".5"/></svg></div>
    <div class="sb-title">DASHBOARDS</div>
  </div>
  <div style="padding:.4rem 0">
    <div class="ni active" id="nav-sup" onclick="gotoPage('supplier',this)">
      <div class="ni-bar"></div>
      <div class="ni-inner">
        <svg viewBox="0 0 14 14" fill="none"><circle cx="7" cy="5" r="3" stroke="white" stroke-width="1.2"/><path d="M2 12c0-2.2 2.2-4 5-4s5 1.8 5 4" stroke="white" stroke-width="1.2" stroke-linecap="round"/></svg>
        <span class="ni-lbl">Supplier Management</span>
      </div>
    </div>
    <div class="ni" id="nav-risk" onclick="gotoPage('risk',this)">
      <div class="ni-bar"></div>
      <div class="ni-inner">
        <svg viewBox="0 0 14 14" fill="none"><path d="M7 2L13 11H1L7 2Z" stroke="white" stroke-width="1.2" stroke-linejoin="round"/><path d="M7 6v2.5" stroke="white" stroke-width="1.2" stroke-linecap="round"/><circle cx="7" cy="10" r=".5" fill="white"/></svg>
        <span class="ni-lbl">Supply Chain Risk</span>
      </div>
    </div>
  </div>
  <div class="sb-grp-lbl">Other</div>
  <div class="ni"><div class="ni-bar"></div><div class="ni-inner"><svg viewBox="0 0 14 14" fill="none"><rect x="1" y="3" width="12" height="8" rx="1" stroke="white" stroke-width="1.2"/><path d="M4 7h6M4 9.5h3.5" stroke="white" stroke-width="1" stroke-linecap="round"/></svg><span class="ni-lbl">Demand Planning</span></div></div>
  <div class="ni"><div class="ni-bar"></div><div class="ni-inner"><svg viewBox="0 0 14 14" fill="none"><path d="M2 12V6l5-4 5 4v6" stroke="white" stroke-width="1.2" stroke-linejoin="round"/></svg><span class="ni-lbl">Inventory Mgmt</span></div></div>
  <div class="ni"><div class="ni-bar"></div><div class="ni-inner"><svg viewBox="0 0 14 14" fill="none"><circle cx="7" cy="7" r="5" stroke="white" stroke-width="1.2"/><path d="M7 4.5v2.5l2 1.5" stroke="white" stroke-width="1.2" stroke-linecap="round"/></svg><span class="ni-lbl">Order Management</span></div></div>
  <div class="ni"><div class="ni-bar"></div><div class="ni-inner"><svg viewBox="0 0 14 14" fill="none"><path d="M2 11L5 7l3 3 4-6" stroke="white" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round"/></svg><span class="ni-lbl">Transportation & Logistics</span></div></div>
  <div class="sb-foot">Anker Innovations Ltd.<br>Procurement Hub · Q1 2025</div>
</div>

<div class="main">
<div class="topbar">
  <div class="tb-title" id="tb-title">Supplier Management Dashboard</div>
  <div class="tb-r">
    <div class="tb-ctrl"><span>Date range</span><select><option>Last year</option><option>Last quarter</option><option>Q1 2025</option></select></div>
    <div class="tb-ctrl"><span>Supplier</span><select><option>All</option><option>OEM/ODM</option><option>Battery cell</option></select></div>
    <div class="tb-btn">Edit</div>
    <div class="tb-btn">Share</div>
    <div class="tb-btn">···</div>
  </div>
</div>

<!-- PAGE: SUPPLIER MANAGEMENT -->
<div class="page active" id="page-supplier">
  <div class="sec-hdr">Supplier Performance Overview</div>
  <div class="kpi-row kpi-4">
    <div class="kpi-card">
      <div class="kpi-label">Supplier Quality Rate</div>
      <div class="kpi-val">89.7%</div>
      <div class="kpi-sep"></div>
      <div class="kpi-sub">
        <div class="kpi-sub-item"><span style="color:#c0392b">▼ -0.4%</span><span>Versus</span></div>
        <div class="kpi-sub-item" style="border-left:1px solid #eee;padding-left:10px"><span class="kpi-sub-num">90.1%</span><span>Previous period</span></div>
      </div>
    </div>
    <div class="kpi-card">
      <div class="kpi-label">Supplier Defect Rate</div>
      <div class="kpi-val" style="color:#c0392b">10.1%</div>
      <div class="kpi-sep"></div>
      <div class="kpi-sub">
        <div class="kpi-sub-item"><span style="color:#c0392b">▲ +2.3%</span><span>Versus</span></div>
        <div class="kpi-sub-item" style="border-left:1px solid #eee;padding-left:10px"><span class="kpi-sub-num">7.8%</span><span>Previous period</span></div>
      </div>
    </div>
    <div class="kpi-card">
      <div class="kpi-label">Supplier On-Time Delivery</div>
      <div class="kpi-val">92.3%</div>
      <div class="kpi-sep"></div>
      <div class="kpi-sub">
        <div class="kpi-sub-item"><span style="color:#27ae60">▲ +0.8%</span><span>Versus</span></div>
        <div class="kpi-sub-item" style="border-left:1px solid #eee;padding-left:10px"><span class="kpi-sub-num">91.5%</span><span>Previous period</span></div>
      </div>
    </div>
    <div class="kpi-card">
      <div class="kpi-label">Cost of Supplier</div>
      <div class="kpi-val" style="font-size:22px">$134,963</div>
      <div class="kpi-sep"></div>
      <div class="kpi-sub">
        <div class="kpi-sub-item"><span style="color:#27ae60">▼ -3.2%</span><span>Versus</span></div>
        <div class="kpi-sub-item" style="border-left:1px solid #eee;padding-left:10px"><span class="kpi-sub-num">$139,420</span><span>Previous period</span></div>
      </div>
    </div>
  </div>

  <div class="g2">
    <div class="chart-card">
      <div class="chart-title">Supplier Quality</div>
      <div style="position:relative;height:195px"><canvas id="c-qual"></canvas></div>
    </div>
    <div class="chart-card">
      <div class="chart-title">Supplier Defect Rate</div>
      <div class="leg">
        <span class="li"><span class="ls" style="background:#2196F3"></span>Raw Material</span>
        <span class="li"><span class="ls" style="background:#4CAF50"></span>Electronics</span>
        <span class="li"><span class="ls" style="background:#F44336"></span>Packaging</span>
      </div>
      <div style="position:relative;height:175px"><canvas id="c-defect"></canvas></div>
    </div>
  </div>

  <div class="g2">
    <div class="chart-card">
      <div class="chart-title">Cost of Suppliers</div>
      <div class="leg" id="cost-leg"></div>
      <div style="position:relative;height:195px"><canvas id="c-cost"></canvas></div>
    </div>
    <div class="chart-card">
      <div class="chart-title">Supplier Scorecard Performance</div>
      <div style="display:flex;justify-content:space-between;font-size:8px;color:#999;margin-bottom:6px">
        <span>Performance Rate</span>
        <span style="display:flex;gap:6px"><span>Low</span><span>————→</span><span>High</span></span>
      </div>
      <div class="hmap-wrap">
        <table class="hmap" id="scorecard-hmap"></table>
      </div>
      <div style="margin-top:12px;display:grid;grid-template-columns:1fr 1fr;gap:6px" id="ext-mini"></div>
    </div>
  </div>
</div>

<!-- PAGE: SUPPLY CHAIN RISK -->
<div class="page" id="page-risk">
  <div class="sec-hdr">Supply Chain Risk Overview</div>

  <div style="display:grid;grid-template-columns:repeat(4,minmax(0,1fr)) 1.4fr;gap:10px;margin-bottom:.9rem">
    <div class="kpi-card">
      <div class="kpi-label">Total Supply Chain Cost</div>
      <div class="kpi-val" style="font-size:22px">$7.8M</div>
      <div class="kpi-sep"></div>
      <div class="kpi-sub">
        <div class="kpi-sub-item"><span style="color:#c0392b">▲ +6.8%</span><span>Versus</span></div>
        <div class="kpi-sub-item" style="border-left:1px solid #eee;padding-left:10px"><span class="kpi-sub-num">$7.3M</span><span>Previous period</span></div>
      </div>
    </div>
    <div class="kpi-card">
      <div class="kpi-label">Supply Chain Cycle Time</div>
      <div class="kpi-val">35 days</div>
      <div class="kpi-sep"></div>
      <div class="kpi-sub">
        <div class="kpi-sub-item"><span style="color:#27ae60">▼ -5.4%</span><span>Versus</span></div>
        <div class="kpi-sub-item" style="border-left:1px solid #eee;padding-left:10px"><span class="kpi-sub-num">37 days</span><span>Previous period</span></div>
      </div>
    </div>
    <div class="kpi-card">
      <div class="kpi-label">Total Delivery Delays</div>
      <div class="kpi-val" style="color:#c0392b">3 200</div>
      <div class="kpi-sep"></div>
      <div class="kpi-sub">
        <div class="kpi-sub-item"><span style="color:#c0392b">▲ +12.3%</span><span>Versus</span></div>
        <div class="kpi-sub-item" style="border-left:1px solid #eee;padding-left:10px"><span class="kpi-sub-num">2 850</span><span>Previous period</span></div>
      </div>
    </div>
    <div class="kpi-card">
      <div class="kpi-label">Perfect Order Rate</div>
      <div class="kpi-val">94.2%</div>
      <div class="kpi-sep"></div>
      <div class="kpi-sub">
        <div class="kpi-sub-item"><span style="color:#c0392b">▼ -1.3%</span><span>Versus</span></div>
        <div class="kpi-sub-item" style="border-left:1px solid #eee;padding-left:10px"><span class="kpi-sub-num">95.5%</span><span>Previous period</span></div>
      </div>
    </div>
    <div class="kpi-card">
      <div class="kpi-label" style="font-size:9px">Delivery Delays</div>
      <div class="leg" style="font-size:8px;gap:5px;margin-bottom:6px">
        <span class="li"><span class="ls" style="background:#4CAF50"></span>Other</span>
        <span class="li"><span class="ls" style="background:#F44336"></span>Supplier</span>
        <span class="li"><span class="ls" style="background:#2196F3"></span>Weather</span>
        <span class="li"><span class="ls" style="background:#FFC107"></span>Transport</span>
      </div>
      <div class="delay-bar">
        <div class="delay-seg" style="flex:16;background:#4CAF50">16%</div>
        <div class="delay-seg" style="flex:25;background:#F44336">25%</div>
        <div class="delay-seg" style="flex:34;background:#2196F3">34%</div>
        <div class="delay-seg" style="flex:25;background:#FFC107;color:#333">25%</div>
      </div>
    </div>
  </div>

  <div class="sec-hdr">Resource and Cost Monitoring</div>
  <div class="chart-card" style="margin-bottom:.9rem">
    <div class="chart-title">Total Supply Chain Cost Breakdown</div>
    <div class="leg">
      <span class="li"><span class="ls" style="background:#4CAF50"></span>Procurement</span>
      <span class="li"><span class="ls" style="background:#2196F3"></span>Transportation</span>
      <span class="li"><span class="ls" style="background:#F44336"></span>Warehousing</span>
    </div>
    <div style="position:relative;height:160px"><canvas id="c-scost"></canvas></div>
  </div>

  <div class="sec-hdr">Supplier Risk Breakdown</div>
  <div class="sup-donuts" id="sup-donuts"></div>

  <div style="display:grid;grid-template-columns:repeat(3,1fr);gap:8px;margin-bottom:.9rem" id="risk-kpis"></div>
</div>

</div>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.js"></script>
<script>
const tc='#999',gc='rgba(0,0,0,.05)';

function gotoPage(id,el){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
  document.querySelectorAll('.ni').forEach(n=>n.classList.remove('active'));
  document.getElementById('page-'+id).classList.add('active');
  el.classList.add('active');
  const t={supplier:'Supplier Management Dashboard',risk:'Supply Chain Risk Management Dashboard'};
  document.getElementById('tb-title').textContent=t[id];
}

/* Quality */
new Chart(document.getElementById('c-qual'),{
  type:'bar',
  data:{
    labels:['Aohai','Salcomp','Huntkey','Hyluton','ATL (new)'],
    datasets:[{data:[94.2,91.8,88.5,85.2,97.1],backgroundColor:'#2196F3',borderRadius:2,barThickness:18}]
  },
  options:{indexAxis:'y',responsive:true,maintainAspectRatio:false,
    plugins:{legend:{display:false},tooltip:{callbacks:{label:c=>c.raw+'%'}}},
    scales:{x:{min:80,max:100,ticks:{font:{size:9},color:tc,callback:v=>v+'%'},grid:{color:gc}},y:{ticks:{font:{size:10},color:'#333'},grid:{display:false}}}
  }
});

/* Defect */
new Chart(document.getElementById('c-defect'),{
  type:'bar',
  data:{
    labels:['Aohai','Salcomp','Huntkey','Hyluton','Apex Wuxi'],
    datasets:[
      {label:'Raw Material',data:[2.1,3.5,4.8,6.2,28.4],backgroundColor:'#2196F3'},
      {label:'Electronics',data:[2.8,3.2,5.1,6.9,14.2],backgroundColor:'#4CAF50'},
      {label:'Packaging',data:[0.9,1.5,1.6,1.7,5.1],backgroundColor:'#F44336'}
    ]
  },
  options:{indexAxis:'y',responsive:true,maintainAspectRatio:false,
    plugins:{legend:{display:false},tooltip:{callbacks:{label:c=>c.dataset.label+': '+c.raw+'%'}}},
    scales:{x:{stacked:true,ticks:{font:{size:9},color:tc,callback:v=>v+'%'},grid:{color:gc}},y:{stacked:true,ticks:{font:{size:10},color:'#333'},grid:{display:false}}}
  }
});

/* Cost pie */
const cd={labels:['Aohai','Salcomp','Huntkey','Hyluton'],pct:[34,28,22,16],cols:['#2196F3','#4CAF50','#F44336','#FF9800']};
document.getElementById('cost-leg').innerHTML=cd.labels.map((l,i)=>`<span class="li"><span class="ls" style="background:${cd.cols[i]}"></span>${l} ${cd.pct[i]}%</span>`).join('');
new Chart(document.getElementById('c-cost'),{
  type:'pie',
  data:{labels:cd.labels,datasets:[{data:cd.pct,backgroundColor:cd.cols,borderWidth:2,borderColor:'#fff'}]},
  options:{responsive:true,maintainAspectRatio:false,plugins:{legend:{display:false},tooltip:{callbacks:{label:c=>c.label+': '+c.raw+'%'}}}}
});

/* Scorecard heatmap */
const scorecardData=[
  {dim:'Quality',vals:[94.2,91.8,88.5,97.1,85.2]},
  {dim:'On-Time Delivery',vals:[96,94,90,95,87]},
  {dim:'Reliability',vals:[92,90,86,96,82]},
  {dim:'Cost-Efficiency',vals:[88,85,80,80,78]},
];
const supLabels=['Aohai','Salcomp','Huntkey','ATL','Hyluton'];
function hmCol(v){
  const n=Math.min(Math.max((v-70)/30,0),1);
  const r=Math.round(33+180*(1-n));
  const g=Math.round(150+55*n);
  const b=Math.round(243-180*n);
  return`rgb(${r},${g},${b})`;
}
const tbl=document.getElementById('scorecard-hmap');
tbl.innerHTML=`<thead><tr><th style="text-align:left"></th>${supLabels.map(s=>`<th>${s}</th>`).join('')}</tr></thead>`;
const tbody=document.createElement('tbody');
scorecardData.forEach(row=>{
  const tr=document.createElement('tr');
  tr.innerHTML=`<td style="color:#555;font-weight:400">${row.dim}</td>${row.vals.map(v=>`<td style="background:${hmCol(v)};color:#fff;border-radius:2px">${v}</td>`).join('')}`;
  tbody.appendChild(tr);
});
tbl.appendChild(tbody);

/* Supplier KPI cards — no labels, just the metric name and value */
const extMini=[
  {n:'Purchase Order Accuracy',v:'98.1%',col:'#2196F3',bar:98},
  {n:'Supplier Lead Time',v:'18.4 days',col:'#FF9800',bar:62},
  {n:'Vendor Fill Rate',v:'91.7%',col:'#4CAF50',bar:92},
  {n:'Collaboration Index',v:'82 / 100',col:'#2196F3',bar:82},
  {n:'Contract Compliance',v:'94.8%',col:'#4CAF50',bar:95},
  {n:'Ethical Sourcing Index',v:'88 / 100',col:'#4CAF50',bar:88},
  {n:'Innovation Contribution',v:'7.3 / 10',col:'#9C27B0',bar:73},
  {n:'Purchase Order Cycle Time',v:'4.2 days',col:'#FF9800',bar:78},
];
document.getElementById('ext-mini').innerHTML=extMini.map(k=>`
  <div style="background:#f8f9fa;border-radius:4px;padding:5px 8px;border-left:2px solid ${k.col}">
    <div style="font-size:8px;color:#777;margin-bottom:1px">${k.n}</div>
    <div style="font-size:13px;font-weight:700;color:#1a1a2e">${k.v}</div>
    <div style="height:2px;background:#eee;border-radius:1px;margin-top:4px">
      <div style="height:100%;width:${k.bar}%;background:${k.col};border-radius:1px"></div>
    </div>
  </div>`).join('');

/* SC cost — pie only, no warehouse data */
new Chart(document.getElementById('c-scost'),{
  type:'pie',
  data:{
    labels:['Procurement 49%','Transportation 41%','Warehousing 10%'],
    datasets:[{data:[49,41,10],backgroundColor:['#4CAF50','#2196F3','#F44336'],borderWidth:2,borderColor:'#fff'}]
  },
  options:{responsive:true,maintainAspectRatio:false,plugins:{legend:{display:false},tooltip:{callbacks:{label:c=>c.label}}}}
});

/* Supplier donuts */
const supAcc=[
  {name:'Aohai (OEM)',val:95,col:'#4CAF50'},
  {name:'Apex Wuxi ⚠',val:52,col:'#F44336'},
  {name:'Salcomp',val:91,col:'#8BC34A'},
  {name:'ATL (new)',val:97,col:'#4CAF50'},
];
const dg=document.getElementById('sup-donuts');
supAcc.forEach((s,i)=>{
  dg.innerHTML+=`<div class="sup-donut-card">
    <div class="sup-donut-title">${s.name} Accuracy</div>
    <div style="position:relative;height:90px"><canvas id="dn${i}"></canvas></div>
    <div class="sup-donut-val" style="color:${s.col}">${s.val}%</div>
  </div>`;
});
supAcc.forEach((s,i)=>{
  new Chart(document.getElementById('dn'+i),{
    type:'doughnut',
    data:{datasets:[{data:[s.val,100-s.val],backgroundColor:[s.col,'#e0e0e0'],borderWidth:0}]},
    options:{responsive:true,maintainAspectRatio:false,cutout:'70%',plugins:{legend:{display:false},tooltip:{enabled:false}}}
  });
});

/* Risk KPI cards — plain, no framework label */
const riskKpis=[
  {n:'Supplier Risk Score',v:'24 / 100',sub:'Apex Wuxi: 92 / 100 (critical)',col:'#F44336',bar:24},
  {n:'Supply Continuity Index',v:'76 / 100',sub:'Business continuity readiness',col:'#FF9800',bar:76},
  {n:'Downtime Recovery Time',v:'6.2 hrs',sub:'Average recovery after disruption',col:'#FF9800',bar:62},
  {n:'Emergency Purchase Ratio',v:'4.1%',sub:'Unplanned procurement share',col:'#F44336',bar:41},
  {n:'Procurement Policy Adherence',v:'97.3%',sub:'Internal & external compliance',col:'#4CAF50',bar:97},
  {n:'Compliance Rate',v:'96.2%',sub:'Product specification adherence',col:'#4CAF50',bar:96},
];
document.getElementById('risk-kpis').innerHTML=riskKpis.map(k=>`
  <div style="background:#fff;border:1px solid #e8eaf0;border-radius:6px;padding:.65rem .9rem;border-left:3px solid ${k.col}">
    <div style="font-size:9px;color:#666;margin-bottom:3px;font-weight:600">${k.n}</div>
    <div style="font-size:18px;font-weight:700;color:#1a1a2e">${k.v}</div>
    <div style="font-size:8px;color:#999;margin-top:2px">${k.sub}</div>
    <div style="height:3px;background:#eee;border-radius:2px;margin-top:6px">
      <div style="height:100%;width:${k.bar}%;background:${k.col};border-radius:2px"></div>
    </div>
  </div>`).join('');
</script>

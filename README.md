
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:var(--font-sans);background:var(--color-background-tertiary);color:var(--color-text-primary)}
.app{min-height:100vh;padding:0}
.topbar{background:var(--color-background-primary);border-bottom:0.5px solid var(--color-border-tertiary);padding:12px 20px;display:flex;align-items:center;justify-content:space-between;gap:12px;flex-wrap:wrap}
.topbar-left{display:flex;align-items:center;gap:10px}
.logo{width:32px;height:32px;background:#1F3864;border-radius:8px;display:flex;align-items:center;justify-content:center;flex-shrink:0}
.logo i{color:#fff;font-size:18px}
.app-title{font-size:16px;font-weight:500;color:var(--color-text-primary)}
.app-sub{font-size:12px;color:var(--color-text-secondary)}
.topbar-right{display:flex;align-items:center;gap:8px}
.btn{padding:7px 14px;border-radius:var(--border-radius-md);border:0.5px solid var(--color-border-secondary);background:var(--color-background-primary);color:var(--color-text-primary);font-size:13px;cursor:pointer;display:flex;align-items:center;gap:6px;transition:background 0.15s}
.btn:hover{background:var(--color-background-secondary)}
.btn-primary{background:#1F3864;color:#fff;border-color:#1F3864}
.btn-primary:hover{background:#162d54}
.badge-live{background:#E2EFDA;color:#375623;font-size:11px;padding:3px 8px;border-radius:20px;font-weight:500;display:flex;align-items:center;gap:4px}
.badge-live .dot{width:6px;height:6px;background:#375623;border-radius:50%;animation:pulse 2s infinite}
@keyframes pulse{0%,100%{opacity:1}50%{opacity:0.4}}
.tabs{display:flex;gap:0;border-bottom:0.5px solid var(--color-border-tertiary);background:var(--color-background-primary);padding:0 20px;overflow-x:auto}
.tab{padding:10px 16px;font-size:13px;cursor:pointer;border-bottom:2px solid transparent;white-space:nowrap;color:var(--color-text-secondary);display:flex;align-items:center;gap:6px;transition:all 0.15s}
.tab:hover{color:var(--color-text-primary)}
.tab.active{color:#1F3864;border-bottom-color:#1F3864;font-weight:500}
.tab-count{font-size:11px;padding:2px 7px;border-radius:20px;background:var(--color-background-secondary)}
.tab.active .tab-count{background:#1F3864;color:#fff}
.content{padding:16px 20px}
.kpi-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(140px,1fr));gap:10px;margin-bottom:16px}
.kpi{background:var(--color-background-primary);border:0.5px solid var(--color-border-tertiary);border-radius:var(--border-radius-lg);padding:12px 14px}
.kpi-label{font-size:11px;color:var(--color-text-secondary);margin-bottom:4px;text-transform:uppercase;letter-spacing:0.5px}
.kpi-value{font-size:26px;font-weight:500}
.kpi-sub{font-size:11px;color:var(--color-text-secondary);margin-top:2px}
.kpi.navy .kpi-value{color:#1F3864}
.kpi.red .kpi-value{color:#9C0006}
.kpi.green .kpi-value{color:#375623}
.kpi.orange .kpi-value{color:#C55A11}
.kpi.teal .kpi-value{color:#1F6391}
.kpi.brown .kpi-value{color:#833C00}
.section-head{display:flex;align-items:center;justify-content:space-between;margin-bottom:10px;flex-wrap:wrap;gap:8px}
.section-title{font-size:13px;font-weight:500;color:var(--color-text-primary)}
.filter-row{display:flex;gap:8px;align-items:center;flex-wrap:wrap}
.filter-row input,.filter-row select{font-size:12px;padding:5px 10px;border-radius:var(--border-radius-md);border:0.5px solid var(--color-border-secondary);background:var(--color-background-primary);color:var(--color-text-primary)}
.table-wrap{background:var(--color-background-primary);border:0.5px solid var(--color-border-tertiary);border-radius:var(--border-radius-lg);overflow:hidden}
table{width:100%;border-collapse:collapse;font-size:12px;table-layout:fixed}
th{background:var(--color-background-secondary);padding:8px 10px;text-align:left;font-weight:500;font-size:11px;color:var(--color-text-secondary);border-bottom:0.5px solid var(--color-border-tertiary);white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
td{padding:8px 10px;border-bottom:0.5px solid var(--color-border-tertiary);vertical-align:top;word-break:break-word;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
tr:last-child td{border-bottom:none}
tr:hover td{background:var(--color-background-secondary)}
.pill{display:inline-flex;align-items:center;font-size:11px;padding:2px 8px;border-radius:20px;font-weight:500;white-space:nowrap}
.pill-green{background:#C6EFCE;color:#375623}
.pill-red{background:#FFC7CE;color:#9C0006}
.pill-yellow{background:#FFEB9C;color:#9C5700}
.pill-blue{background:#DEEAF1;color:#1F6391}
.pill-orange{background:#FCE4D6;color:#C55A11}
.pill-navy{background:#D6DCE4;color:#1F3864}
.stage-bar{display:flex;gap:0;align-items:stretch;margin-bottom:14px}
.stage{flex:1;padding:8px 10px;font-size:11px;background:var(--color-background-secondary);border:0.5px solid var(--color-border-tertiary);position:relative;display:flex;flex-direction:column;gap:2px}
.stage:not(:last-child){border-right:none}
.stage:first-child{border-radius:var(--border-radius-md) 0 0 var(--border-radius-md)}
.stage:last-child{border-radius:0 var(--border-radius-md) var(--border-radius-md) 0}
.stage.active{background:#1F3864;border-color:#1F3864}
.stage.done{background:#E2EFDA;border-color:#A9D18E}
.stage.pending{background:#FFEB9C;border-color:#FFD966}
.stage-num{font-size:10px;font-weight:500;opacity:0.7}
.stage.active .stage-num,.stage.active .stage-name{color:#fff}
.stage.done .stage-num,.stage.done .stage-name{color:#375623}
.stage.pending .stage-name{color:#9C5700}
.stage-name{font-size:11px;font-weight:500}
.empty-state{text-align:center;padding:40px 20px;color:var(--color-text-secondary)}
.empty-state i{font-size:36px;display:block;margin-bottom:8px;opacity:0.4}
.loading-box{text-align:center;padding:40px 20px;color:var(--color-text-secondary)}
.loading-box i{font-size:32px;display:block;margin-bottom:8px;opacity:0.5;animation:spin 1.2s linear infinite}
@keyframes spin{from{transform:rotate(0deg)}to{transform:rotate(360deg)}}
.error-box{background:#FCE4D6;border:0.5px solid #F4B183;border-radius:var(--border-radius-lg);padding:16px 20px;margin-bottom:14px;font-size:13px;color:#C55A11}
.detail-panel{background:var(--color-background-primary);border:0.5px solid var(--color-border-tertiary);border-radius:var(--border-radius-lg);padding:16px;margin-top:12px}
.detail-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.detail-field{display:flex;flex-direction:column;gap:2px}
.detail-label{font-size:10px;color:var(--color-text-secondary);text-transform:uppercase;letter-spacing:0.4px}
.detail-value{font-size:13px;color:var(--color-text-primary)}
.approval-chain{margin-top:12px}
.stage-row{display:flex;gap:12px;align-items:flex-start;margin-bottom:16px;position:relative}
.stage-row:not(:last-child)::before{content:'';position:absolute;left:15px;top:32px;width:1px;height:calc(100% - 8px);background:var(--color-border-tertiary)}
.stage-icon{width:30px;height:30px;border-radius:50%;display:flex;align-items:center;justify-content:center;flex-shrink:0;font-size:14px}
.stage-icon.done-icon{background:#C6EFCE;color:#375623}
.stage-icon.active-icon{background:#1F3864;color:#fff}
.stage-icon.waiting-icon{background:var(--color-background-secondary);color:var(--color-text-secondary)}
.stage-info{flex:1}
.stage-info-title{font-size:13px;font-weight:500}
.stage-info-sub{font-size:11px;color:var(--color-text-secondary);margin-top:2px}
.input-row{display:flex;gap:8px;align-items:center;margin-top:8px;flex-wrap:wrap}
.input-row input{font-size:12px;padding:5px 10px;border-radius:var(--border-radius-md);border:0.5px solid var(--color-border-secondary);background:var(--color-background-primary);color:var(--color-text-primary);width:140px}
.input-row .btn{font-size:12px;padding:5px 12px}
.refresh-info{font-size:11px;color:var(--color-text-secondary);display:flex;align-items:center;gap:4px}
</style>

<div class="app">
<div class="topbar">
  <div class="topbar-left">
    <div class="logo"><i class="ti ti-ambulance" aria-hidden="true"></i></div>
    <div>
      <div class="app-title">Fleet Maintenance Tracker</div>
      <div class="app-sub">Live from Google Sheet</div>
    </div>
  </div>
  <div class="topbar-right">
    <div class="badge-live"><span class="dot"></span><span id="sync-label">Connecting...</span></div>
    <button class="btn" onclick="fetchData()"><i class="ti ti-refresh" aria-hidden="true"></i> Refresh</button>
  </div>
</div>

<div class="tabs">
  <div class="tab active" onclick="switchTab('dashboard',this)"><i class="ti ti-layout-dashboard" aria-hidden="true"></i> Dashboard</div>
  <div class="tab" onclick="switchTab('direct',this)"><i class="ti ti-check" aria-hidden="true"></i> Direct Approval <span class="tab-count" id="cnt-direct">0</span></div>
  <div class="tab" onclick="switchTab('chain',this)"><i class="ti ti-git-merge" aria-hidden="true"></i> Full Chain <span class="tab-count" id="cnt-chain">0</span></div>
  <div class="tab" onclick="switchTab('all',this)"><i class="ti ti-list" aria-hidden="true"></i> All Records <span class="tab-count" id="cnt-all">0</span></div>
</div>

<div class="content">
  <div id="error-area"></div>
  <div id="tab-dashboard"></div>
  <div id="tab-direct" style="display:none"></div>
  <div id="tab-chain" style="display:none"></div>
  <div id="tab-all" style="display:none"></div>
</div>
</div>

<script>
const SHEET_ID = "1mGR2yWWCqq1nVV6Bps58NL5B10ZMdfaql-2VFywyX94";
const approvalData = {};
let allRows = [];
let activeTab = "dashboard";
let selectedRow = null;

function switchTab(tab, el) {
  activeTab = tab;
  document.querySelectorAll(".tab").forEach(t => t.classList.remove("active"));
  el.classList.add("active");
  ["dashboard","direct","chain","all"].forEach(t => {
    document.getElementById("tab-"+t).style.display = t===tab ? "block" : "none";
  });
  if (allRows.length) renderTab(tab);
}

async function fetchData() {
  document.getElementById("sync-label").textContent = "Syncing...";
  document.getElementById("error-area").innerHTML = "";
  const url = `https://docs.google.com/spreadsheets/d/${SHEET_ID}/gviz/tq?tqx=out:csv&sheet=Sheet1`;
  try {
    const res = await fetch(url);
    if (!res.ok) throw new Error("HTTP " + res.status);
    const text = await res.text();
    parseCSV(text);
    document.getElementById("sync-label").textContent = "Live · " + new Date().toLocaleTimeString("en-IN",{hour:"2-digit",minute:"2-digit"});
  } catch(e) {
    document.getElementById("sync-label").textContent = "Offline";
    document.getElementById("error-area").innerHTML = `
      <div class="error-box">
        <strong><i class="ti ti-alert-circle" aria-hidden="true"></i> Cannot reach Google Sheet.</strong><br>
        Make sure your sheet is shared as "Anyone with the link can view", then click Refresh.
        <br><small style="opacity:0.8">Error: ${e.message}</small>
      </div>`;
    if (!allRows.length) showOfflineDemo();
  }
}

function parseCSV(text) {
  const lines = text.trim().split("\n");
  if (lines.length < 2) return;
  const headers = parseCSVLine(lines[0]).map(h => h.toLowerCase().trim());
  allRows = [];
  for (let i = 1; i < lines.length; i++) {
    const vals = parseCSVLine(lines[i]);
    if (!vals.length || vals.every(v => !v.trim())) continue;
    const row = {};
    headers.forEach((h, idx) => { row[h] = (vals[idx] || "").replace(/^"|"$/g,"").trim(); });
    // Map known fields
    const r = {
      id: row["row_id"] || row["id"] || ("ROW_"+i),
      wrNo: row["wr no"] || row["wrno"] || row["wr_no"] || ("WR-"+String(i).padStart(3,"0")),
      date: row["date"] || "",
      regno: row["regno"] || row["reg no"] || row["vehicle reg"] || "",
      cluster: row["cluster"] || "",
      district: row["district"] || "",
      make: row["make"] || "",
      model: row["model"] || "",
      complaint: row["complaint"] || "",
      action: row["action"] || "",
      workshop: row["workshop"] || "",
      status: row["status"] || "",
      estimate: parseFloat(row["estimate"] || row["estimate ₹"] || "0") || 0,
      invoice: parseFloat(row["invoice"] || row["invoice ₹"] || "0") || 0,
      towing: row["towing"] || "",
      towvendor: row["towvendor"] || row["tow vendor"] || "",
      bddate: row["bddate"] || row["bd date"] || row["breakdown date"] || "",
      bdtime: row["bdtime"] || row["bd time"] || row["breakdown time"] || "",
      odo: row["odo"] || row["odometer"] || "",
      approval: row["approval"] || "",
      advance: row["advance"] || "",
      negotiated: row["negotiated"] || "",
      remarks: row["remarks"] || "",
      raw: row
    };
    r.route = r.estimate > 3000 ? "chain" : (r.estimate > 0 ? "direct" : "direct");
    if (!approvalData[r.id]) approvalData[r.id] = { fleetDate:"", fleetTime:"", fleetBy:"", purchMailDate:"", purchMailTime:"", purchApprDate:"", purchApprTime:"", commMailDate:"", commMailTime:"", commApprDate:"", commApprTime:"", finalMailDate:"", finalMailTime:"", fieldMailDate:"", fieldMailTime:"", fieldBy:"" };
    allRows.push(r);
  }
  updateCounts();
  renderTab(activeTab);
}

function parseCSVLine(line) {
  const result = []; let cur = ""; let inQ = false;
  for (let i = 0; i < line.length; i++) {
    if (line[i] === '"') { inQ = !inQ; }
    else if (line[i] === ',' && !inQ) { result.push(cur); cur = ""; }
    else { cur += line[i]; }
  }
  result.push(cur);
  return result;
}

function showOfflineDemo() {
  allRows = [
    {id:"demo1",wrNo:"WR-001",date:"07/06/2026",regno:"MH14CL1312",cluster:"C2",district:"Pune",make:"Force",model:"Traveller",complaint:"Link Damage",action:"Taken",workshop:"",status:"On Road",estimate:1500,invoice:1500,towing:"No",towvendor:"",bddate:"07/06/2026",bdtime:"",odo:"1400",approval:"Approved",advance:"0",negotiated:"",remarks:"Approved",route:"direct",raw:{}},
    {id:"demo2",wrNo:"WR-002",date:"08/06/2026",regno:"MH14CL0981",cluster:"C5",district:"Pune",make:"",model:"",complaint:"Crown pinion & assy damage",action:"",workshop:"Milan motors",status:"Off Road",estimate:24724,invoice:0,towing:"Yes",towvendor:"New Ganesh Crane",bddate:"08/06/2026",bdtime:"",odo:"740478",approval:"Pending",advance:"0",negotiated:"",remarks:"",route:"chain",raw:{}},
    {id:"demo3",wrNo:"WR-003",date:"08/06/2026",regno:"MH14CL1208",cluster:"C5",district:"Pune",make:"Leyland",model:"Dost",complaint:"Radiator coolant leakage",action:"Hose & pipe changed",workshop:"Local Garage",status:"On Road",estimate:850,invoice:840,towing:"No",towvendor:"",bddate:"08/06/2026",bdtime:"",odo:"576959",approval:"Closed",advance:"0",negotiated:"",remarks:"",route:"direct",raw:{}},
    {id:"demo4",wrNo:"WR-004",date:"08/06/2026",regno:"MH14CL0674",cluster:"C3",district:"Thane",make:"Force",model:"Traveller",complaint:"Center bearing out, leaf spring",action:"Waiting",workshop:"Mumbai Nashik Hwy",status:"Off Road",estimate:9460,invoice:0,towing:"No",towvendor:"",bddate:"08/06/2026",bdtime:"13:44",odo:"90830",approval:"Pending",advance:"0",negotiated:"",remarks:"",route:"chain",raw:{}},
    {id:"demo5",wrNo:"WR-005",date:"08/06/2026",regno:"MH14CL1358",cluster:"C3",district:"Thane",make:"Ashok Leyland",model:"Dost",complaint:"Front Hub, Brake caliper, Disc rotor",action:"",workshop:"Shubham Motor Garage",status:"Off Road",estimate:16720,invoice:0,towing:"No",towvendor:"",bddate:"08/06/2026",bdtime:"16:45",odo:"284887",approval:"Pending",advance:"0",negotiated:"",remarks:"",route:"chain",raw:{}},
    {id:"demo6",wrNo:"WR-006",date:"08/06/2026",regno:"MH14CL1326",cluster:"C6",district:"Pune",make:"Force",model:"Traveller",complaint:"Shock absorber bolt loose",action:"Moved to nearest garage",workshop:"",status:"On Road",estimate:600,invoice:600,towing:"No",towvendor:"",bddate:"08/06/2026",bdtime:"",odo:"",approval:"Closed",advance:"0",negotiated:"",remarks:"",route:"direct",raw:{}},
  ];
  allRows.forEach(r => { if (!approvalData[r.id]) approvalData[r.id] = {}; });
  updateCounts(); renderTab(activeTab);
}

function updateCounts() {
  const direct = allRows.filter(r => r.route === "direct");
  const chain  = allRows.filter(r => r.route === "chain");
  document.getElementById("cnt-direct").textContent = direct.length;
  document.getElementById("cnt-chain").textContent  = chain.length;
  document.getElementById("cnt-all").textContent    = allRows.length;
}

function statusPill(s) {
  if (!s) return "";
  if (s==="On Road"||s==="Closed") return `<span class="pill pill-green">${s}</span>`;
  if (s==="Off Road") return `<span class="pill pill-red">${s}</span>`;
  if (s==="Pending") return `<span class="pill pill-yellow">${s}</span>`;
  return `<span class="pill pill-blue">${s}</span>`;
}
function routePill(r) {
  return r==="chain"
    ? `<span class="pill pill-orange">Full Chain &gt;₹3K</span>`
    : `<span class="pill pill-green">Direct ≤₹3K</span>`;
}
function fmt(n) { return n ? "₹"+Number(n).toLocaleString("en-IN") : "—"; }

function renderTab(tab) {
  if (tab==="dashboard") renderDashboard();
  else if (tab==="direct") renderDirect();
  else if (tab==="chain") renderChain();
  else if (tab==="all") renderAll();
}

function renderDashboard() {
  const total  = allRows.length;
  const offRd  = allRows.filter(r=>r.status==="Off Road").length;
  const onRd   = allRows.filter(r=>r.status==="On Road"||r.status==="Closed").length;
  const pend   = allRows.filter(r=>r.status==="Pending").length;
  const direct = allRows.filter(r=>r.route==="direct").length;
  const chain  = allRows.filter(r=>r.route==="chain").length;
  const totalEst = allRows.reduce((a,r)=>a+(r.estimate||0),0);
  const pendAmt  = allRows.filter(r=>r.status==="Pending"||r.status==="Off Road").reduce((a,r)=>a+(r.estimate||0),0);

  const recent = [...allRows].reverse().slice(0,8);
  const recentRows = recent.map(r => `
    <tr>
      <td style="font-weight:500">${r.wrNo}</td>
      <td>${r.regno}</td>
      <td>${r.district}</td>
      <td style="max-width:160px;overflow:hidden;text-overflow:ellipsis">${r.complaint}</td>
      <td>${fmt(r.estimate)}</td>
      <td>${statusPill(r.status)}</td>
      <td>${routePill(r.route)}</td>
    </tr>`).join("");

  document.getElementById("tab-dashboard").innerHTML = `
    <div class="kpi-grid">
      <div class="kpi navy"><div class="kpi-label">Total Requests</div><div class="kpi-value">${total}</div><div class="kpi-sub">All time</div></div>
      <div class="kpi red"><div class="kpi-label">Off Road</div><div class="kpi-value">${offRd}</div><div class="kpi-sub">Vehicles down</div></div>
      <div class="kpi green"><div class="kpi-label">On Road</div><div class="kpi-value">${onRd}</div><div class="kpi-sub">Running</div></div>
      <div class="kpi orange"><div class="kpi-label">Pending</div><div class="kpi-value">${pend}</div><div class="kpi-sub">Awaiting action</div></div>
      <div class="kpi teal"><div class="kpi-label">Direct ≤₹3K</div><div class="kpi-value">${direct}</div><div class="kpi-sub">Fleet desk only</div></div>
      <div class="kpi brown"><div class="kpi-label">Full Chain &gt;₹3K</div><div class="kpi-value">${chain}</div><div class="kpi-sub">Multi-approval</div></div>
    </div>
    <div class="kpi-grid" style="grid-template-columns:1fr 1fr;margin-bottom:16px">
      <div class="kpi navy"><div class="kpi-label">Total Estimated Cost</div><div class="kpi-value" style="font-size:20px">₹${totalEst.toLocaleString("en-IN")}</div></div>
      <div class="kpi red"><div class="kpi-label">Pending Amount</div><div class="kpi-value" style="font-size:20px">₹${pendAmt.toLocaleString("en-IN")}</div></div>
    </div>
    <div class="section-head"><div class="section-title">Recent Requests</div></div>
    <div class="table-wrap">
      <table>
        <thead><tr><th style="width:80px">WR No</th><th style="width:110px">Vehicle</th><th style="width:80px">District</th><th>Complaint</th><th style="width:90px">Estimate</th><th style="width:90px">Status</th><th style="width:110px">Route</th></tr></thead>
        <tbody>${recentRows || '<tr><td colspan="7" style="text-align:center;color:var(--color-text-secondary);padding:24px">No data yet</td></tr>'}</tbody>
      </table>
    </div>`;
}

function renderDirect() {
  const rows = allRows.filter(r => r.route === "direct");
  const filterHtml = `<div class="section-head">
    <div class="section-title">Direct Approval — Estimate ≤ ₹3,000 (Fleet Desk Only)</div>
    <div class="filter-row">
      <input id="f-direct" placeholder="Search..." oninput="filterDirect()" style="width:160px">
      <select id="s-direct" onchange="filterDirect()">
        <option value="">All Status</option>
        <option>On Road</option><option>Off Road</option><option>Pending</option><option>Closed</option>
      </select>
    </div>
  </div>`;
  document.getElementById("tab-direct").innerHTML = filterHtml + `<div id="direct-table"></div>`;
  renderDirectTable(rows);
}

function filterDirect() {
  const q = document.getElementById("f-direct").value.toLowerCase();
  const s = document.getElementById("s-direct").value;
  let rows = allRows.filter(r => r.route==="direct");
  if (q) rows = rows.filter(r => (r.wrNo+r.regno+r.complaint+r.district).toLowerCase().includes(q));
  if (s) rows = rows.filter(r => r.status===s);
  renderDirectTable(rows);
}

function renderDirectTable(rows) {
  if (!rows.length) { document.getElementById("direct-table").innerHTML = `<div class="empty-state"><i class="ti ti-check" aria-hidden="true"></i>No direct approval records</div>`; return; }
  const tbody = rows.map(r => {
    const ad = approvalData[r.id] || {};
    const stagesDone = (ad.fleetDate?"✔ Fleet":"") + (ad.fieldMailDate?" → ✔ Notified":"");
    const rowClass = !ad.fleetDate && r.estimate>0 ? "style='background:#FFFBEB'" : (ad.fieldMailDate ? "style='background:#F0FFF4'" : "");
    return `<tr ${rowClass} onclick="openDetail('${r.id}')" style="${(rowClass||"") + "cursor:pointer"}">
      <td style="font-weight:500">${r.wrNo}</td>
      <td>${r.regno}</td>
      <td>${r.district}</td>
      <td style="max-width:140px;overflow:hidden;text-overflow:ellipsis">${r.complaint}</td>
      <td style="color:#C55A11;font-weight:500">${fmt(r.estimate)}</td>
      <td>${statusPill(r.status)}</td>
      <td>${ad.fleetDate ? `<span class="pill pill-green">Approved ${ad.fleetDate}</span>` : `<span class="pill pill-yellow">Pending</span>`}</td>
      <td>${ad.fieldMailDate ? `<span class="pill pill-blue">Notified</span>` : `<span class="pill" style="background:var(--color-background-secondary)">—</span>`}</td>
    </tr>`;
  }).join("");
  document.getElementById("direct-table").innerHTML = `
    <div class="table-wrap">
      <table>
        <thead><tr>
          <th style="width:80px">WR No</th><th style="width:110px">Vehicle</th><th style="width:80px">District</th>
          <th>Complaint</th><th style="width:90px">Estimate</th><th style="width:90px">Status</th>
          <th style="width:130px">Fleet Approval</th><th style="width:90px">Field Notified</th>
        </tr></thead>
        <tbody>${tbody}</tbody>
      </table>
    </div>
    <div style="font-size:11px;color:var(--color-text-secondary);margin-top:6px"><i class="ti ti-click" aria-hidden="true"></i> Click any row to fill approval details</div>
    ${selectedRow && approvalData[selectedRow] ? renderDetailPanel(selectedRow) : ""}`;
}

function renderChain() {
  const rows = allRows.filter(r => r.route === "chain");
  const filterHtml = `<div class="section-head">
    <div class="section-title">Full Approval Chain — Estimate > ₹3,000</div>
    <div class="filter-row">
      <input id="f-chain" placeholder="Search..." oninput="filterChain()" style="width:160px">
      <select id="s-chain" onchange="filterChain()">
        <option value="">All Status</option>
        <option>On Road</option><option>Off Road</option><option>Pending</option><option>Closed</option>
      </select>
    </div>
  </div>`;
  document.getElementById("tab-chain").innerHTML = filterHtml + `<div id="chain-table"></div>`;
  renderChainTable(rows);
}

function filterChain() {
  const q = document.getElementById("f-chain").value.toLowerCase();
  const s = document.getElementById("s-chain").value;
  let rows = allRows.filter(r => r.route==="chain");
  if (q) rows = rows.filter(r => (r.wrNo+r.regno+r.complaint+r.district).toLowerCase().includes(q));
  if (s) rows = rows.filter(r => r.status===s);
  renderChainTable(rows);
}

function getChainStage(id) {
  const ad = approvalData[id] || {};
  if (!ad.fleetDate) return 1;
  if (!ad.purchApprDate) return 2;
  if (!ad.commApprDate) return 3;
  if (!ad.finalMailDate) return 4;
  return 5;
}

function renderChainTable(rows) {
  if (!rows.length) { document.getElementById("chain-table").innerHTML = `<div class="empty-state"><i class="ti ti-git-merge" aria-hidden="true"></i>No full-chain records</div>`; return; }
  const stageColors = ["","style='background:#FFC7CE'","style='background:#FFEB9C'","style='background:#FFF2CC'","style='background:#DEEAF1'","style='background:#E2EFDA'"];
  const stageLabels = ["","Stage 1: Pending Fleet","Stage 2: Fleet Done, Awaiting Purchase","Stage 3: Purchase Done, Awaiting Commercial","Stage 4: Commercial Done, Final Mail Pending","Stage 5: Fully Approved"];
  const tbody = rows.map(r => {
    const st = getChainStage(r.id);
    return `<tr ${stageColors[st]} onclick="openDetail('${r.id}')" style="cursor:pointer">
      <td style="font-weight:500">${r.wrNo}</td>
      <td>${r.regno}</td>
      <td>${r.district}</td>
      <td style="max-width:120px;overflow:hidden;text-overflow:ellipsis">${r.complaint}</td>
      <td style="color:#C55A11;font-weight:500">${fmt(r.estimate)}</td>
      <td>${statusPill(r.status)}</td>
      <td><span class="pill ${st===5?"pill-green":st>=3?"pill-blue":"pill-yellow"}">${stageLabels[st]}</span></td>
    </tr>`;
  }).join("");
  document.getElementById("chain-table").innerHTML = `
    <div class="stage-bar">
      <div class="stage"><div class="stage-num">Stage 1</div><div class="stage-name">Field Raises</div></div>
      <div class="stage"><div class="stage-num">Stage 2</div><div class="stage-name">Fleet Desk</div></div>
      <div class="stage"><div class="stage-num">Stage 3</div><div class="stage-name">Purchase</div></div>
      <div class="stage"><div class="stage-num">Stage 4</div><div class="stage-name">Commercial</div></div>
      <div class="stage"><div class="stage-num">Stage 5</div><div class="stage-name">Final Mail</div></div>
    </div>
    <div class="table-wrap">
      <table>
        <thead><tr>
          <th style="width:80px">WR No</th><th style="width:110px">Vehicle</th><th style="width:80px">District</th>
          <th>Complaint</th><th style="width:90px">Estimate</th><th style="width:90px">Status</th>
          <th>Approval Stage</th>
        </tr></thead>
        <tbody>${tbody}</tbody>
      </table>
    </div>
    <div style="font-size:11px;color:var(--color-text-secondary);margin-top:6px"><i class="ti ti-click" aria-hidden="true"></i> Click any row to update approval stages</div>
    ${selectedRow && approvalData[selectedRow] ? renderDetailPanel(selectedRow) : ""}`;
}

function renderAll() {
  const filterHtml = `<div class="section-head">
    <div class="section-title">All Records</div>
    <div class="filter-row">
      <input id="f-all" placeholder="Search..." oninput="filterAll()" style="width:160px">
      <select id="s-all" onchange="filterAll()">
        <option value="">All Status</option>
        <option>On Road</option><option>Off Road</option><option>Pending</option><option>Closed</option>
      </select>
      <select id="r-all" onchange="filterAll()">
        <option value="">All Routes</option>
        <option value="direct">Direct ≤₹3K</option>
        <option value="chain">Full Chain &gt;₹3K</option>
      </select>
    </div>
  </div>`;
  document.getElementById("tab-all").innerHTML = filterHtml + `<div id="all-table"></div>`;
  renderAllTable(allRows);
}

function filterAll() {
  const q = document.getElementById("f-all").value.toLowerCase();
  const s = document.getElementById("s-all").value;
  const rt= document.getElementById("r-all").value;
  let rows = allRows;
  if (q) rows = rows.filter(r => (r.wrNo+r.regno+r.complaint+r.district+r.make+r.model).toLowerCase().includes(q));
  if (s) rows = rows.filter(r => r.status===s);
  if (rt) rows = rows.filter(r => r.route===rt);
  renderAllTable(rows);
}

function renderAllTable(rows) {
  if (!rows.length) { document.getElementById("all-table").innerHTML = `<div class="empty-state"><i class="ti ti-list" aria-hidden="true"></i>No records found</div>`; return; }
  const tbody = rows.map(r => `<tr onclick="openDetail('${r.id}')" style="cursor:pointer">
    <td style="font-weight:500">${r.wrNo}</td>
    <td>${r.date}</td>
    <td>${r.regno}</td>
    <td>${r.district}</td>
    <td style="max-width:120px;overflow:hidden;text-overflow:ellipsis">${r.complaint}</td>
    <td>${fmt(r.estimate)}</td>
    <td>${statusPill(r.status)}</td>
    <td>${routePill(r.route)}</td>
  </tr>`).join("");
  document.getElementById("all-table").innerHTML = `
    <div class="table-wrap">
      <table>
        <thead><tr>
          <th style="width:80px">WR No</th><th style="width:90px">Date</th><th style="width:110px">Vehicle</th>
          <th style="width:80px">District</th><th>Complaint</th><th style="width:90px">Estimate</th>
          <th style="width:90px">Status</th><th style="width:110px">Route</th>
        </tr></thead>
        <tbody>${tbody}</tbody>
      </table>
    </div>`;
}

function openDetail(id) {
  selectedRow = id;
  renderTab(activeTab);
  setTimeout(() => {
    const dp = document.getElementById("detail-panel-"+id);
    if (dp) dp.scrollIntoView({behavior:"smooth",block:"nearest"});
  }, 100);
}

function renderDetailPanel(id) {
  const r = allRows.find(x => x.id===id);
  if (!r) return "";
  const ad = approvalData[id] || {};

  if (r.route === "direct") {
    return `<div class="detail-panel" id="detail-panel-${id}">
      <div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:12px">
        <div style="font-size:14px;font-weight:500">${r.wrNo} — ${r.regno} — ${r.complaint}</div>
        <button class="btn" onclick="selectedRow=null;renderTab(activeTab)" style="font-size:11px;padding:4px 10px"><i class="ti ti-x" aria-hidden="true"></i></button>
      </div>
      <div class="detail-grid" style="margin-bottom:14px">
        <div class="detail-field"><div class="detail-label">District</div><div class="detail-value">${r.district}</div></div>
        <div class="detail-field"><div class="detail-label">Breakdown Date</div><div class="detail-value">${r.bddate} ${r.bdtime}</div></div>
        <div class="detail-field"><div class="detail-label">Workshop</div><div class="detail-value">${r.workshop||"—"}</div></div>
        <div class="detail-field"><div class="detail-label">Estimate</div><div class="detail-value" style="color:#C55A11;font-weight:500">${fmt(r.estimate)}</div></div>
      </div>
      <div class="approval-chain">
        <div class="stage-row">
          <div class="stage-icon done-icon"><i class="ti ti-send" aria-hidden="true"></i></div>
          <div class="stage-info">
            <div class="stage-info-title">Stage 1 — Field raised request</div>
            <div class="stage-info-sub">${r.bddate} ${r.bdtime}</div>
            <div class="input-row">
              <input placeholder="Raised by (name)" value="${ad.fieldBy||""}" onchange="save('${id}','fieldBy',this.value)" >
            </div>
          </div>
        </div>
        <div class="stage-row">
          <div class="stage-icon ${ad.fleetDate?"done-icon":"active-icon"}"><i class="ti ti-${ad.fleetDate?"check":"clock"}" aria-hidden="true"></i></div>
          <div class="stage-info">
            <div class="stage-info-title">Stage 2 — Fleet Desk Approval</div>
            <div class="stage-info-sub">${ad.fleetDate ? "Approved: "+ad.fleetDate+" "+ad.fleetTime : "Pending your input"}</div>
            <div class="input-row">
              <input type="date" value="${ad.fleetDate||""}" onchange="save('${id}','fleetDate',this.value)" >
              <input type="time" value="${ad.fleetTime||""}" onchange="save('${id}','fleetTime',this.value)" >
              <input placeholder="Approved by" value="${ad.fleetBy||""}" onchange="save('${id}','fleetBy',this.value)" >
            </div>
          </div>
        </div>
        <div class="stage-row">
          <div class="stage-icon ${ad.fieldMailDate?"done-icon":"waiting-icon"}"><i class="ti ti-mail" aria-hidden="true"></i></div>
          <div class="stage-info">
            <div class="stage-info-title">Stage 3 — Notify Field (Mail Sent)</div>
            <div class="stage-info-sub">${ad.fieldMailDate ? "Sent: "+ad.fieldMailDate+" "+ad.fieldMailTime : "Pending"}</div>
            <div class="input-row">
              <input type="date" value="${ad.fieldMailDate||""}" onchange="save('${id}','fieldMailDate',this.value)" >
              <input type="time" value="${ad.fieldMailTime||""}" onchange="save('${id}','fieldMailTime',this.value)" >
            </div>
          </div>
        </div>
      </div>
    </div>`;
  } else {
    const st = getChainStage(id);
    return `<div class="detail-panel" id="detail-panel-${id}">
      <div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:12px">
        <div style="font-size:14px;font-weight:500">${r.wrNo} — ${r.regno} — ${r.complaint}</div>
        <button class="btn" onclick="selectedRow=null;renderTab(activeTab)" style="font-size:11px;padding:4px 10px"><i class="ti ti-x" aria-hidden="true"></i></button>
      </div>
      <div class="detail-grid" style="margin-bottom:14px">
        <div class="detail-field"><div class="detail-label">District</div><div class="detail-value">${r.district}</div></div>
        <div class="detail-field"><div class="detail-label">Breakdown Date/Time</div><div class="detail-value">${r.bddate} ${r.bdtime}</div></div>
        <div class="detail-field"><div class="detail-label">Workshop</div><div class="detail-value">${r.workshop||"—"}</div></div>
        <div class="detail-field"><div class="detail-label">Estimate</div><div class="detail-value" style="color:#C55A11;font-weight:500">${fmt(r.estimate)}</div></div>
      </div>
      <div class="approval-chain">
        <div class="stage-row">
          <div class="stage-icon done-icon"><i class="ti ti-send" aria-hidden="true"></i></div>
          <div class="stage-info">
            <div class="stage-info-title">Stage 1 — Field raises request</div>
            <div class="stage-info-sub">${r.bddate} ${r.bdtime}</div>
            <div class="input-row"><input placeholder="Raised by" value="${ad.fieldBy||""}" onchange="save('${id}','fieldBy',this.value)"></div>
          </div>
        </div>
        <div class="stage-row">
          <div class="stage-icon ${st>1?"done-icon":st===1?"active-icon":"waiting-icon"}"><i class="ti ti-${st>1?"check":"clock"}" aria-hidden="true"></i></div>
          <div class="stage-info">
            <div class="stage-info-title">Stage 2 — Fleet Desk Reviews</div>
            <div class="stage-info-sub">${ad.fleetDate?"Reviewed: "+ad.fleetDate+" "+ad.fleetTime:"Pending"}</div>
            <div class="input-row">
              <input type="date" value="${ad.fleetDate||""}" onchange="save('${id}','fleetDate',this.value)">
              <input type="time" value="${ad.fleetTime||""}" onchange="save('${id}','fleetTime',this.value)">
              <input placeholder="Reviewed by" value="${ad.fleetBy||""}" onchange="save('${id}','fleetBy',this.value)">
            </div>
          </div>
        </div>
        <div class="stage-row">
          <div class="stage-icon ${st>2?"done-icon":st===2?"active-icon":"waiting-icon"}"><i class="ti ti-mail-forward" aria-hidden="true"></i></div>
          <div class="stage-info">
            <div class="stage-info-title">Stage 3 — Purchase Dept (Email sent + Approved)</div>
            <div class="stage-info-sub">${ad.purchApprDate?"Approved: "+ad.purchApprDate+" "+ad.purchApprTime:"Pending"}</div>
            <div class="input-row">
              <input type="date" placeholder="Mail sent date" value="${ad.purchMailDate||""}" onchange="save('${id}','purchMailDate',this.value)">
              <input type="time" value="${ad.purchMailTime||""}" onchange="save('${id}','purchMailTime',this.value)">
            </div>
            <div class="input-row">
              <input type="date" placeholder="Approval date" value="${ad.purchApprDate||""}" onchange="save('${id}','purchApprDate',this.value)">
              <input type="time" value="${ad.purchApprTime||""}" onchange="save('${id}','purchApprTime',this.value)">
            </div>
          </div>
        </div>
        <div class="stage-row">
          <div class="stage-icon ${st>3?"done-icon":st===3?"active-icon":"waiting-icon"}"><i class="ti ti-mail-forward" aria-hidden="true"></i></div>
          <div class="stage-info">
            <div class="stage-info-title">Stage 4 — Commercial Dept (Email sent + Approved)</div>
            <div class="stage-info-sub">${ad.commApprDate?"Approved: "+ad.commApprDate+" "+ad.commApprTime:"Pending"}</div>
            <div class="input-row">
              <input type="date" placeholder="Mail sent date" value="${ad.commMailDate||""}" onchange="save('${id}','commMailDate',this.value)">
              <input type="time" value="${ad.commMailTime||""}" onchange="save('${id}','commMailTime',this.value)">
            </div>
            <div class="input-row">
              <input type="date" placeholder="Approval date" value="${ad.commApprDate||""}" onchange="save('${id}','commApprDate',this.value)">
              <input type="time" value="${ad.commApprTime||""}" onchange="save('${id}','commApprTime',this.value)">
            </div>
          </div>
        </div>
        <div class="stage-row">
          <div class="stage-icon ${st>=5?"done-icon":st===4?"active-icon":"waiting-icon"}"><i class="ti ti-mail" aria-hidden="true"></i></div>
          <div class="stage-info">
            <div class="stage-info-title">Stage 5 — Fleet Desk sends final mail to Field</div>
            <div class="stage-info-sub">${ad.finalMailDate?"Sent: "+ad.finalMailDate+" "+ad.finalMailTime:"Pending — send after Purchase + Commercial both approved"}</div>
            <div class="input-row">
              <input type="date" value="${ad.finalMailDate||""}" onchange="save('${id}','finalMailDate',this.value)">
              <input type="time" value="${ad.finalMailTime||""}" onchange="save('${id}','finalMailTime',this.value)">
            </div>
          </div>
        </div>
      </div>
    </div>`;
  }
}

function save(id, field, value) {
  if (!approvalData[id]) approvalData[id] = {};
  approvalData[id][field] = value;
  saveToStorage();
}

async function saveToStorage() {
  try { await window.storage.set("fleet_approvals", JSON.stringify(approvalData)); } catch(e) {}
}

async function loadFromStorage() {
  try {
    const r = await window.storage.get("fleet_approvals");
    if (r && r.value) {
      const saved = JSON.parse(r.value);
      Object.assign(approvalData, saved);
    }
  } catch(e) {}
}

async function init() {
  await loadFromStorage();
  await fetchData();
  setInterval(fetchData, 60000);
}

init();
</script>

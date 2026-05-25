
<style>
@import url('https://fonts.googleapis.com/css2?family=Sora:wght@300;400;500;600&family=JetBrains+Mono:wght@400;500&display=swap');
*{margin:0;padding:0;box-sizing:border-box}
:root{
  --bg:#0d1117;--bg2:#161b22;--bg3:#21262d;
  --border:#30363d;--border2:#484f58;
  --text:#e6edf3;--text2:#8b949e;--text3:#656d76;
  --green:#3fb950;--blue:#58a6ff;--purple:#bc8cff;
  --orange:#ffa657;--pink:#f778ba;--teal:#39d353;
}
body{background:var(--bg);font-family:'Sora',sans-serif;color:var(--text);padding:2rem 1rem;min-height:100vh}
.wrapper{max-width:860px;margin:0 auto}

.profile-header{display:grid;grid-template-columns:auto 1fr;gap:2rem;align-items:start;margin-bottom:2rem}
.avatar-wrap{position:relative;width:88px;height:88px}
.avatar{width:88px;height:88px;border-radius:50%;background:linear-gradient(135deg,#3fb950,#58a6ff,#bc8cff);display:flex;align-items:center;justify-content:center;font-size:28px;font-weight:600;color:#fff;letter-spacing:-1px;font-family:'Sora',sans-serif;border:2px solid var(--border)}
.online-dot{position:absolute;bottom:4px;right:4px;width:14px;height:14px;border-radius:50%;background:var(--green);border:2.5px solid var(--bg)}

.name{font-size:22px;font-weight:600;color:var(--text);margin-bottom:2px}
.handle{font-size:15px;color:var(--text2);font-weight:300;margin-bottom:10px}
.bio{font-size:13.5px;color:var(--text2);line-height:1.6;max-width:500px;margin-bottom:12px}
.meta{display:flex;gap:16px;flex-wrap:wrap}
.meta-item{display:flex;align-items:center;gap:5px;font-size:12px;color:var(--text3)}
.meta-item i{font-size:14px;color:var(--text3)}
.meta-item a{color:var(--blue);text-decoration:none}
.meta-item a:hover{text-decoration:underline}

.follow-row{display:flex;align-items:center;gap:12px;margin-top:12px;flex-wrap:wrap}
.btn-follow{padding:5px 16px;border-radius:6px;font-size:13px;font-weight:500;cursor:pointer;border:1px solid;font-family:'Sora',sans-serif;transition:all 0.15s}
.btn-primary{background:var(--green);color:#0d1117;border-color:var(--green)}
.btn-primary:hover{filter:brightness(0.88)}
.btn-secondary{background:var(--bg3);color:var(--text);border-color:var(--border2)}
.btn-secondary:hover{background:var(--border)}
.followers-count{font-size:13px;color:var(--text2)}
.followers-count span{color:var(--text);font-weight:500}

.divider{border:none;border-top:1px solid var(--border);margin:1.5rem 0}

.stats-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:12px;margin-bottom:2rem}
.stat-card{background:var(--bg2);border:1px solid var(--border);border-radius:8px;padding:14px 16px}
.stat-num{font-size:22px;font-weight:600;font-family:'JetBrains Mono',monospace;color:var(--text)}
.stat-label{font-size:11px;color:var(--text3);margin-top:2px;text-transform:uppercase;letter-spacing:0.06em}
.stat-delta{font-size:11px;color:var(--green);margin-top:4px}

.section-title{font-size:13px;font-weight:500;color:var(--text2);text-transform:uppercase;letter-spacing:0.08em;margin-bottom:14px;display:flex;align-items:center;gap:8px}
.section-title::after{content:'';flex:1;height:1px;background:var(--border)}

.grid-2{display:grid;grid-template-columns:1fr 1fr;gap:14px;margin-bottom:2rem}

.repo-card{background:var(--bg2);border:1px solid var(--border);border-radius:10px;padding:16px;transition:border-color 0.15s;cursor:pointer}
.repo-card:hover{border-color:var(--border2)}
.repo-top{display:flex;align-items:center;justify-content:space-between;margin-bottom:8px}
.repo-name{font-size:14px;font-weight:500;color:var(--blue);display:flex;align-items:center;gap:6px}
.repo-name i{font-size:14px;color:var(--text3)}
.repo-badge{font-size:10px;padding:2px 8px;border-radius:20px;border:1px solid var(--border2);color:var(--text3)}
.repo-desc{font-size:12.5px;color:var(--text2);line-height:1.5;margin-bottom:12px}
.repo-meta{display:flex;gap:14px;align-items:center}
.repo-lang{display:flex;align-items:center;gap:5px;font-size:12px;color:var(--text2)}
.lang-dot{width:10px;height:10px;border-radius:50%;flex-shrink:0}
.repo-stars{display:flex;align-items:center;gap:4px;font-size:12px;color:var(--text2)}

.tech-section{margin-bottom:2rem}
.tech-grid{display:flex;flex-wrap:wrap;gap:8px}
.tech-tag{display:flex;align-items:center;gap:6px;padding:6px 12px;border-radius:6px;font-size:12.5px;font-weight:500;border:1px solid;font-family:'JetBrains Mono',monospace;transition:all 0.15s;cursor:default}
.tech-tag:hover{filter:brightness(1.15)}
.t-blue{background:rgba(88,166,255,0.1);color:#58a6ff;border-color:rgba(88,166,255,0.25)}
.t-purple{background:rgba(188,140,255,0.1);color:#bc8cff;border-color:rgba(188,140,255,0.25)}
.t-green{background:rgba(63,185,80,0.1);color:#3fb950;border-color:rgba(63,185,80,0.25)}
.t-orange{background:rgba(255,166,87,0.1);color:#ffa657;border-color:rgba(255,166,87,0.25)}
.t-pink{background:rgba(247,120,186,0.1);color:#f778ba;border-color:rgba(247,120,186,0.25)}
.t-teal{background:rgba(57,211,83,0.1);color:#39d353;border-color:rgba(57,211,83,0.25)}
.t-gray{background:rgba(139,148,158,0.1);color:#8b949e;border-color:rgba(139,148,158,0.25)}

.contrib-section{margin-bottom:2rem}
.contrib-graph{background:var(--bg2);border:1px solid var(--border);border-radius:10px;padding:16px}
.contrib-top{display:flex;justify-content:space-between;align-items:center;margin-bottom:14px}
.contrib-count{font-size:13px;color:var(--text2)}
.contrib-count strong{color:var(--text)}
.months{display:flex;gap:0;margin-bottom:6px}
.month-label{font-size:10px;color:var(--text3);width:28px;text-align:center;flex-shrink:0}
.graph-grid{display:flex;gap:3px}
.graph-col{display:flex;flex-direction:column;gap:3px}
.graph-cell{width:11px;height:11px;border-radius:2px;background:var(--bg3)}
.l1{background:rgba(57,211,83,0.2)}
.l2{background:rgba(57,211,83,0.4)}
.l3{background:rgba(57,211,83,0.65)}
.l4{background:#39d353}

.activity-section{margin-bottom:2rem}
.activity-list{display:flex;flex-direction:column;gap:0}
.activity-item{display:flex;align-items:flex-start;gap:12px;padding:12px 0;border-bottom:1px solid var(--border)}
.activity-item:last-child{border-bottom:none}
.act-icon{width:28px;height:28px;border-radius:50%;background:var(--bg3);border:1px solid var(--border);display:flex;align-items:center;justify-content:center;flex-shrink:0;margin-top:1px}
.act-icon i{font-size:13px;color:var(--text3)}
.act-text{font-size:13px;color:var(--text2);line-height:1.5}
.act-text strong{color:var(--blue)}
.act-time{font-size:11px;color:var(--text3);margin-top:2px}

.streak-bar{background:var(--bg2);border:1px solid var(--border);border-radius:10px;padding:16px;margin-bottom:2rem;display:flex;gap:24px;align-items:center}
.streak-num{font-size:36px;font-weight:600;font-family:'JetBrains Mono',monospace;color:var(--orange);line-height:1}
.streak-label{font-size:11px;color:var(--text3);text-transform:uppercase;letter-spacing:0.08em;margin-top:4px}
.streak-divider{width:1px;height:48px;background:var(--border)}
.streak-detail{flex:1}
.streak-row{display:flex;justify-content:space-between;font-size:12px;margin-bottom:6px}
.streak-row span:first-child{color:var(--text3)}
.streak-row span:last-child{color:var(--text);font-weight:500;font-family:'JetBrains Mono',monospace}
.streak-progress{height:4px;background:var(--bg3);border-radius:2px;overflow:hidden}
.streak-fill{height:100%;background:linear-gradient(90deg,var(--orange),var(--pink));border-radius:2px}
</style>

<h2 class="sr-only" style="position:absolute;width:1px;height:1px;overflow:hidden">GitHub profile design for Chuot Chuonchetra, Full Stack Developer from Cambodia</h2>

<div class="wrapper">

<div class="profile-header">
  <div class="avatar-wrap">
    <div class="avatar">CC</div>
    <div class="online-dot"></div>
  </div>
  <div>
    <div class="name">Chuot Chuonchetra</div>
    <div class="handle">@chuonchetra · <span style="color:var(--text3);font-size:13px">he/him</span></div>
    <div class="bio">Full Stack Developer from 🇰🇭 Cambodia. Building scalable web apps with React, TypeScript & Node.js. Passionate about clean architecture, modern UI/UX, and real-world digital solutions.</div>
    <div class="meta">
      <span class="meta-item"><i class="ti ti-map-pin" aria-hidden="true"></i>Phnom Penh, Cambodia</span>
      <span class="meta-item"><i class="ti ti-link" aria-hidden="true"></i><a href="#">portfolio.dev</a></span>
      <span class="meta-item"><i class="ti ti-calendar" aria-hidden="true"></i>Joined 2022</span>
    </div>
    <div class="follow-row">
      <button class="btn-follow btn-primary">Follow</button>
      <button class="btn-follow btn-secondary">Sponsor</button>
      <span class="followers-count"><span>248</span> followers · <span>61</span> following</span>
    </div>
  </div>
</div>

<div class="stats-grid">
  <div class="stat-card">
    <div class="stat-num">34</div>
    <div class="stat-label">Repositories</div>
    <div class="stat-delta">↑ 8 this year</div>
  </div>
  <div class="stat-card">
    <div class="stat-num">1.2k</div>
    <div class="stat-label">Contributions</div>
    <div class="stat-delta">↑ 312 this month</div>
  </div>
  <div class="stat-card">
    <div class="stat-num">248</div>
    <div class="stat-label">Stars earned</div>
    <div class="stat-delta">↑ 42 this month</div>
  </div>
  <div class="stat-card">
    <div class="stat-num">19</div>
    <div class="stat-label">PRs merged</div>
    <div class="stat-delta">↑ 5 this month</div>
  </div>
</div>

<div class="section-title">pinned repositories</div>
<div class="grid-2">
  <div class="repo-card">
    <div class="repo-top">
      <div class="repo-name"><i class="ti ti-lock" aria-hidden="true"></i>pos-system</div>
      <span class="repo-badge">Public</span>
    </div>
    <div class="repo-desc">Full-featured Point of Sale system with inventory management, analytics dashboard, and ABA PayWay integration.</div>
    <div class="repo-meta">
      <div class="repo-lang"><div class="lang-dot" style="background:#3178c6"></div>TypeScript</div>
      <div class="repo-stars"><i class="ti ti-star" style="font-size:13px" aria-hidden="true"></i>47</div>
      <div class="repo-stars"><i class="ti ti-git-fork" style="font-size:13px" aria-hidden="true"></i>12</div>
    </div>
  </div>
  <div class="repo-card">
    <div class="repo-top">
      <div class="repo-name"><i class="ti ti-shopping-cart" aria-hidden="true"></i>ecommerce-platform</div>
      <span class="repo-badge">Public</span>
    </div>
    <div class="repo-desc">Modern e-commerce platform built with React + Node.js, featuring JWT auth, Stripe integration, and real-time order tracking.</div>
    <div class="repo-meta">
      <div class="repo-lang"><div class="lang-dot" style="background:#f7df1e"></div>JavaScript</div>
      <div class="repo-stars"><i class="ti ti-star" style="font-size:13px" aria-hidden="true"></i>38</div>
      <div class="repo-stars"><i class="ti ti-git-fork" style="font-size:13px" aria-hidden="true"></i>9</div>
    </div>
  </div>
  <div class="repo-card">
    <div class="repo-top">
      <div class="repo-name"><i class="ti ti-chart-bar" aria-hidden="true"></i>dashboard-analytics</div>
      <span class="repo-badge">Public</span>
    </div>
    <div class="repo-desc">Admin dashboard with charts, KPI cards, user management, and role-based access control using React + Tailwind CSS.</div>
    <div class="repo-meta">
      <div class="repo-lang"><div class="lang-dot" style="background:#3178c6"></div>TypeScript</div>
      <div class="repo-stars"><i class="ti ti-star" style="font-size:13px" aria-hidden="true"></i>31</div>
      <div class="repo-stars"><i class="ti ti-git-fork" style="font-size:13px" aria-hidden="true"></i>7</div>
    </div>
  </div>
  <div class="repo-card">
    <div class="repo-top">
      <div class="repo-name"><i class="ti ti-api" aria-hidden="true"></i>rest-api-starter</div>
      <span class="repo-badge">Public</span>
    </div>
    <div class="repo-desc">Production-ready Express.js REST API boilerplate with JWT auth, Sequelize ORM, MySQL, rate limiting, and Swagger docs.</div>
    <div class="repo-meta">
      <div class="repo-lang"><div class="lang-dot" style="background:#68a063"></div>Node.js</div>
      <div class="repo-stars"><i class="ti ti-star" style="font-size:13px" aria-hidden="true"></i>29</div>
      <div class="repo-stars"><i class="ti ti-git-fork" style="font-size:13px" aria-hidden="true"></i>14</div>
    </div>
  </div>
</div>

<div class="tech-section">
  <div class="section-title">tech stack</div>
  <div class="tech-grid">
    <span class="tech-tag t-blue"><i class="ti ti-brand-react" aria-hidden="true"></i>React.js</span>
    <span class="tech-tag t-blue"><i class="ti ti-brand-typescript" aria-hidden="true"></i>TypeScript</span>
    <span class="tech-tag t-green"><i class="ti ti-brand-nodejs" aria-hidden="true"></i>Node.js</span>
    <span class="tech-tag t-green">Express.js</span>
    <span class="tech-tag t-purple"><i class="ti ti-database" aria-hidden="true"></i>MySQL</span>
    <span class="tech-tag t-purple">Sequelize ORM</span>
    <span class="tech-tag t-teal">Tailwind CSS</span>
    <span class="tech-tag t-orange"><i class="ti ti-bolt" aria-hidden="true"></i>Vite</span>
    <span class="tech-tag t-pink">Vue.js</span>
    <span class="tech-tag t-gray"><i class="ti ti-lock" aria-hidden="true"></i>JWT Auth</span>
    <span class="tech-tag t-gray"><i class="ti ti-brand-git" aria-hidden="true"></i>Git</span>
    <span class="tech-tag t-gray">REST API</span>
  </div>
</div>

<div class="streak-bar">
  <div>
    <div class="streak-num">47</div>
    <div class="streak-label">day streak 🔥</div>
  </div>
  <div class="streak-divider"></div>
  <div class="streak-detail">
    <div class="streak-row"><span>Total contributions (2025)</span><span>1,247</span></div>
    <div class="streak-row"><span>Longest streak</span><span>62 days</span></div>
    <div class="streak-progress"><div class="streak-fill" style="width:76%"></div></div>
  </div>
</div>

<div class="contrib-section">
  <div class="section-title">contribution activity</div>
  <div class="contrib-graph">
    <div class="contrib-top">
      <span class="contrib-count"><strong>1,247 contributions</strong> in the last year</span>
      <span style="font-size:12px;color:var(--text3)">2024 – 2025</span>
    </div>
    <div id="graph-root"></div>
    <div style="display:flex;align-items:center;gap:6px;margin-top:10px;justify-content:flex-end">
      <span style="font-size:11px;color:var(--text3)">Less</span>
      <div style="width:10px;height:10px;border-radius:2px;background:var(--bg3)"></div>
      <div style="width:10px;height:10px;border-radius:2px;background:rgba(57,211,83,0.2)"></div>
      <div style="width:10px;height:10px;border-radius:2px;background:rgba(57,211,83,0.4)"></div>
      <div style="width:10px;height:10px;border-radius:2px;background:rgba(57,211,83,0.65)"></div>
      <div style="width:10px;height:10px;border-radius:2px;background:#39d353"></div>
      <span style="font-size:11px;color:var(--text3)">More</span>
    </div>
  </div>
</div>

<div class="activity-section">
  <div class="section-title">recent activity</div>
  <div class="activity-list">
    <div class="activity-item">
      <div class="act-icon"><i class="ti ti-git-commit" aria-hidden="true"></i></div>
      <div>
        <div class="act-text">Pushed 3 commits to <strong>pos-system</strong> — feat: add ABA PayWay webhook handler</div>
        <div class="act-time">2 hours ago</div>
      </div>
    </div>
    <div class="activity-item">
      <div class="act-icon"><i class="ti ti-git-pull-request" aria-hidden="true"></i></div>
      <div>
        <div class="act-text">Opened pull request <strong>#24</strong> in ecommerce-platform — refactor: migrate to TypeScript strict mode</div>
        <div class="act-time">1 day ago</div>
      </div>
    </div>
    <div class="activity-item">
      <div class="act-icon"><i class="ti ti-star" aria-hidden="true"></i></div>
      <div>
        <div class="act-text">Starred <strong>shadcn/ui</strong> and <strong>trpc/trpc</strong></div>
        <div class="act-time">2 days ago</div>
      </div>
    </div>
    <div class="activity-item">
      <div class="act-icon"><i class="ti ti-package" aria-hidden="true"></i></div>
      <div>
        <div class="act-text">Created repository <strong>inventory-management</strong> — new full stack project with React + Express</div>
        <div class="act-time">4 days ago</div>
      </div>
    </div>
  </div>
</div>

</div>

<script>
const levels = [0,0,1,1,2,1,0,2,3,2,1,3,4,3,2,1,0,1,2,3,2,4,3,2,1,0,1,2,1,0,1,2,3,4,3,2,1,2,3,2,1,0,1,2,3,2,1,2,3,4,3,2,1];
const months = ['Jun','Jul','Aug','Sep','Oct','Nov','Dec','Jan','Feb','Mar','Apr','May'];
const lc = ['','l1','l2','l3','l4'];
const root = document.getElementById('graph-root');
const mRow = document.createElement('div');
mRow.style.cssText = 'display:flex;gap:3px;margin-bottom:6px;margin-left:14px';
months.forEach(m => {
  const s = document.createElement('span');
  s.textContent = m;
  s.style.cssText = 'font-size:10px;color:var(--text3);width:42px;flex-shrink:0;text-align:center';
  mRow.appendChild(s);
});
root.appendChild(mRow);
const grid = document.createElement('div');
grid.style.cssText = 'display:flex;gap:3px';
const weeks = 52;
const seeded = Array.from({length:weeks*7},(_,i) => {
  const base = levels[i % levels.length];
  const r = Math.random();
  if(r < 0.28) return 0;
  if(r < 0.5) return Math.max(0,base-1);
  if(r < 0.78) return base;
  if(r < 0.92) return Math.min(4,base+1);
  return Math.min(4,base+2);
});
const dLabel = document.createElement('div');
dLabel.style.cssText = 'display:flex;flex-direction:column;gap:3px;margin-right:4px';
['','Mon','','Wed','','Fri',''].forEach(d=>{
  const s=document.createElement('span');
  s.textContent=d;
  s.style.cssText='font-size:10px;color:var(--text3);height:11px;line-height:11px;text-align:right;min-width:24px';
  dLabel.appendChild(s);
});
grid.appendChild(dLabel);
for(let w=0;w<weeks;w++){
  const col = document.createElement('div');
  col.className='graph-col';
  for(let d=0;d<7;d++){
    const cell = document.createElement('div');
    const l = seeded[w*7+d];
    cell.className = 'graph-cell' + (l ? ' '+lc[l] : '');
    cell.title = `${l===0?'No':l===1?'1-2':l===2?'3-5':l===3?'6-9':'10+'} contributions`;
    col.appendChild(cell);
  }
  grid.appendChild(col);
}
root.appendChild(grid);
</script>

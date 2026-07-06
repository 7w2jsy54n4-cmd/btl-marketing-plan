# btl-marketing-plan
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>BTL Marketing Plan — Ahmedabad Launch</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Inter:wght@400;500;600;700;800&family=IBM+Plex+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#14161A;
    --ink-2:#1F2228;
    --paper:#F5F3EE;
    --paper-dim:#E9E6DD;
    --accent:#FF4B3E;
    --accent-dim:#4a2420;
    --lime:#CBFF4D;
    --grey:#9A9FA8;
    --grey-dark:#5B5F68;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  @media (prefers-reduced-motion: reduce){
    *{animation:none!important;transition:none!important;scroll-behavior:auto!important;}
  }
  body{
    margin:0;
    background:var(--ink);
    color:var(--paper);
    font-family:'Inter',sans-serif;
    line-height:1.5;
    -webkit-font-smoothing:antialiased;
  }
  .display{font-family:'Bebas Neue',sans-serif; letter-spacing:0.02em;}
  .mono{font-family:'IBM Plex Mono',monospace;}

  /* HERO */
  .hero{
    padding:64px 24px 48px;
    border-bottom:1px solid #2a2d34;
    position:relative;
    overflow:hidden;
  }
  .hero::before{
    content:"";
    position:absolute;
    top:-40%; right:-10%;
    width:420px; height:420px;
    background:radial-gradient(circle, rgba(255,75,62,0.28) 0%, rgba(255,75,62,0) 70%);
    pointer-events:none;
  }
  .eyebrow{
    display:inline-flex;
    align-items:center;
    gap:8px;
    font-family:'IBM Plex Mono',monospace;
    font-size:11.5px;
    letter-spacing:0.14em;
    color:var(--lime);
    text-transform:uppercase;
    margin-bottom:22px;
  }
  .eyebrow .dot{width:6px;height:6px;border-radius:50%;background:var(--lime);display:inline-block;animation:pulse 2s infinite;}
  @keyframes pulse{0%,100%{opacity:1;}50%{opacity:0.35;}}
  h1.title{
    font-size:clamp(48px, 12vw, 88px);
    line-height:0.92;
    margin:0 0 14px;
    color:var(--paper);
  }
  h1.title span{color:var(--accent);}
  .subtitle{
    font-size:16px;
    color:var(--grey);
    max-width:520px;
    margin:0 0 28px;
    font-weight:500;
  }
  .byline{
    display:flex;
    flex-wrap:wrap;
    gap:10px 28px;
    font-size:13px;
    color:var(--grey);
    border-top:1px solid #2a2d34;
    padding-top:18px;
    margin-top:6px;
  }
  .byline b{color:var(--paper); font-weight:700;}

  .stat-row{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:1px;
    background:#2a2d34;
    margin-top:36px;
    border:1px solid #2a2d34;
  }
  .stat{
    background:var(--ink);
    padding:20px 16px;
    text-align:left;
  }
  .stat .num{font-family:'Bebas Neue'; font-size:clamp(30px,6vw,44px); color:var(--accent); line-height:1;}
  .stat .lbl{font-size:11px; color:var(--grey); text-transform:uppercase; letter-spacing:0.08em; margin-top:6px;}

  /* CONTROLS */
  .controls{
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:22px 24px 8px;
    max-width:900px;
    margin:0 auto;
  }
  .controls .hint{font-size:12.5px; color:var(--grey);}
  .toggle-all{
    background:none;
    border:1px solid #3a3d44;
    color:var(--paper);
    font-family:'IBM Plex Mono',monospace;
    font-size:11.5px;
    letter-spacing:0.06em;
    text-transform:uppercase;
    padding:8px 14px;
    border-radius:100px;
    cursor:pointer;
    transition:border-color 0.2s, background 0.2s;
  }
  .toggle-all:hover{border-color:var(--accent); background:rgba(255,75,62,0.08);}

  /* ACCORDION */
  .plan{
    max-width:900px;
    margin:0 auto;
    padding:8px 24px 90px;
  }
  .item{
    border-bottom:1px solid #2a2d34;
  }
  .item:first-child{border-top:1px solid #2a2d34;}
  .head{
    width:100%;
    background:none;
    border:none;
    display:flex;
    align-items:center;
    gap:18px;
    padding:22px 0;
    cursor:pointer;
    text-align:left;
    color:var(--paper);
    font-family:inherit;
  }
  .idx{
    font-family:'IBM Plex Mono',monospace;
    font-size:13px;
    color:var(--ink);
    background:var(--grey);
    min-width:34px;
    height:34px;
    display:flex;
    align-items:center;
    justify-content:center;
    border-radius:6px;
    flex-shrink:0;
    transition:background 0.25s, color 0.25s;
  }
  .item[data-open="true"] .idx{background:var(--accent); color:var(--ink);}
  .head .htext{flex:1; min-width:0;}
  .head h2{
    font-family:'Bebas Neue';
    font-size:clamp(20px,4vw,28px);
    margin:0;
    letter-spacing:0.01em;
    color:var(--paper);
  }
  .head .teaser{
    font-size:13px;
    color:var(--grey);
    margin-top:3px;
    display:block;
    font-weight:500;
  }
  .chip{
    font-family:'IBM Plex Mono',monospace;
    font-size:10.5px;
    color:var(--lime);
    border:1px solid rgba(203,255,77,0.35);
    padding:4px 9px;
    border-radius:100px;
    white-space:nowrap;
    flex-shrink:0;
    text-transform:uppercase;
  }
  .chevron{
    flex-shrink:0;
    width:20px; height:20px;
    color:var(--grey);
    transition:transform 0.3s ease;
  }
  .item[data-open="true"] .chevron{transform:rotate(180deg); color:var(--accent);}

  .panel{
    max-height:0;
    overflow:hidden;
    transition:max-height 0.4s cubic-bezier(.4,0,.2,1);
  }
  .panel-inner{
    padding:2px 0 32px 52px;
    color:#2b2b2b;
  }
  .body-block{
    background:var(--paper);
    color:#232323;
    border-radius:14px;
    padding:22px 24px;
  }
  .body-block p{margin:0 0 14px; font-size:14.5px; color:#3a3a3a;}
  .body-block p:last-child{margin-bottom:0;}
  .body-block ul{margin:0 0 6px; padding-left:20px;}
  .body-block li{margin-bottom:9px; font-size:14.5px; color:#3a3a3a;}
  .body-block h4{
    font-family:'Bebas Neue';
    font-size:18px;
    color:var(--accent);
    margin:18px 0 8px;
    letter-spacing:0.02em;
  }
  .body-block h4:first-child{margin-top:0;}
  .sub{margin-bottom:18px;}
  .sub:last-child{margin-bottom:0;}

  table{width:100%; border-collapse:collapse; margin:10px 0 18px; font-size:13.5px;}
  table:last-child{margin-bottom:0;}
  th{
    background:var(--ink);
    color:var(--paper);
    text-align:left;
    padding:10px 12px;
    font-size:11px;
    text-transform:uppercase;
    letter-spacing:0.05em;
    font-family:'IBM Plex Mono',monospace;
    font-weight:500;
  }
  td{
    padding:10px 12px;
    border-bottom:1px solid var(--paper-dim);
    color:#3a3a3a;
    vertical-align:top;
  }
  tr:last-child td{border-bottom:none;}
  th:first-child, td:first-child{border-radius:0;}

  .closing{
    background:var(--ink-2);
    border-left:3px solid var(--accent);
    padding:20px 24px;
    margin-top:6px;
  }
  .closing p{color:#d8d8d8; font-size:14.5px;}
  .signoff{margin-top:14px; font-family:'Bebas Neue'; font-size:22px; color:var(--paper);}

  footer{
    text-align:center;
    padding:30px 24px 60px;
    color:var(--grey-dark);
    font-size:12px;
  }

  @media (max-width:560px){
    .panel-inner{padding-left:0;}
    .head{gap:12px;}
    .chip{display:none;}
    .stat-row{grid-template-columns:1fr;}
  }
</style>
</head>
<body>

<div class="hero">
  <span class="eyebrow"><span class="dot"></span>Candidacy — Lead, BTL Marketing, Ahmedabad</span>
  <h1 class="title">BTL PLAN<br><span>AHMEDABAD.</span></h1>
  <p class="subtitle">A 90-day ground activation, lead generation and membership conversion plan for the CG Road and Vastrapur launches.</p>
  <div class="byline">
    <span>Submitted by <b>Mohit Raj</b></span>
    <span>Prepared for <b>JAS</b></span>
    <span>Centers: <b>CG Road · Vastrapur</b></span>
  </div>
  <div class="stat-row">
    <div class="stat"><div class="num mono">72</div><div class="lbl">Trial classes / 90 days</div></div>
    <div class="stat"><div class="num mono">6</div><div class="lbl">BTL activation pillars</div></div>
    <div class="stat"><div class="num mono">12–15%</div><div class="lbl">Target trial→member conversion</div></div>
  </div>
</div>

<div class="controls">
  <span class="hint">Tap any section to expand</span>
  <button class="toggle-all" id="toggleAll">Expand all</button>
</div>

<div class="plan" id="plan"></div>

<footer>BTL Marketing Plan · Ahmedabad Launch · Prepared for JAS by Mohit Raj</footer>

<script>
const sections = [
  {
    tag: "Overview",
    title: "Executive Summary",
    teaser: "Why free trial classes are the engine of this whole plan.",
    body: `<div class="body-block">
      <p>Two new centers are opening in Ahmedabad — CG Road and Vastrapur — offering group class formats across Dance, Yoga, Boxing, Strength and Gym. The mandate: build local awareness fast, get the community moving inside our centers, and convert first-time attendees into paying members within 90 days.</p>
      <p>This plan is built around one core BTL principle — nothing sells a fitness brand like a first free class. Every activation below (society activations, corporate tie-ups, college outreach, influencer classes) exists to funnel people into one thing: a free trial class at the center, run 3 times a week, every week, without fail. From there, a disciplined lead-capture and follow-up system converts attendees into members.</p>
      <p><b>Target:</b> 2 centers × 12 weeks × 3 trial classes/week = 72 trial sessions minimum, feeding a structured 7-day conversion funnel, with a goal of 12–15% trial-to-membership conversion by Month 3.</p>
    </div>`
  },
  {
    tag: "Goals",
    title: "Objectives & Success Definition",
    teaser: "What winning looks like by Day 90.",
    body: `<div class="body-block"><ul>
      <li>Drive qualified footfall into CG Road and Vastrapur through hyperlocal BTL activity — not paid digital-led.</li>
      <li>Establish a repeatable weekly cadence: 3 trial classes/week/center, 6 across both centers.</li>
      <li>Build a clean, centralized lead database (name, phone, area, class attended, interest level) owned by each center manager.</li>
      <li>Convert trial attendees to paying members via a structured 3-touchpoint follow-up within 7 days of their session.</li>
      <li>Hit a founding-member base of 300+ members per center by end of Month 3, with 40% acquired via BTL-sourced trials.</li>
    </ul></div>`
  },
  {
    tag: "Market",
    title: "CG Road vs Vastrapur",
    teaser: "Two very different micro-markets, two different playbooks.",
    body: `<div class="body-block">
      <table>
        <tr><th>Parameter</th><th>CG Road</th><th>Vastrapur</th></tr>
        <tr><td>Audience</td><td>Young working professionals, corporate crowd, retail staff, students nearby</td><td>Family-heavy residential, IT/business owners, lake-goers, higher women's fitness participation</td></tr>
        <tr><td>Peak footfall</td><td>7–9 AM & 7–10 PM</td><td>6–9 AM & 6–9 PM, plus weekend mornings</td></tr>
        <tr><td>Best class mix</td><td>Boxing, Strength, quick-sweat Gym formats</td><td>Yoga, Dance, family/women-only Strength batches</td></tr>
        <tr><td>Key BTL zones</td><td>Corporate parks, malls, PG clusters</td><td>Vastrapur Lake, societies, schools</td></tr>
        <tr><td>Competitive read</td><td>Existing premium gyms — differentiate on community + group energy</td><td>Fragmented local yoga/zumba studios — easy to out-position on brand + variety</td></tr>
      </table>
    </div>`
  },
  {
    tag: "Audience",
    title: "Target Audience Segments",
    teaser: "Five groups, five different reasons to walk in.",
    body: `<div class="body-block"><ul>
      <li><b>Corporate professionals (25–40):</b> want quick, high-energy sessions before/after work.</li>
      <li><b>Residential society members (25–55):</b> want variety and the safety of a known nearby brand.</li>
      <li><b>College students (18–24):</b> price-sensitive, drawn to Dance/Boxing and social-worthy content.</li>
      <li><b>Homemakers & women's fitness groups:</b> strong pull for Yoga & Dance mornings, referral-heavy.</li>
      <li><b>Competitor gym-goers:</b> switchers who respond to "try us free" and better group-class variety.</li>
    </ul></div>`
  },
  {
    tag: "Strategy",
    title: "BTL Strategy Pillars",
    teaser: "Six ground-level channels, all feeding the same trial calendar.",
    body: `<div class="body-block">
      <div class="sub"><h4>1 · Society & RWA Activation</h4><ul>
        <li>Tie up with 8–10 large societies within 2 km of each center for weekend "Society Fit Fest" pop-ups.</li>
        <li>Every attendee gets a QR-code flyer for a free trial class at the center that week.</li>
        <li>Partner with RWA WhatsApp groups — group discount for 5+ members joining together.</li>
      </ul></div>
      <div class="sub"><h4>2 · Corporate & Office Park Outreach (CG Road focus)</h4><ul>
        <li>Lunchtime or post-work "Desk Break" 20-min samplers at 5–7 corporate offices/co-working spaces.</li>
        <li>Corporate group membership slabs (10+ employees) with an HR-coordinated onboarding day.</li>
      </ul></div>
      <div class="sub"><h4>3 · College & Young Adult Outreach</h4><ul>
        <li>Campus activation booths near 3–4 large colleges — Dance/Boxing sampler + reel-style content.</li>
        <li>Student ID discount for the first 100 sign-ups per center.</li>
      </ul></div>
      <div class="sub"><h4>4 · On-Ground Sampling at High-Footfall Points</h4><ul>
        <li>Weekend stalls at Vastrapur Lake and near CG Road malls — 5-min "try a move" hooks into a QR sign-up.</li>
      </ul></div>
      <div class="sub"><h4>5 · Micro-Influencer & Local Community Faces</h4><ul>
        <li>5–6 hyperlocal micro-influencers (5k–50k followers) per zone for a free trial + content swap.</li>
        <li>Guest-led opening week class from a known local Zumba/Yoga instructor.</li>
      </ul></div>
      <div class="sub"><h4>6 · Referral Engine (Member-Gets-Member)</h4><ul>
        <li>Every new member gets 2 referral passes to gift a free trial class — tracked back to a reward.</li>
      </ul></div>
    </div>`
  },
  {
    tag: "Schedule",
    title: "Weekly Trial Class Framework",
    teaser: "3 fixed classes a week, per center — same days, every week.",
    body: `<div class="body-block">
      <table>
        <tr><th>Day</th><th>Time</th><th>Format</th><th>Feeder activation</th></tr>
        <tr><td>Tuesday</td><td>7:00–8:00 PM</td><td>Dance / Zumba</td><td>Society + college outreach</td></tr>
        <tr><td>Thursday</td><td>6:30–7:30 AM (Vastrapur) / 8:00–9:00 PM (CG Road)</td><td>Boxing / Strength</td><td>Corporate outreach + lake/mall sampling</td></tr>
        <tr><td>Saturday</td><td>9:00–10:00 AM</td><td>Yoga / Family Wellness</td><td>RWA tie-ups + referral slot</td></tr>
      </table>
      <p>Each batch capped at 20–25 attendees — keeps energy high and instructor attention personal, which is what gets people to come back and pay.</p>
    </div>`
  },
  {
    tag: "Process",
    title: "Lead Capture Process",
    teaser: "No attendee leaves a class without being captured.",
    body: `<div class="body-block"><ul>
      <li>Entry-desk QR code / tab form captures name, phone, area, class attended, interest level (hot/warm/cold) in under 30 seconds.</li>
      <li>Center Manager directly owns this sheet/CRM entry for every session — reviewed daily, no exceptions.</li>
      <li>Same-day, each lead is tagged with a follow-up owner.</li>
      <li>Weekly consolidated lead report shared with Mohit — totals, hot/warm/cold split, source of activation.</li>
    </ul></div>`
  },
  {
    tag: "Funnel",
    title: "Conversion Funnel: Trial → Membership",
    teaser: "Three touchpoints, seven days, one owner.",
    body: `<div class="body-block">
      <table>
        <tr><th>Touchpoint</th><th>Timing</th><th>Owner</th><th>Action</th></tr>
        <tr><td>Touch 1</td><td>Within 2 hrs</td><td>Manager</td><td>Thank-you call/WhatsApp + ask how the class felt + share plans</td></tr>
        <tr><td>Touch 2</td><td>Day 2</td><td>Manager</td><td>Limited-window "founding member" offer + invite to a second class if undecided</td></tr>
        <tr><td>Touch 3</td><td>Day 5–7</td><td>Manager</td><td>Final personal call — address objections and close, or mark lost with reason</td></tr>
      </table>
      <p>Every "lost" lead is tagged with a reason (price, location, timing, format mismatch) — this data directly shapes Month 2 and 3 adjustments.</p>
    </div>`
  },
  {
    tag: "Timeline",
    title: "90-Day Roadmap",
    teaser: "Seed → Scale → Optimize, in three four-week blocks.",
    body: `<div class="body-block">
      <div class="sub"><h4>Month 1 · Seed & Sample</h4><ul>
        <li>Finalize 8–10 society tie-ups and 5–7 corporate contacts per center.</li>
        <li>Launch the fixed Tue/Thu/Sat trial schedule at both centers from Week 1.</li>
        <li>Run opening week with 1–2 micro-influencer/guest-led sessions to seed content.</li>
        <li>Goal: 150+ leads/center, first 30–40 conversions/center.</li>
      </ul></div>
      <div class="sub"><h4>Month 2 · Scale & Convert</h4><ul>
        <li>Expand society/college activations based on Month 1 response data.</li>
        <li>Launch the referral engine once each center has ~150 members.</li>
        <li>Introduce corporate group membership packages as a distinct push.</li>
        <li>Goal: 250+ cumulative leads/center, conversion improving to 10–12%.</li>
      </ul></div>
      <div class="sub"><h4>Month 3 · Optimize & Lock-In</h4><ul>
        <li>Double down on the highest-performing channel per center — data-led, not assumption-led.</li>
        <li>Run a "Founding Member Deadline" urgency campaign for undecided leads.</li>
        <li>Community open-house event at each center to lock in retention and referral content.</li>
        <li>Goal: 300+ members/center, 12–15% overall conversion, a documented playbook for the next city.</li>
      </ul></div>
    </div>`
  },
  {
    tag: "Team",
    title: "Roles & Ownership",
    teaser: "Who owns what, so nothing falls through.",
    body: `<div class="body-block">
      <table>
        <tr><th>Role</th><th>Responsibility</th></tr>
        <tr><td>Mohit (BTL Lead)</td><td>Strategy, partnership sourcing, weekly review with JAS, activation calendar ownership</td></tr>
        <tr><td>Center Manager</td><td>Owns lead capture at every class, drives the 3-touch follow-up, daily CRM hygiene, on-ground execution</td></tr>
        <tr><td>Instructors</td><td>Deliver high-energy trial sessions — the actual conversion moment, briefed weekly on the attending segment</td></tr>
        <tr><td>BTL Associates</td><td>Society/college/mall stall execution, flyers, QR sign-ups, content capture</td></tr>
      </table>
    </div>`
  },
  {
    tag: "Metrics",
    title: "Weekly KPI Dashboard",
    teaser: "Tracked every Monday, per center.",
    body: `<div class="body-block">
      <table>
        <tr><th>Metric</th><th>Target / week</th></tr>
        <tr><td>Trial classes conducted</td><td>3</td></tr>
        <tr><td>Total trial attendees</td><td>45–60</td></tr>
        <tr><td>Leads captured</td><td>100% of attendees</td></tr>
        <tr><td>Hot leads followed up within 48 hrs</td><td>100%</td></tr>
        <tr><td>Trials converted to membership</td><td>12–15%, cumulative</td></tr>
        <tr><td>New tie-ups added</td><td>1–2</td></tr>
      </table>
    </div>`
  },
  {
    tag: "Budget",
    title: "Indicative BTL Budget Allocation",
    teaser: "Illustrative split, per center per month.",
    body: `<div class="body-block">
      <table>
        <tr><th>Head</th><th>% of Budget</th><th>Notes</th></tr>
        <tr><td>On-ground activation</td><td>35%</td><td>Stalls, society/college pop-ups, signage, sampling props</td></tr>
        <tr><td>Guest/influencer sessions</td><td>20%</td><td>Content collaboration, no large influencer spends</td></tr>
        <tr><td>Print & collateral</td><td>15%</td><td>Localized flyers, standees, QR cards</td></tr>
        <tr><td>Referral & founding-member incentives</td><td>15%</td><td>Merchandise, free PT sessions, referral rewards</td></tr>
        <tr><td>Contingency</td><td>15%</td><td>Reactive activity based on early response data</td></tr>
      </table>
    </div>`
  },
  {
    tag: "Risk",
    title: "Risks & Mitigation",
    teaser: "What could go wrong, and the fix already built in.",
    body: `<div class="body-block"><ul>
      <li><b>Trial attendees don't convert</b> → strict 3-touch follow-up with logged objection reasons, not a one-and-done call.</li>
      <li><b>Society/corporate tie-ups stall</b> → parallel-track 8–10 leads per channel so one delay doesn't stall the calendar.</li>
      <li><b>Class quality dips at scale</b> → cap batch sizes at 20–25, brief instructors weekly on the specific audience.</li>
      <li><b>Lead hygiene breaks down</b> → daily manager review + weekly consolidated report to Mohit, non-negotiable.</li>
    </ul></div>`
  },
  {
    tag: "Close",
    title: "Why This Plan Wins",
    teaser: "One system: sample, capture, follow up, convert.",
    body: `<div class="closing">
      <p>This plan is built on a simple, provable loop: get people into a free class → capture their details without fail → follow up like it matters → convert with urgency and a real offer. It doesn't rely on guesswork or big media spends — it relies on disciplined, weekly, on-ground execution that compounds over 90 days. Every activation exists to feed the trial class calendar, and every trial class exists to feed the conversion funnel. That's a system JAS can measure, trust, and scale to the next city.</p>
      <div class="signoff">— Mohit Raj</div>
    </div>`
  }
];

const plan = document.getElementById('plan');

sections.forEach((s, i) => {
  const item = document.createElement('div');
  item.className = 'item';
  item.setAttribute('data-open', 'false');

  const num = String(i + 1).padStart(2, '0');
  const panelId = 'panel-' + i;
  const headId = 'head-' + i;

  item.innerHTML = `
    <button class="head" id="${headId}" aria-expanded="false" aria-controls="${panelId}">
      <span class="idx mono">${num}</span>
      <span class="htext">
        <h2>${s.title}</h2>
        <span class="teaser">${s.teaser}</span>
      </span>
      <span class="chip">${s.tag}</span>
      <svg class="chevron" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="6 9 12 15 18 9"></polyline></svg>
    </button>
    <div class="panel" id="${panelId}" role="region" aria-labelledby="${headId}">
      <div class="panel-inner">${s.body}</div>
    </div>
  `;
  plan.appendChild(item);

  const head = item.querySelector('.head');
  const panel = item.querySelector('.panel');

  head.addEventListener('click', () => {
    const isOpen = item.getAttribute('data-open') === 'true';
    setOpen(item, panel, head, !isOpen);
  });
});

function setOpen(item, panel, head, open){
  item.setAttribute('data-open', open ? 'true' : 'false');
  head.setAttribute('aria-expanded', open ? 'true' : 'false');
  if(open){
    panel.style.maxHeight = panel.scrollHeight + 'px';
  } else {
    panel.style.maxHeight = '0px';
  }
}

let allOpen = false;
document.getElementById('toggleAll').addEventListener('click', (e) => {
  allOpen = !allOpen;
  e.target.textContent = allOpen ? 'Collapse all' : 'Expand all';
  document.querySelectorAll('.item').forEach(item => {
    const panel = item.querySelector('.panel');
    const head = item.querySelector('.head');
    setOpen(item, panel, head, allOpen);
  });
});

// Recalculate open panel heights on resize (text reflow changes scrollHeight)
window.addEventListener('resize', () => {
  document.querySelectorAll('.item[data-open="true"]').forEach(item => {
    const panel = item.querySelector('.panel');
    panel.style.maxHeight = panel.scrollHeight + 'px';
  });
});
</script>
</body>
</html>

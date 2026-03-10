---
layout: page
permalink: /students/
title: students
description: A summary of supervision and co-supervision activities @ ISEL/IPL
nav: true
nav_order: 3
---

<style>
  /* ── Imports ── */
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,600;1,400&family=DM+Mono:wght@300;400&family=Lato:wght@300;400;700&display=swap');

  /* ── Root tokens ── */
  :root {
    --ink:       #1a1a2e;
    --muted:     #5a5a7a;
    --rule:      #d4d4e8;
    --surface:   #f7f7fb;
    --accent:    #c0392b;       /* deep academic red */
    --accent2:   #1a6b8a;      /* steel blue */
    --tag-bg:    #eef2f7;
    --tag-txt:   #2c4a6e;
    --ongoing-bg:#fff8ec;
    --ongoing-bd:#e8a020;
    --mono:      'DM Mono', monospace;
    --serif:     'Playfair Display', Georgia, serif;
    --sans:      'Lato', sans-serif;
    --radius:    6px;
    --shadow:    0 2px 12px rgba(26,26,46,.07);
  }

  /* ── Page shell ── */
  .sv-page {
    font-family: var(--sans);
    color: var(--ink);
    max-width: 900px;
    margin: 0 auto;
    padding: 0 1rem 4rem;
  }

  /* ── Hero banner ── */
  .sv-hero {
    border-left: 4px solid var(--accent);
    padding: 1.6rem 2rem;
    margin: 2.5rem 0 3rem;
    background: var(--surface);
    border-radius: 0 var(--radius) var(--radius) 0;
    box-shadow: var(--shadow);
  }
  .sv-hero p {
    margin: 0;
    font-size: 1.05rem;
    line-height: 1.7;
    color: var(--muted);
    font-weight: 300;
  }
  .sv-hero strong {
    font-family: var(--serif);
    font-size: 2rem;
    font-weight: 600;
    color: var(--ink);
    display: block;
    margin-bottom: .5rem;
    line-height: 1.15;
  }

  /* ── Stat strip ── */
  .sv-stats {
    display: flex;
    gap: 1.5rem;
    flex-wrap: wrap;
    margin-bottom: 3.5rem;
  }
  .sv-stat {
    flex: 1 1 140px;
    background: #fff;
    border: 1px solid var(--rule);
    border-radius: var(--radius);
    padding: 1.1rem 1.4rem;
    text-align: center;
    box-shadow: var(--shadow);
  }
  .sv-stat-num {
    font-family: var(--serif);
    font-size: 2.2rem;
    font-weight: 600;
    color: var(--accent2);
    line-height: 1;
  }
  .sv-stat-lbl {
    font-size: .72rem;
    letter-spacing: .08em;
    text-transform: uppercase;
    color: var(--muted);
    margin-top: .35rem;
  }

  /* ── Programme section ── */
  .sv-programme {
    margin-bottom: 3.5rem;
  }
  .sv-prog-header {
    display: flex;
    align-items: baseline;
    gap: 1rem;
    margin-bottom: 1.2rem;
    padding-bottom: .6rem;
    border-bottom: 2px solid var(--rule);
  }
  .sv-prog-title {
    font-family: var(--serif);
    font-size: 1.25rem;
    font-weight: 600;
    color: var(--ink);
    margin: 0;
  }
  .sv-prog-degree {
    font-family: var(--mono);
    font-size: .7rem;
    font-weight: 400;
    color: #fff;
    background: var(--accent2);
    border-radius: 3px;
    padding: .15em .5em;
    letter-spacing: .04em;
    white-space: nowrap;
    position: relative;
    top: -1px;
  }
  .sv-prog-degree.msc { background: var(--accent2); }
  .sv-prog-degree.bsc { background: #4a7c59; }

  /* ── Card grid ── */
  .sv-cards {
    display: grid;
    gap: .75rem;
  }

  /* ── Thesis card ── */
  .sv-card {
    display: grid;
    grid-template-columns: 54px 1fr auto;
    align-items: start;
    gap: 0 1rem;
    background: #fff;
    border: 1px solid var(--rule);
    border-radius: var(--radius);
    padding: .9rem 1.1rem;
    box-shadow: var(--shadow);
    transition: box-shadow .18s, border-color .18s, transform .18s;
  }
  .sv-card:hover {
    box-shadow: 0 6px 24px rgba(26,26,46,.12);
    border-color: #bbbbd8;
    transform: translateY(-1px);
  }
  .sv-card.ongoing {
    border-left: 3px solid var(--ongoing-bd);
    background: var(--ongoing-bg);
  }

  /* Year column */
  .sv-year {
    font-family: var(--mono);
    font-size: .82rem;
    color: var(--muted);
    padding-top: .15rem;
    text-align: right;
    line-height: 1.4;
  }

  /* Main column */
  .sv-main {}
  .sv-title {
    font-size: .95rem;
    font-weight: 400;
    color: var(--ink);
    line-height: 1.45;
    margin: 0 0 .3rem;
  }
  .sv-title em { font-style: italic; color: var(--muted); }
  .sv-students {
    font-size: .8rem;
    color: var(--muted);
    font-weight: 300;
    display: flex;
    flex-wrap: wrap;
    gap: .3rem;
  }
  .sv-student-chip {
    background: var(--tag-bg);
    color: var(--tag-txt);
    border-radius: 3px;
    padding: .05em .45em;
    font-size: .75rem;
  }

  /* Badge column */
  .sv-badge {
    align-self: center;
  }
  .sv-ongoing-badge {
    font-family: var(--mono);
    font-size: .64rem;
    letter-spacing: .06em;
    text-transform: uppercase;
    background: var(--ongoing-bd);
    color: #fff;
    border-radius: 3px;
    padding: .15em .5em;
    white-space: nowrap;
  }

  /* ── Legend ── */
  .sv-legend {
    margin-top: 3rem;
    padding-top: 1rem;
    border-top: 1px solid var(--rule);
    font-size: .78rem;
    color: var(--muted);
    display: flex;
    gap: 1.5rem;
    flex-wrap: wrap;
  }
  .sv-legend-item {
    display: flex;
    align-items: center;
    gap: .4rem;
  }
  .sv-legend-dot {
    width: 10px; height: 10px;
    border-radius: 2px;
    flex-shrink: 0;
  }

  /* ── Responsive ── */
  @media (max-width: 600px) {
    .sv-card {
      grid-template-columns: 44px 1fr;
    }
    .sv-badge { display: none; }
    .sv-card.ongoing .sv-title::after {
      content: ' ↗';
      font-style: normal;
      color: var(--ongoing-bd);
    }
    .sv-stats { gap: .75rem; }
    .sv-stat { flex: 1 1 100px; }
  }
</style>

<div class="sv-page">

  <!-- Hero -->
  <div class="sv-hero">
    <strong>Student Supervision</strong>
    <p>
      Over the years, I supervised or co-supervised more than <strong>70 students</strong> across
      Master's and Bachelor's programmes (MEIC, MEET, LEIC, LEIRT, and LEIM) at ISEL/IPL.
      These works span distributed systems, cloud &amp; edge computing, cybersecurity, IoT,
      and mobile devices — often resulting in publications and applied research outcomes.
      The records below cover <strong>2021–2025</strong>.
    </p>
  </div>

  <!-- Stats strip -->
  <div class="sv-stats">
    <div class="sv-stat">
      <div class="sv-stat-num">70+</div>
      <div class="sv-stat-lbl">Total students</div>
    </div>
    <div class="sv-stat">
      <div class="sv-stat-num">6</div>
      <div class="sv-stat-lbl">Ongoing works</div>
    </div>
    <div class="sv-stat">
      <div class="sv-stat-num">5</div>
      <div class="sv-stat-lbl">Programmes</div>
    </div>
    <div class="sv-stat">
      <div class="sv-stat-num">2021</div>
      <div class="sv-stat-lbl">Records from</div>
    </div>
  </div>

  <!-- ═══ MSc MEIC ═══ -->
  <section class="sv-programme">
    <div class="sv-prog-header">
      <h2 class="sv-prog-title">Informatics and Computer Engineering</h2>
      <span class="sv-prog-degree msc">MSc · MEIC</span>
    </div>
    <div class="sv-cards">

      <div class="sv-card ongoing">
        <div class="sv-year">2025</div>
        <div class="sv-main">
          <p class="sv-title">QuickFaaS + OmniFlow</p>
          <div class="sv-students"><span class="sv-student-chip">Pedro Carvalho</span></div>
        </div>
        <div class="sv-badge"><span class="sv-ongoing-badge">Ongoing</span></div>
      </div>

      <div class="sv-card ongoing">
        <div class="sv-year">2024</div>
        <div class="sv-main">
          <p class="sv-title">Advanced Function Composition in Serverless Platforms</p>
          <div class="sv-students"><span class="sv-student-chip">Tiago Silva</span></div>
        </div>
        <div class="sv-badge"><span class="sv-ongoing-badge">Ongoing</span></div>
      </div>

      <div class="sv-card ongoing">
        <div class="sv-year">2024</div>
        <div class="sv-main">
          <p class="sv-title">Data-Driven Optimisation of Multimodal Public Transport System</p>
          <div class="sv-students"><span class="sv-student-chip">João Cravo</span></div>
        </div>
        <div class="sv-badge"><span class="sv-ongoing-badge">Ongoing</span></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2023</div>
        <div class="sv-main">
          <p class="sv-title"><em>Integration of Travel Context Information into Multimodal Platforms</em></p>
          <div class="sv-students"><span class="sv-student-chip">Pedro Diogo</span></div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2023</div>
        <div class="sv-main">
          <p class="sv-title"><em>LockyCloudCore – CTT Locker Management Infrastructure</em></p>
          <div class="sv-students"><span class="sv-student-chip">Miguel Seleiro</span></div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2023</div>
        <div class="sv-main">
          <p class="sv-title"><em>Scalable Processing Architecture for Banking Operations</em></p>
          <div class="sv-students"><span class="sv-student-chip">Afonso Machado</span></div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2022</div>
        <div class="sv-main">
          <p class="sv-title"><em>Security in Hybrid ITS Networks</em></p>
          <div class="sv-students"><span class="sv-student-chip">Ricardo Severino</span></div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2022</div>
        <div class="sv-main">
          <p class="sv-title"><em>Function Composition in Function-as-a-Service Platforms</em></p>
          <div class="sv-students"><span class="sv-student-chip">Bernardo Costa</span></div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2022</div>
        <div class="sv-main">
          <p class="sv-title"><em>Monitoring Resources in FaaS Platforms</em></p>
          <div class="sv-students"><span class="sv-student-chip">Beatriz Guerreiro</span></div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2022</div>
        <div class="sv-main">
          <p class="sv-title"><em>Software Weaknesses Detection using Machine Learning</em></p>
          <div class="sv-students"><span class="sv-student-chip">Sana Conté</span></div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2022</div>
        <div class="sv-main">
          <p class="sv-title"><em>FaaS Utility</em></p>
          <div class="sv-students"><span class="sv-student-chip">Henrique Santos</span> <span class="sv-student-chip" style="background:#e8eef8;color:#3a5080;">IST</span></div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2022</div>
        <div class="sv-main">
          <p class="sv-title"><em>FaaS@Edge</em></p>
          <div class="sv-students"><span class="sv-student-chip">Catarina Gonçalves</span> <span class="sv-student-chip" style="background:#e8eef8;color:#3a5080;">IST</span></div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2022</div>
        <div class="sv-main">
          <p class="sv-title"><em>RapiTest – Web Application for REST API Testing</em></p>
          <div class="sv-students"><span class="sv-student-chip">Duarte Felício</span></div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2022</div>
        <div class="sv-main">
          <p class="sv-title"><em>Characterizing and Providing Interoperability to FaaS Platforms</em></p>
          <div class="sv-students"><span class="sv-student-chip">Pedro Rodrigues</span></div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2022</div>
        <div class="sv-main">
          <p class="sv-title"><em>Reducing Execution Time in FaaS Cloud Platforms</em></p>
          <div class="sv-students"><span class="sv-student-chip">Ivan Rosa</span></div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2021</div>
        <div class="sv-main">
          <p class="sv-title"><em>Intrusion Detection in LoRaWAN Networks</em></p>
          <div class="sv-students"><span class="sv-student-chip">Filipe Fidalgo</span></div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2021</div>
        <div class="sv-main">
          <p class="sv-title"><em>SPDSBench: Stream Processing Infrastructure Analysis</em></p>
          <div class="sv-students"><span class="sv-student-chip">Rúben Garcia</span></div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2021</div>
        <div class="sv-main">
          <p class="sv-title"><em>Complex Event Processing for C-ITS Message Dissemination</em></p>
          <div class="sv-students"><span class="sv-student-chip">Caio Gedan</span></div>
        </div>
        <div class="sv-badge"></div>
      </div>

    </div><!-- /cards -->

  </section>

  <!-- ═══ MSc MEIM ═══ -->
  <section class="sv-programme">
    <div class="sv-prog-header">
      <h2 class="sv-prog-title">Informatics and Multimedia Engineering</h2>
      <span class="sv-prog-degree msc">MSc · MEIM</span>
    </div>
    <div class="sv-cards">

      <div class="sv-card ongoing">
        <div class="sv-year">2024</div>
        <div class="sv-main">
          <p class="sv-title">Phishing detection service</p>
          <div class="sv-students"><span class="sv-student-chip">Gonçalo Nunes</span></div>
        </div>
        <div class="sv-badge"><span class="sv-ongoing-badge">Ongoing</span></div>
      </div>

    </div>

  </section>

  <!-- ═══ MSc MEET ═══ -->
  <section class="sv-programme">
    <div class="sv-prog-header">
      <h2 class="sv-prog-title">Electronic and Telecommunications Engineering</h2>
      <span class="sv-prog-degree msc">MSc · MEET</span>
    </div>
    <div class="sv-cards">

      <div class="sv-card ongoing">
        <div class="sv-year">2024</div>
        <div class="sv-main">
          <p class="sv-title">Applications Performance Analysis in C-ITS</p>
          <div class="sv-students"><span class="sv-student-chip">Petru Sandu</span></div>
        </div>
        <div class="sv-badge"><span class="sv-ongoing-badge">Ongoing</span></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2021</div>
        <div class="sv-main">
          <p class="sv-title"><em>Integration of an Intrusion Detection System into a Railway Communications Gateway</em></p>
          <div class="sv-students"><span class="sv-student-chip">Filipe Costa</span></div>
        </div>
        <div class="sv-badge"></div>
      </div>

    </div>

  </section>

  <!-- ═══ BSc LEIC ═══ -->
  <section class="sv-programme">
    <div class="sv-prog-header">
      <h2 class="sv-prog-title">Informatics and Computer Engineering</h2>
      <span class="sv-prog-degree bsc">BSc · LEIC</span>
    </div>
    <div class="sv-cards">

      <div class="sv-card">
        <div class="sv-year">2024</div>
        <div class="sv-main">
          <p class="sv-title">Voyagio – Skyscannig Web App</p>
          <div class="sv-students">
            <span class="sv-student-chip">Tiago Neves</span>
            <span class="sv-student-chip">David Antunes</span>
          </div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2024</div>
        <div class="sv-main">
          <p class="sv-title">Armazenamento em Multi-Cloud com Segurança para Dados Sensíveis</p>
          <div class="sv-students"><span class="sv-student-chip">Francisco Saraiva</span></div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2024</div>
        <div class="sv-main">
          <p class="sv-title">Prometheus Kotlin Client Library</p>
          <div class="sv-students">
            <span class="sv-student-chip">Rafael Nicolau</span>
            <span class="sv-student-chip">Mário Carvalho</span>
          </div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2023</div>
        <div class="sv-main">
          <p class="sv-title"><em>Planning Mobile Networks as a Service</em></p>
          <div class="sv-students">
            <span class="sv-student-chip">Jorge Simões</span>
            <span class="sv-student-chip">Tiago Silva</span>
          </div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2023</div>
        <div class="sv-main">
          <p class="sv-title"><em>Autonomous Aerial Collection of Mobile Network Quality Measurements</em></p>
          <div class="sv-students">
            <span class="sv-student-chip">Pedro Raminhos</span>
            <span class="sv-student-chip">Daniel Vicente</span>
          </div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2023</div>
        <div class="sv-main">
          <p class="sv-title"><em>Web Platform for Project Creation and Material Exchange</em></p>
          <div class="sv-students">
            <span class="sv-student-chip">Filipe Costa</span>
            <span class="sv-student-chip">José Rodrigues</span>
          </div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2021</div>
        <div class="sv-main">
          <p class="sv-title"><em>Monence – Collaborative Financial Management Web App</em></p>
          <div class="sv-students">
            <span class="sv-student-chip">Hugo Cameira</span>
            <span class="sv-student-chip">João Matos</span>
          </div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2021</div>
        <div class="sv-main">
          <p class="sv-title"><em>HyGlycemiaControl – Blood Glucose Monitoring Platform</em></p>
          <div class="sv-students">
            <span class="sv-student-chip">Vera Serra</span>
            <span class="sv-student-chip">Joana Soeiro</span>
            <span class="sv-student-chip">Joana Vieira</span>
          </div>
        </div>
        <div class="sv-badge"></div>
      </div>

      <div class="sv-card">
        <div class="sv-year">2021</div>
        <div class="sv-main">
          <p class="sv-title"><em>5G QoS Analysis Application</em></p>
          <div class="sv-students">
            <span class="sv-student-chip">Afonso Nobre</span>
            <span class="sv-student-chip">Ricardo Silva</span>
          </div>
        </div>
        <div class="sv-badge"></div>
      </div>

    </div>

  </section>

  <!-- ═══ BSc LEIRT ═══ -->
  <section class="sv-programme">
    <div class="sv-prog-header">
      <h2 class="sv-prog-title">Computer Networks and Telecommunications Engineering</h2>
      <span class="sv-prog-degree bsc">BSc · LEIRT</span>
    </div>
    <div class="sv-cards">

      <div class="sv-card">
        <div class="sv-year">2021</div>
        <div class="sv-main">
          <p class="sv-title"><em>IQ-MON – 5G QoS Monitoring Application</em></p>
          <div class="sv-students">
            <span class="sv-student-chip">Rodrigo Nogueira</span>
            <span class="sv-student-chip">Gonçalo Dias</span>
          </div>
        </div>
        <div class="sv-badge"></div>
      </div>

    </div>

  </section>

  <!-- Legend -->
  <div class="sv-legend">
    <div class="sv-legend-item">
      <div class="sv-legend-dot" style="background:var(--ongoing-bd);"></div>
      <span>Ongoing work</span>
    </div>
    <div class="sv-legend-item">
      <div class="sv-legend-dot" style="background:var(--accent2);"></div>
      <span>MSc programme</span>
    </div>
    <div class="sv-legend-item">
      <div class="sv-legend-dot" style="background:#4a7c59;"></div>
      <span>BSc programme</span>
    </div>
    <div class="sv-legend-item">
      <div class="sv-legend-dot" style="background:#e8eef8;border:1px solid #bbb;"></div>
      <span>External institution (IST)</span>
    </div>
  </div>

</div><!-- /sv-page -->

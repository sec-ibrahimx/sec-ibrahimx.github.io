<script src="https://cdn.tailwindcss.com"></script>
<script src="https://unpkg.com/lucide@latest"></script>

<style>
  :root {
    --ib-bg: #0b1120;
    --ib-surface: #101a2b;
    --ib-surface-hover: #142238;
    --ib-border: #243249;
    --ib-text: #e6edf7;
    --ib-muted: #9aaac0;
    --ib-accent: #38bdf8;
    --ib-accent-soft: rgba(56, 189, 248, 0.10);
  }

  .ib-portfolio {
    width: 100%;
    max-width: 900px;
    margin-inline: auto;
    padding: 2rem 1.25rem 3.5rem;
    color: var(--ib-text);
    font-family: inherit;
    -webkit-font-smoothing: antialiased;
  }

  .ib-portfolio * { box-sizing: border-box; }

  .ib-portfolio a { text-decoration: none; }

  .ib-portfolio .ib-panel {
    background: linear-gradient(145deg, rgba(17, 27, 45, .96), rgba(13, 21, 36, .94));
    border: 1px solid var(--ib-border);
    border-radius: 18px;
  }

  .ib-portfolio .ib-profile {
    position: relative;
    overflow: hidden;
    padding: clamp(1.2rem, 3vw, 2rem);
    margin-bottom: 2.4rem;
  }

  .ib-portfolio .ib-profile::before {
    content: "";
    position: absolute;
    width: 260px;
    height: 260px;
    top: -170px;
    right: -90px;
    border-radius: 50%;
    background: rgba(56, 189, 248, .09);
    filter: blur(8px);
    pointer-events: none;
  }

  .ib-portfolio .ib-profile-top {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 1rem;
  }

  .ib-portfolio .ib-identity {
    display: flex;
    align-items: center;
    gap: 1rem;
    min-width: 0;
  }

  .ib-portfolio .ib-avatar {
    display: grid;
    place-items: center;
    width: 58px;
    height: 58px;
    flex: 0 0 58px;
    color: var(--ib-accent);
    background: var(--ib-accent-soft);
    border: 1px solid rgba(56, 189, 248, .24);
    border-radius: 16px;
  }

  .ib-portfolio .ib-name {
    margin: 0;
    color: #f8fafc;
    font-size: clamp(1.45rem, 3vw, 1.85rem);
    font-weight: 750;
    line-height: 1.15;
    letter-spacing: -.035em;
  }

  .ib-portfolio .ib-role {
    margin: .4rem 0 0;
    color: var(--ib-muted);
    font-size: .92rem;
    line-height: 1.5;
  }

  .ib-portfolio .ib-github {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: .5rem;
    flex-shrink: 0;
    padding: .65rem .9rem;
    border: 1px solid #34445d;
    border-radius: 10px;
    color: #dce7f5;
    font-size: .82rem;
    font-weight: 600;
    transition: background .2s ease, border-color .2s ease, transform .2s ease;
  }

  .ib-portfolio .ib-github:hover {
    background: #1a2940;
    border-color: #4b6688;
    transform: translateY(-1px);
  }

  .ib-portfolio .ib-intro {
    max-width: 680px;
    margin: 1.5rem 0 1.25rem;
    color: #c7d3e3;
    font-size: .98rem;
    line-height: 1.8;
  }

  .ib-portfolio .ib-tags {
    display: flex;
    flex-wrap: wrap;
    gap: .55rem;
  }

  .ib-portfolio .ib-tag {
    display: inline-flex;
    align-items: center;
    gap: .45rem;
    padding: .45rem .7rem;
    border: 1px solid #26364c;
    border-radius: 9px;
    background: rgba(8, 15, 28, .55);
    color: #c6d4e6;
    font-size: .76rem;
  }

  .ib-portfolio .ib-section { margin-bottom: 2.5rem; }

  .ib-portfolio .ib-section-heading {
    display: flex;
    align-items: center;
    gap: .7rem;
    margin: 0 0 1rem;
    color: #f0f5fb;
    font-size: 1.12rem;
    font-weight: 720;
    letter-spacing: -.015em;
  }

  .ib-portfolio .ib-heading-icon {
    display: grid;
    place-items: center;
    width: 34px;
    height: 34px;
    border-radius: 10px;
    background: var(--ib-accent-soft);
    border: 1px solid rgba(56, 189, 248, .18);
    color: var(--ib-accent);
  }

  .ib-portfolio .ib-section-kicker {
    margin: -.45rem 0 1rem 2.85rem;
    color: #8293aa;
    font-size: .84rem;
    line-height: 1.6;
  }

  .ib-portfolio .ib-interest-list {
    display: grid;
    gap: .8rem;
  }

  .ib-portfolio .ib-interest {
    display: flex;
    align-items: flex-start;
    gap: .95rem;
    padding: 1rem 1.05rem;
    background: rgba(16, 26, 43, .72);
    border: 1px solid var(--ib-border);
    border-radius: 14px;
  }

  .ib-portfolio .ib-interest-icon {
    display: grid;
    place-items: center;
    width: 42px;
    height: 42px;
    flex: 0 0 42px;
    margin-top: .1rem;
    border-radius: 11px;
    color: #a9c1dd;
    background: #17243a;
    border: 1px solid #293a52;
  }

  .ib-portfolio .ib-interest-content { flex: 1; min-width: 0; }

  .ib-portfolio .ib-card-title {
    margin: 0 0 .35rem;
    color: #eef4fb;
    font-size: .98rem;
    line-height: 1.45;
    font-weight: 700;
  }

  .ib-portfolio .ib-card-copy {
    margin: 0;
    color: var(--ib-muted);
    font-size: .86rem;
    line-height: 1.7;
  }

  .ib-portfolio .ib-label {
    flex-shrink: 0;
    margin-top: .1rem;
    padding: .28rem .5rem;
    border: 1px solid #33435a;
    border-radius: 7px;
    color: #b5c5d9;
    background: rgba(25, 39, 60, .7);
    font-size: .7rem;
    white-space: nowrap;
  }

  .ib-portfolio .ib-label-ai { color: #d3baff; border-color: #55427b; background: rgba(75, 47, 117, .2); }
  .ib-portfolio .ib-label-systems { color: #9ed7ff; border-color: #315a7a; background: rgba(32, 85, 122, .2); }
  .ib-portfolio .ib-label-projects { color: #9ee7c2; border-color: #2d6951; background: rgba(30, 105, 75, .18); }

  .ib-portfolio .ib-work-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: .9rem;
  }

  .ib-portfolio .ib-work-card {
    display: flex;
    flex-direction: column;
    min-height: 190px;
    padding: 1.15rem;
    border: 1px solid var(--ib-border);
    border-radius: 15px;
    background: linear-gradient(145deg, rgba(17, 27, 45, .9), rgba(13, 21, 36, .88));
    transition: transform .2s ease, border-color .2s ease, background .2s ease;
  }

  .ib-portfolio .ib-work-card:hover {
    transform: translateY(-3px);
    border-color: #3a5876;
    background: linear-gradient(145deg, #142238, #101b2d);
  }

  .ib-portfolio .ib-work-top {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: .75rem;
    margin-bottom: 1rem;
  }

  .ib-portfolio .ib-work-icon {
    display: grid;
    place-items: center;
    width: 42px;
    height: 42px;
    border-radius: 12px;
    color: var(--ib-accent);
    background: var(--ib-accent-soft);
    border: 1px solid rgba(56, 189, 248, .2);
  }

  .ib-portfolio .ib-arrow {
    color: #71849e;
    transition: color .2s ease, transform .2s ease;
  }

  .ib-portfolio .ib-work-card:hover .ib-arrow {
    color: var(--ib-accent);
    transform: translate(2px, -2px);
  }

  .ib-portfolio .ib-work-card .ib-card-copy { margin-top: .2rem; }

  .ib-portfolio .ib-card-foot {
    display: flex;
    align-items: center;
    gap: .4rem;
    margin-top: auto;
    padding-top: 1.1rem;
    color: #7f93ad;
    font-size: .75rem;
  }

  .ib-portfolio .ib-notes {
    display: grid;
    gap: .75rem;
  }

  .ib-portfolio .ib-note-row {
    display: flex;
    align-items: flex-start;
    gap: .85rem;
    padding: .95rem 1rem;
    border: 1px solid var(--ib-border);
    border-radius: 12px;
    background: rgba(16, 26, 43, .55);
  }

  .ib-portfolio .ib-note-dot {
    width: 8px;
    height: 8px;
    flex: 0 0 8px;
    margin-top: .48rem;
    border-radius: 50%;
    background: var(--ib-accent);
    box-shadow: 0 0 12px rgba(56, 189, 248, .28);
  }

  .ib-portfolio .ib-note-row p {
    margin: 0;
    color: var(--ib-muted);
    font-size: .85rem;
    line-height: 1.7;
  }

  .ib-portfolio .ib-note-row strong {
    color: #dce7f5;
    font-weight: 650;
  }

  .ib-portfolio .ib-footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: .8rem;
    padding-top: 1.2rem;
    border-top: 1px solid #1c293b;
    color: #718198;
    font-size: .76rem;
  }

  .ib-portfolio .ib-footer a { color: #9cb4d0; }
  .ib-portfolio .ib-footer a:hover { color: var(--ib-accent); }

  .ib-portfolio a:focus-visible {
    outline: 2px solid var(--ib-accent);
    outline-offset: 4px;
  }

  @media (max-width: 640px) {
    .ib-portfolio { padding: 1.25rem 1rem 2.5rem; }
    .ib-portfolio .ib-profile { margin-bottom: 2rem; }
    .ib-portfolio .ib-profile-top { align-items: flex-start; }
    .ib-portfolio .ib-avatar { width: 48px; height: 48px; flex-basis: 48px; border-radius: 13px; }
    .ib-portfolio .ib-identity { gap: .75rem; }
    .ib-portfolio .ib-role { font-size: .8rem; }
    .ib-portfolio .ib-github { padding: .58rem .65rem; font-size: .76rem; }
    .ib-portfolio .ib-intro { font-size: .91rem; }
    .ib-portfolio .ib-work-grid { grid-template-columns: 1fr; }
    .ib-portfolio .ib-work-card { min-height: 0; }
    .ib-portfolio .ib-interest { gap: .7rem; padding: .9rem; }
    .ib-portfolio .ib-interest-icon { width: 36px; height: 36px; flex-basis: 36px; }
    .ib-portfolio .ib-label { display: none; }
    .ib-portfolio .ib-footer { align-items: flex-start; flex-direction: column; }
  }

  @media (prefers-reduced-motion: reduce) {
    .ib-portfolio * { scroll-behavior: auto !important; transition: none !important; }
  }
</style>

<div class="ib-portfolio">

  <!-- Profile -->
  <section class="ib-panel ib-profile">
    <div class="ib-profile-top">
      <div class="ib-identity">
        <div class="ib-avatar" aria-hidden="true">
          <i data-lucide="shield-check" style="width:27px;height:27px"></i>
        </div>
        <div>
          <h1 class="ib-name">Ibrahim</h1>
          <p class="ib-role">Systems &amp; AI Security Researcher</p>
        </div>
      </div>
      <a class="ib-github" href="https://github.com/sec-ibrahimx" target="_blank" rel="noopener noreferrer">
        <i data-lucide="github" style="width:16px;height:16px"></i>
        <span>GitHub</span>
        <i data-lucide="arrow-up-right" style="width:13px;height:13px"></i>
      </a>
    </div>

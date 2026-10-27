---
permalink: /
title: ""
author_profile: false
---

<style>
.home-page {
  max-width: 860px;
  margin: 1.5rem auto 3rem;
  color: #dbe5f0;
  font-family: inherit;
  line-height: 1.75;
}

.home-page * {
  box-sizing: border-box;
}

.home-hero {
  padding: 2rem;
  border: 1px solid #26384b;
  border-radius: 18px;
  background: linear-gradient(145deg, #101d2c, #0b1420);
}

.home-kicker {
  margin: 0 0 .65rem;
  color: #5eead4;
  font-size: .78rem;
  font-weight: 700;
  letter-spacing: .14em;
  text-transform: uppercase;
}

.home-page h1 {
  margin: 0;
  color: #f4f8fc;
  font-size: clamp(2rem, 5vw, 3rem);
  line-height: 1.15;
  letter-spacing: -.04em;
}

.home-role {
  margin: .8rem 0 1rem;
  color: #91a9c0;
  font-size: 1.05rem;
}

.home-intro {
  max-width: 660px;
  margin: 0;
  color: #c1cfdd;
  font-size: 1rem;
}

.home-links {
  display: flex;
  flex-wrap: wrap;
  gap: .7rem;
  margin-top: 1.5rem;
}

.home-link {
  display: inline-block;
  padding: .65rem 1rem;
  border: 1px solid #38516a;
  border-radius: 9px;
  color: #e8f4ff !important;
  text-decoration: none !important;
  font-size: .92rem;
  font-weight: 650;
  transition: border-color .18s ease, background .18s ease;
}

.home-link-primary {
  border-color: #14b8a6;
  background: #0f766e;
  color: #ffffff !important;
}

.home-link:hover {
  border-color: #5eead4;
  background: #172a3b;
}

.home-link-primary:hover {
  background: #115e59;
}

.home-section {
  margin-top: 2.2rem;
}

.home-section h2 {
  margin: 0 0 .35rem;
  color: #f1f6fb;
  font-size: 1.35rem;
  letter-spacing: -.02em;
}

.home-section-intro {
  margin: 0 0 1rem;
  color: #91a9c0;
  font-size: .95rem;
}

.home-interest-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: .85rem;
}

.home-interest {
  padding: 1rem 1.1rem;
  border: 1px solid #26384b;
  border-radius: 12px;
  background: #0e1926;
}

.home-interest h3 {
  margin: 0 0 .35rem;
  color: #e6eef7;
  font-size: 1rem;
}

.home-interest p {
  margin: 0;
  color: #9fb1c3;
  font-size: .9rem;
  line-height: 1.65;
}

.home-explore {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: .85rem;
}

.home-explore a {
  display: block;
  padding: 1.1rem;
  border: 1px solid #26384b;
  border-radius: 12px;
  background: #0e1926;
  color: inherit !important;
  text-decoration: none !important;
  transition: border-color .18s ease, transform .18s ease;
}

.home-explore a:hover {
  border-color: #2dd4bf;
  transform: translateY(-2px);
}

.home-explore strong {
  display: block;
  margin-bottom: .25rem;
  color: #e6eef7;
  font-size: 1rem;
}

.home-explore span {
  display: block;
  color: #9fb1c3;
  font-size: .9rem;
}

.home-footer {
  margin-top: 2rem;
  padding-top: 1rem;
  border-top: 1px solid #26384b;
  color: #71879b;
  font-size: .82rem;
}

@media (max-width: 600px) {
  .home-page {
    margin-top: .5rem;
  }

  .home-hero {
    padding: 1.35rem;
  }

  .home-interest-grid,
  .home-explore {
    grid-template-columns: 1fr;
  }
}

@media (prefers-reduced-motion: reduce) {
  .home-page *,
  .home-page *::before,
  .home-page *::after {
    transition: none !important;
    transform: none !important;
  }
}
</style>

<div class="home-page">

  <section class="home-hero">
    <p class="home-kicker">Security Research · Systems · AI</p>
    <h1>Ibrahim</h1>
    <p class="home-role">Systems &amp; AI Security Researcher</p>
    <p class="home-intro">
      Securing systems and AI from the adversary's vantage point through
      empirical offensive research. I explore how systems behave under
      pressure, where security assumptions fail, and how those findings
      can lead to stronger defenses.
    </p>

    <div class="home-links">
      <a class="home-link home-link-primary"
         href="https://github.com/sec-ibrahimx"
         target="_blank" rel="noopener noreferrer">GitHub ↗</a>
      <a class="home-link" href="/research/">Explore Research</a>
      <a class="home-link" href="/blog/">Technical Notes</a>
    </div>
  </section>

  <section class="home-section">
    <h2>Focus &amp; Interests</h2>
    <p class="home-section-intro">
      The areas I study and build in.
    </p>

    <div class="home-interest-grid">
      <article class="home-interest">
        <h3>Security Research &amp; Paper Analysis</h3>
        <p>Examining research methods, validating claims, and understanding practical security implications.</p>
      </article>

      <article class="home-interest">
        <h3>AI Security</h3>
        <p>Exploring threats to AI-enabled systems, model reliability, and ways to evaluate defensive techniques.</p>
      </article>

      <article class="home-interest">
        <h3>Systems &amp; Network Security</h3>
        <p>Studying network behavior, protocols, attack patterns, and the boundaries between systems.</p>
      </article>

      <article class="home-interest">
        <h3>Applied Technical Projects</h3>
        <p>Turning research questions into experiments, prototypes, and measurable technical results.</p>
      </article>
    </div>
  </section>

  <section class="home-section">
    <h2>Explore</h2>
    <p class="home-section-intro">
      Browse the research and technical writing available on this site.
    </p>

    <div class="home-explore">
      <a href="/research/">
        <strong>Research &amp; Analysis ↗</strong>
        <span>Research notes, paper analysis, and security investigations.</span>
      </a>

      <a href="/blog/">
        <strong>Technical Notes ↗</strong>
        <span>Technical write-ups, experiments, and lessons learned.</span>
      </a>
    </div>
  </section>

  <footer class="home-footer">
    Independent security research and practical experimentation.
  </footer>

</div>

---
layout: default
title: Home
---

<div class="profile-container">
  <div class="profile-image">
    <img src="{{ '/assets/images/profile_blurry2.png' | relative_url }}" alt="Michael Wakeham">
  </div>
  <div class="profile-text">
    <h1 style="font-weight: 700;">Michael Wakeham</h1>
    <p>I'm an undergraduate student studying Computer Science at Boston University, currently working with Prof. <a class="custom-link" href="https://boqinggong.github.io/">Boqing Gong</a> and Prof. <a class="custom-link" href="https://deeptigp.github.io/">Deepti Ghadiyaram</a>.</p>
    <p class="profile-para-gap">My research interests lie in computer vision and machine learning. More specifically, I like vision language models, 3D vision, and generative models.</p>
    <p class="profile-links">
      <a class="custom-link" href="mailto:mwakeham@bu.edu">Email</a>
      <span class="link-sep" aria-hidden="true">·</span>
      <a class="custom-link" href="{{ '/assets/images/Michael_Wakeham_CV (1).pdf' | relative_url }}">CV</a>
      <span class="link-sep" aria-hidden="true">·</span>
      <a class="custom-link" href="https://scholar.google.com/citations?user=jHfzgugAAAAJ&amp;hl=en">Google Scholar</a>
      <span class="link-sep" aria-hidden="true">·</span>
      <a class="custom-link" href="https://www.linkedin.com/in/mikewakeham/">LinkedIn</a>
    </p>
  </div>
</div>

{% include research-projects.html %}

<section class="edu-section" aria-labelledby="edu-heading">
  <h2 id="edu-heading" class="research-heading">Education</h2>

  <div class="edu-entry">
    <div class="edu-logo">
      <img src="{{ '/assets/images/boston_university.png' | relative_url }}" alt="Boston University" />
    </div>
    <div class="edu-body">
      <p class="edu-school">Boston University</p>
      <p class="edu-degree">B.A. in Computer Science</p>
      <p class="edu-date">2023 – 2027</p>
    </div>
  </div>
</section>

<style>
  /* ── Global ─────────────────────────────────────── */
  p { margin: 0; }

  /* ── Accent colour ──────────────────────────────── */
  .custom-link            { color: #7b5ea7; text-decoration: none; }
  .custom-link:hover,
  .custom-link:visited:hover { color: #5a4888; text-decoration: underline; }
  .custom-link:visited    { color: #7b5ea7; }

  /* ── Shared separator ───────────────────────────── */
  .link-sep { margin: 0 0.35em; color: #666; }

  /* ── Page wrapper (widen for research section) ──── */
  .page-content .wrapper { max-width: 900px; }

  /* ── Profile block ──────────────────────────────── */
  .profile-container {
    display: flex;
    flex-wrap: wrap;
    align-items: flex-start;
    gap: 40px;
    max-width: 750px;
    margin: 0 auto;
  }
  .profile-image {
    flex: 0 0 300px;
    border-radius: 8px;
  }
  .profile-image img {
    width: 100%;
    height: auto;
    border-radius: 8px;
    display: block;
  }
  .profile-text {
    flex: 1;
    min-width: 200px;
    margin-top: 1rem;
  }
  .profile-para-gap  { margin-top: 1rem; }
  .profile-links     { margin-top: 1rem; line-height: 1.6; margin-left: 2em; }

  /* ── Research section ───────────────────────────── */
  .research-section {
    max-width: 100%;
    margin: 4rem auto 0;
    padding: 0 0 1.5rem;
    box-sizing: border-box;
  }
  .section-hr {
    border: 0;
    height: 1px;
    background-color: #666;
    margin: 0 0 1.5rem;
    display: block;
  }
  .research-heading {
    margin: 0 0 1rem;
    font-size: 1.65rem;
    font-weight: 400;
    line-height: 1.2;
    color: #111;
  }

  /* ── Project cards ──────────────────────────────── */
  .project-card {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem 1.25rem;
    align-items: center;
    margin-bottom: 2rem;
  }
  .project-card:last-of-type { margin-bottom: 0; }

  .project-teaser { flex: 0 0 450px; max-width: 100%; }
  .project-teaser-inner {
    display: block;
    line-height: 0;
    border-radius: 4px;
    overflow: hidden;
    box-shadow: 0 1px 4px rgba(0,0,0,.12);
    background: transparent;
  }
  .project-teaser img { width: 100%; height: auto; display: block; mix-blend-mode: multiply; }
  .project-teaser-video { width: 100%; height: auto; display: block; }

  .project-body  { flex: 1; min-width: 200px; }
  .project-title { margin: 0 0 0.25rem; font-size: 1.05rem; font-weight: 600; line-height: 1.35; }
  .project-venue { margin: 0 0 0.5rem;  font-size: 0.95rem; color: #555; }

  .project-authors     { margin: 0 0 0.4rem; font-size: 0.9rem; line-height: 1.5; color: #333; }
  .project-description { margin: 0 0 0.4rem; font-size: 0.9rem; line-height: 1.5; color: #333; }
  .author-name-self { text-decoration: underline; text-underline-offset: 2px; }
  .author-mark      { font-size: 0.85em; vertical-align: super; line-height: 0; }

  .project-footnote { margin: 0 0 0.5rem; font-size: 0.82rem; color: #666; line-height: 1.4; }
  .project-links {
    margin: 0;
    font-size: 0.92rem;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 0 0.5em;
  }
  .project-links .link-sep { margin: 0; line-height: 1; }

  /* ── Education section ──────────────────────────── */
  .edu-section {
    max-width: 100%;
    margin: 4rem auto 0;
    padding: 0 0 1.5rem;
    box-sizing: border-box;
  }
  .edu-section .research-heading {
    margin-bottom: 2.5rem;
  }
  .edu-entry {
    display: flex;
    align-items: flex-start;
    gap: 1.25rem;
  }
  .edu-body { flex: 1; min-width: 0; }
  .edu-logo {
    flex: 0 0 120px;
  }
  .edu-logo img {
    width: 120px;
    height: 120px;
    object-fit: contain;
    display: block;
    mix-blend-mode: multiply;
  }
  .edu-school { font-weight: 600; font-size: 1rem; margin: 0; color: #111; }
  .edu-degree { font-size: 0.95rem; margin: 0.15rem 0 0; color: #333; }
  .edu-date   { font-size: 0.88rem; margin: 0.1rem 0 0; color: #666; }
</style>

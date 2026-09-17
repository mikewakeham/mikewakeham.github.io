---
layout: default
title: Home
---

<div class="profile-container">
  <div class="profile-image">
    <div class="profile-photo-toggle">
      <img class="profile-photo profile-photo-primary" src="{{ '/assets/images/profile.png' | relative_url }}" alt="Michael Wakeham">
      <img class="profile-photo profile-photo-stadium" src="{{ '/assets/images/white_hart_lane.jpg' | relative_url }}" alt="White Hart Lane">
    </div>
    <span class="profile-photo-caption">White Hart Lane 2017</span>
  </div>
  <div class="profile-text">
    <h1 style="font-weight: 500;">Michael Wakeham</h1>
    <p>Hi! I'm an undergraduate student studying computer science at Boston University, where I work with Prof. <a class="custom-link" href="https://boqinggong.github.io/">Boqing Gong</a> and Prof. <a class="custom-link" href="https://deeptigp.github.io/">Deepti Ghadiyaram</a>. I'm also a visiting research intern at Kempner Institute, working with Prof. <a class="custom-link" href="https://qianqianwang68.github.io/">Qianqian Wang</a> and Dr. <a class="custom-link" href="https://ruojincai.github.io/">Ruojin Cai</a></p>
    <!-- <p class="profile-para-gap">My research interests are in computer vision and machine learning. More specifically, I like 3D vision, vision language models, and generative models</p> -->
    <p class="profile-para-gap">My research interests are in computer vision and machine learning. More specifically, I am interested in understanding, representing, and generating the 4D world from incomplete observation.</p>
    <p class="profile-links">
      <!-- Copyable email UI (disabled; retained in case it is restored later)
      <span class="profile-email">mwakeham@bu.edu</span>
      <button class="copy-email" type="button" aria-label="Copy email address" title="Copy email address" data-copy-email="mwakeham@bu.edu">
        <svg class="copy-email-icon copy-email-icon-copy" aria-hidden="true" viewBox="0 0 24 24">
          <rect width="14" height="14" x="8" y="8" rx="2"></rect>
          <path d="M4 16c-1.1 0-2-.9-2-2V4c0-1.1.9-2 2-2h10c1.1 0 2 .9 2 2"></path>
        </svg>
        <svg class="copy-email-icon copy-email-icon-check" aria-hidden="true" viewBox="0 0 24 24">
          <path d="m20 6-11 11-5-5"></path>
        </svg>
      </button>
      -->
      <a class="custom-link" href="mailto:mwakeham@bu.edu">Email</a>
      <span class="link-sep" aria-hidden="true">·</span>
      <a class="custom-link" href="{{ '/assets/images/Michael_Wakeham_CV.pdf' | relative_url }}">CV</a>
      <span class="link-sep" aria-hidden="true">·</span>
      <a class="custom-link" href="https://scholar.google.com/citations?user=jHfzgugAAAAJ&amp;hl=en">Google Scholar</a>
      <span class="link-sep" aria-hidden="true">·</span>
      <a class="custom-link" href="https://www.linkedin.com/in/mikewakeham/">LinkedIn</a>
    </p>
  </div>
</div>

{% include research-projects.html %}

<!-- Education section (disabled; retained for possible restoration)
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
-->

<style>
  /* ── Global ─────────────────────────────────────── */
  html, body { background-color: #fff; }
  .site-header { border: 0; }
  p { margin: 0; }

  /* ── Accent colour ──────────────────────────────── */
  .custom-link            { color: #7b5ea7; text-decoration: none; }
  .custom-link:hover,
  .custom-link:visited:hover { color: #5a4888; text-decoration: underline; }
  .custom-link:visited    { color: #7b5ea7; }

  /* ── Shared separator ───────────────────────────── */
  .link-sep {
    margin: 0 0.35em;
    color: #666;
    user-select: none;
    -webkit-user-select: none;
  }

  /* ── Page wrapper (widen for research section) ──── */
  .page-content .wrapper { max-width: 990px; }

  /* ── Profile block ──────────────────────────────── */
  .profile-container {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 32px;
    max-width: 985px;
    margin: 0 auto;
  }
  .profile-image {
    flex: 0 0 225px;
    border-radius: 8px;
    position: relative;
  }
  .profile-photo-toggle {
    position: relative;
    display: block;
    width: 100%;
    aspect-ratio: 516 / 484;
    padding: 0;
    border: 0;
    overflow: hidden;
    border-radius: 8px;
    background: none;
    cursor: default;
  }
  .profile-photo {
    position: absolute;
    inset: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
  }
  .profile-photo-primary { opacity: 1; }
  .profile-photo-stadium { opacity: 0; }
  .profile-photo-caption {
    position: absolute;
    top: -1.45rem;
    left: 50%;
    z-index: 1;
    color: #111;
    font-size: 0.9rem;
    line-height: 1.25;
    white-space: nowrap;
    opacity: 0;
    transform: translateX(-50%);
    pointer-events: none;
  }
  .profile-photo-toggle.is-showing-stadium .profile-photo-primary { opacity: 0; }
  .profile-photo-toggle.is-showing-stadium .profile-photo-stadium,
  .profile-photo-toggle.is-showing-stadium + .profile-photo-caption { opacity: 1; }
  .profile-text {
    flex: 1;
    min-width: 200px;
    margin-top: 0.5rem;
  }
  .profile-text h1 { font-size: 2rem; line-height: 1.2; }
  .profile-para-gap  { margin-top: 1rem; }
  .profile-links     { margin-top: 1rem; line-height: 1.6; text-align: left; }
  .profile-links .link-sep { color: #111; }
  /* Copyable email UI styles (disabled; retained for possible restoration)
  .profile-email { color: #555; }
  .copy-email {
    appearance: none;
    border: 0;
    padding: 0;
    margin: 0 0 0 0.18em;
    width: 1.25em;
    height: 1.25em;
    background: none;
    color: #7b5ea7;
    cursor: pointer;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    vertical-align: -0.27em;
    user-select: none;
    -webkit-user-select: none;
  }
  .copy-email-icon {
    width: 18px;
    height: 18px;
    display: block;
    fill: none;
    stroke: currentColor;
    stroke-width: 2;
    stroke-linecap: round;
    stroke-linejoin: round;
  }
  .copy-email-icon-check { display: none; }
  .copy-email.is-copied { color: #7b5ea7; }
  .copy-email.is-copied .copy-email-icon-copy { display: none; }
  .copy-email.is-copied .copy-email-icon-check { display: block; }
  .copy-email:hover { color: #5a4888; }
  .copy-email:focus-visible {
    outline: 2px solid #777;
    outline-offset: 2px;
    border-radius: 2px;
  }
  */

  /* ── Research section ───────────────────────────── */
  .research-section {
    max-width: 100%;
    margin: 2rem auto 0;
    padding: 0 0 1.5rem;
    box-sizing: border-box;
  }
  .section-hr {
    border: 0;
    height: 1px;
    background-color: #d0d0d0;
    margin: 0 0 1.5rem;
    display: block;
  }
  .research-heading {
    margin: 0 0 1rem;
    font-size: 1.5rem;
    font-weight: 400;
    line-height: 1.2;
    color: #111;
  }

  /* ── Project cards ──────────────────────────────── */
  .project-card {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem 1.25rem;
    align-items: flex-start;
    margin-bottom: 2.5rem;
  }
  .project-card:last-of-type { margin-bottom: 0; }

  .project-teaser { flex: 0 0 370px; max-width: 100%; }
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
  .project-authors-unlinked { color: #111; }
  .project-description { margin: 0 0 0.4rem; font-size: 0.9rem; line-height: 1.5; color: #333; }
  .author-name-self { text-decoration: underline; text-underline-offset: 2px; }
  .author-mark      { font-size: 0.85em; vertical-align: super; line-height: 0; }
  .author-toggle {
    color: #666;
    cursor: pointer;
    text-decoration-line: underline;
    text-decoration-style: dashed;
    text-decoration-thickness: 1px;
    text-underline-offset: 2px;
  }
  .author-toggle:hover,
  .author-toggle:focus-visible {
    color: #444;
  }
  .author-toggle:focus-visible {
    outline: 2px solid #777;
    outline-offset: 2px;
    border-radius: 2px;
  }
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
    margin: 3rem auto 0;
    padding: 0 0 1.5rem;
    box-sizing: border-box;
  }
  .edu-section .research-heading {
    margin-bottom: 2rem;
  }
  .edu-entry {
    display: flex;
    align-items: flex-start;
    gap: 1.25rem;
  }
  .edu-body { flex: 1; min-width: 0; }
  .edu-logo {
    flex: 0 0 100px;
  }
  .edu-logo img {
    width: 100px;
    height: 100px;
    object-fit: contain;
    display: block;
    mix-blend-mode: multiply;
  }
  .edu-school { font-weight: 600; font-size: 1rem; margin: 0; color: #111; }
  .edu-degree { font-size: 0.95rem; margin: 0.15rem 0 0; color: #333; }
  .edu-date   { font-size: 0.88rem; margin: 0.1rem 0 0; color: #666; }
</style>

<script>
  document.querySelectorAll('.profile-photo-toggle').forEach(function (button) {
    var resetTimer;

    function showStadium() {
      window.clearTimeout(resetTimer);
      button.classList.add('is-showing-stadium');

      resetTimer = window.setTimeout(function () {
        button.classList.remove('is-showing-stadium');
      }, 2000);
    }

    button.addEventListener('click', showStadium);
  });
</script>

<!-- Copyable email UI script (disabled; retained for possible restoration)
<script>
  document.querySelectorAll('[data-copy-email]').forEach(function (button) {
    button.addEventListener('click', function () {
      navigator.clipboard.writeText(button.dataset.copyEmail).then(function () {
        button.classList.add('is-copied');
        button.setAttribute('aria-label', 'Email address copied');
        button.setAttribute('title', 'Copied');

        window.setTimeout(function () {
          button.classList.remove('is-copied');
          button.setAttribute('aria-label', 'Copy email address');
          button.setAttribute('title', 'Copy email address');
        }, 1500);
      });
    });
  });
</script>
-->

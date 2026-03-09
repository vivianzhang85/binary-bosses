---
layout: post
title: "Plan of Improvements of Friends of Poway Seniors Website"
permalink: /plans/friendsofpowayseniors
---
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Website Improvements — Friends of Poway Seniors</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=DM+Sans:wght@400;500;600&display=swap" rel="stylesheet" />
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --green: #5aab64;
      --green-light: #243d27;
      --gold: #c4993a;
      --dark: #0f1f11;
      --mid: #a8c4ab;
      --bg: #152418;
      --white: #e8f2e9;
      --border: #2a4030;
      --card-bg: #1c3320;
    }

    body {
      font-family: 'DM Sans', sans-serif;
      background: var(--bg);
      color: var(--white);
      min-height: 100vh;
    }

    /* FRONT MATTER / HEADER */
    header {
      background: var(--dark);
      color: var(--white);
      padding: 3rem 2rem 2.5rem;
      position: relative;
      overflow: hidden;
    }

    header::before {
      content: '';
      position: absolute;
      top: -60px; right: -60px;
      width: 300px; height: 300px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(196,153,58,0.18) 0%, transparent 70%);
    }

    .front-matter {
      max-width: 780px;
      margin: 0 auto;
      position: relative;
    }

    .tag {
      display: inline-block;
      font-size: 0.7rem;
      font-weight: 600;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      color: var(--gold);
      border: 1px solid rgba(196,153,58,0.4);
      padding: 0.3rem 0.8rem;
      border-radius: 100px;
      margin-bottom: 1.2rem;
    }

    header h1 {
      font-family: 'Playfair Display', serif;
      font-size: clamp(2rem, 5vw, 3rem);
      font-weight: 900;
      line-height: 1.15;
      margin-bottom: 1rem;
    }

    header h1 span {
      color: var(--gold);
    }

    .meta-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
      gap: 0.5rem 2rem;
      margin-top: 1.5rem;
      padding-top: 1.5rem;
      border-top: 1px solid rgba(255,255,255,0.12);
      font-size: 0.82rem;
    }

    .meta-item label {
      display: block;
      color: rgba(255,255,255,0.45);
      font-size: 0.68rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      margin-bottom: 0.2rem;
    }

    .meta-item span {
      color: rgba(255,255,255,0.85);
      font-weight: 500;
    }

    /* MAIN CONTENT */
    main {
      max-width: 780px;
      margin: 0 auto;
      padding: 3rem 2rem 5rem;
    }

    .section-label {
      font-size: 0.68rem;
      font-weight: 600;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      color: var(--green);
      margin-bottom: 1.2rem;
      display: flex;
      align-items: center;
      gap: 0.6rem;
    }

    .section-label::after {
      content: '';
      flex: 1;
      height: 1px;
      background: var(--border);
    }

    /* IMPROVEMENT CARDS */
    .improvements {
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    .card {
      background: var(--card-bg);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 1.4rem 1.6rem;
      display: grid;
      grid-template-columns: 2.5rem 1fr;
      gap: 0 1rem;
      transition: box-shadow 0.2s, transform 0.2s;
      position: relative;
    }

    .card:hover {
      box-shadow: 0 6px 24px rgba(0,0,0,0.3);
      transform: translateY(-2px);
    }

    .card.priority-high {
      border-left: 4px solid #d94f4f;
    }
    .card.priority-med {
      border-left: 4px solid var(--gold);
    }
    .card.priority-low {
      border-left: 4px solid var(--green);
    }

    .card-num {
      font-family: 'Playfair Display', serif;
      font-size: 1.3rem;
      font-weight: 700;
      color: var(--border);
      line-height: 1;
      padding-top: 2px;
    }

    .card-body h3 {
      font-size: 0.95rem;
      font-weight: 600;
      color: var(--white);
      margin-bottom: 0.35rem;
      line-height: 1.3;
    }

    .card-body p {
      font-size: 0.84rem;
      color: var(--mid);
      line-height: 1.6;
    }

    .priority-badge {
      position: absolute;
      top: 1rem;
      right: 1.2rem;
      font-size: 0.62rem;
      font-weight: 600;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      padding: 0.18rem 0.55rem;
      border-radius: 100px;
    }

    .priority-high .priority-badge { background: rgba(217,79,79,0.2); color: #f08080; border: 1px solid rgba(217,79,79,0.4); }
    .priority-med .priority-badge  { background: rgba(196,153,58,0.2); color: #d4aa60; border: 1px solid rgba(196,153,58,0.4); }
    .priority-low .priority-badge  { background: rgba(90,171,100,0.2); color: var(--green); border: 1px solid rgba(90,171,100,0.4); }

    /* SUMMARY FOOTER */
    .summary {
      margin-top: 3rem;
      background: var(--green-light);
      border: 1px solid #2e5235;
      border-radius: 12px;
      padding: 1.5rem 1.8rem;
    }

    .summary h2 {
      font-family: 'Playfair Display', serif;
      font-size: 1.1rem;
      font-weight: 700;
      color: var(--white);
      margin-bottom: 0.6rem;
    }

    .summary p {
      font-size: 0.84rem;
      color: var(--mid);
      line-height: 1.7;
    }

    .summary strong {
      color: var(--white);
    }
  </style>
</head>
<body>

<header>
  <div class="front-matter">
    <div class="tag">Capstone Project — Website Improvements</div>
    <h1>Planned Improvements for<br /><span>Friends of Poway Seniors</span></h1>
    <div class="meta-grid">
      <div class="meta-item"><label>Organization</label><span>Friends of Poway Seniors</span></div>
      <div class="meta-item"><label>Current Site</label><span>business.poway.com</span></div>
      <div class="meta-item"><label>Date</label><span>March 2026</span></div>
      <div class="meta-item"><label>Status</label><span>In Planning</span></div>
    </div>
  </div>
</header>

<main>

  <div class="section-label">Proposed Changes</div>

  <div class="improvements">

    <div class="card priority-high">
      <span class="priority-badge">High</span>
      <div class="card-num">01</div>
      <div class="card-body">
        <h3>Simplify the Navigation &amp; Dropdown Menus</h3>
        <p>The current "About Us" dropdown has far too many options — <em>Our Mission and Vision, About the Chamber, Meet the Staff, Board of Directors, Committees &amp; Specialty Groups, Testimonials,</em> and <em>Contact</em> — which overwhelms visitors. We'll consolidate these into 2–3 clear links so users can find what they need without being bombarded with choices.</p>
      </div>
    </div>

    <div class="card priority-high">
      <span class="priority-badge">High</span>
      <div class="card-num">02</div>
      <div class="card-body">
        <h3>Reduce Overall Number of Top-Level Nav Items</h3>
        <p>The header navigation contains too many top-level items (About Us, Business Directory, Membership, Community, Events, News &amp; Resources). This clutters the experience. We'll pare it down to the most essential sections and eliminate unecessary sections like business directory.</p>
      </div>
    </div>

    <div class="card priority-high">
      <span class="priority-badge">High</span>
      <div class="card-num">03</div>
      <div class="card-body">
        <h3>Clean Up the Layout &amp; Visual Hierarchy</h3>
        <p>The current page feels unstructured — text blocks, highlights, and images are loosely arranged with no clear visual flow. We'll add consistent spacing, cleaner section headings, and a logical reading order so visitors understand the organization's purpose at a glance.</p>
      </div>
    </div>

    <div class="card priority-med">
      <span class="priority-badge">Medium</span>
      <div class="card-num">04</div>
      <div class="card-body">
        <h3>Add a Clear Call-to-Action Above the Fold</h3>
        <p>Visitors landing on the page have no immediate action to take. We'll add a prominent CTA button — such as "Donate," "Volunteer," or "Get Help" — near the top of the page so users know how to engage right away.</p>
      </div>
    </div>

    <div class="card priority-low">
      <span class="priority-badge">Low</span>
      <div class="card-num">05</div>
      <div class="card-body">
        <h3>Upgrade the Images Section</h3>
        <p>Currently only one small logo image appears in the Images section, which looks unfinished. We'll add real photos of events, volunteers, and seniors served by the organization to build trust and emotional connection with visitors.</p>
      </div>
    </div>

    <div class="card priority-low">
      <span class="priority-badge">Low</span>
      <div class="card-num">06</div>
      <div class="card-body">
        <h3>Improve Contact &amp; Hours Visibility</h3>
        <p>Hours and driving directions are buried mid-page. We'll surface key contact info — phone number, hours, and address — in a more prominent, easy-to-spot section (potentially a sticky sidebar or top banner) so it's more appealing and clearer.</p>
      </div>
    </div>

  </div>

  <div class="summary">
    <h2>Overall Goal</h2>
    <p>
      The Friends of Poway Seniors website has good bones — clear mission, real community impact — but its current design makes it hard to navigate and harder to trust. Our group's improvements focus on three things: <strong>cutting clutter from the menus</strong>, <strong>improving readability and layout</strong>, and <strong>better showcasing the organization's work</strong> so that seniors, donors, and volunteers can all find what they need quickly.
    </p>
  </div>

</main>

</body>
</html>
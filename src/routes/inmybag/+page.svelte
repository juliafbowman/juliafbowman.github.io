<script>
  </script>
  
  <div class="finder-home">
    <h2 class="home-title">Welcome</h2>
    <p class="home-subtitle">
      Use the sidebar to explore different parts of my work and schooling experiences.
    </p>
  
    <div class="home-sections">
      <section class="home-section">
        <h3 class="section-heading">Experience</h3>
        <p class="section-body">
          Browse roles like <strong>Fitch Group</strong> and projects. This section focuses on
          what I’ve built, how I collaborate, and the tools I use in professional and academic settings.
        </p>
      </section>
  
      <section class="home-section">
        <h3 class="section-heading">Academics</h3>
        <p class="section-body">
          See relevant courses, university organizations, and mentorship work. This area highlights
          how my coursework and campus involvement connect to my work both on and off campus.
        </p>
      </section>
  
      <section class="home-section">
        <h3 class="section-heading">Personal</h3>
        <p class="section-body">
          Visit 'In My Bag' to take a peek at the things I carry, read, and enjoy
          outside of classes and work.
        </p>
      </section>
  
      <section class="home-section">
        <h3 class="section-heading">How to Navigate</h3>
        <ul class="section-list">
          <li>Click any item in the left sidebar to switch sections.</li>
          <li>The window title updates at the top to reflect where you are.</li>
          <li>GitHub icons appear where projects have repositories for you to open.</li>
        </ul>
      </section>
    </div>
  </div>
  
  <style>
    .finder-home {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "SF Pro Text",
        sans-serif;
      padding: 16px 20px 20px;
      color: #222;
    }
  
    .home-title {
      font-size: 1.1rem;
      font-weight: 600;
      margin: 0 0 4px 0;
      color: #2b2b2f;
    }
  
    .home-subtitle {
      margin: 0 0 14px 0;
      font-size: 0.9rem;
      color: #55575c;
      max-width: 640px;
      line-height: 1.35;
    }
  
    .home-sections {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px 16px;
    }
  
    .home-section {
      padding: 10px 12px;
      border-radius: 10px;
      border: 1px solid #e4e4e8;
      background-color: #fafafb;
      box-shadow: 0 1px 2px rgba(0, 0, 0, 0.03);
      font-size: 0.88rem;
      line-height: 1.35;
    }
  
    .section-heading {
      margin: 0 0 6px 0;
      font-size: 0.85rem;
      font-weight: 600;
      letter-spacing: 0.04em;
      text-transform: uppercase;
      color: #7b7b80;
    }
  
    .section-body {
      margin: 0;
      color: #44464b;
    }
  
    .section-list {
      margin: 0;
      padding-left: 1.1rem;
      color: #44464b;
      font-size: 0.86rem;
    }
  
    .section-list li {
      margin-bottom: 4px;
    }
  
    @media (max-width: 700px) {
      .home-sections {
        grid-template-columns: 1fr;
      }
  
      .finder-home {
        padding: 12px 14px 18px;
      }
    }
  </style>
  
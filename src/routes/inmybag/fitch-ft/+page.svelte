<script lang="ts">
    const meta = {
      role: "Software Engineer",
      company: "Fitch Group",
      location: "Chicago, IL • Hybrid",
      dates: "Feb 2026 – Present",
      type: "Full-time"
    };

    const highlights = [
      "Details in progress :-)",
      ".",
      ".",
    ];

    const technologies = [
      "Java",
      "Spring Boot",
      "PostgreSQL",
      "REST APIs",
      "GitHub / GitHub Actions",
      "Kafka",
      "Docker",
      "Postman"
    ];
  </script>

  <!-- finder content area -->
  <div class="file-grid fitch-layout">
    <!-- top row -->
    <div class="fitch-meta">
      <div class="meta-section">
        <div class="meta-label">Role</div>
        <div class="meta-value">{meta.role}</div>
      </div>
      <div class="meta-section">
        <div class="meta-label">Type</div>
        <div class="meta-value">{meta.type}</div>
      </div>
      <div class="meta-section">
        <div class="meta-label">Dates</div>
        <div class="meta-value">{meta.dates}</div>
      </div>
    </div>

    <div class="meta-divider"></div>

    <!-- company and location -->
    <div class="fitch-company-line">
      <span class="company-name">{meta.company}</span>
      <span class="dot">•</span>
      <span class="location">{meta.location}</span>
    </div>

    <!-- two column body -->
    <div class="fitch-body">
      <div class="fitch-column">
        <h3 class="fitch-heading">What I do</h3>
        <ul class="fitch-list">
          {#each highlights as item}
            <li>{item}</li>
          {/each}
        </ul>
      </div>

      <div class="fitch-column">
        <h3 class="fitch-heading">Tools & Tech</h3>
        <div class="tag-row">
          {#each technologies as tech}
            <span class="tag">{tech}</span>
          {/each}
        </div>
      </div>
    </div>
  </div>

  <style>
    .fitch-layout {
      display: block;
      padding: 10px 15px;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "SF Pro Text", sans-serif;
      color: #333;
    }

    /* top meta row */
    .fitch-meta {
      display: flex;
      gap: 16px;
      font-size: 0.9rem;
    }

    .meta-section {
      flex: 1;
      min-width: 0;
    }

    .meta-label {
      text-transform: uppercase;
      letter-spacing: 0.06em;
      font-size: 0.7rem;
      color: #9a9a9a;
      margin-bottom: 2px;
    }

    .meta-value {
      font-weight: 500;
      color: #444;
      white-space: pre-line;
    }

    .meta-divider {
      border-bottom: 1px solid #e5e5e5;
      margin: 10px 0 8px 0;
    }

    .fitch-company-line {
      font-size: 0.9rem;
      color: #777;
      margin-bottom: 10px;
    }

    .company-name {
      font-weight: 500;
      color: #555;
    }

    .dot {
      margin: 0 4px;
    }

    .location {
      color: #999;
    }

    /* body area */
    .fitch-body {
      display: flex;
      gap: 24px;
      margin-top: 4px;
    }

    .fitch-column {
      flex: 1;
      min-width: 0;
    }

    .fitch-heading {
      font-size: 0.85rem;
      font-weight: 600;
      color: #888;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      margin: 0 0 6px 0;
    }

    .fitch-list {
      list-style: disc;
      padding-left: 18px;
      margin: 0;
      font-size: 0.9rem;
      line-height: 1.45;
      color: #444;
    }

    .fitch-list li + li {
      margin-top: 4px;
    }

    .tag-row {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      margin-top: 2px;
    }

    .tag {
      font-size: 0.8rem;
      padding: 3px 8px;
      border-radius: 999px;
      background-color: #f2f2f2;
      color: #555;
      border: 1px solid #e2e2e2;
      white-space: nowrap;
    }

    /* small screen tweaks */
    @media (max-width: 768px) {
      .fitch-body {
        flex-direction: column;
        gap: 16px;
      }
    }
  </style>

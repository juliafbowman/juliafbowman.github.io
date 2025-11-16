<script lang="ts">
    import { resolve } from '$app/paths';
    export let title: string = "get to know me";
    console.log("Finder.svelte received title:", title);
  </script>
  
  <main>
    <div class="finder-window">
      <!-- sidebar for finder -->
      <aside class="finder-sidebar">
        <div class="control-lights">
          <div class="light red"></div>
          <div class="light yellow"></div>
          <div class="light green"></div>
        </div>
        <div class="sidebar-content">
          <div class="sidebar-section">
            <h4 class="sidebar-header">Experience</h4>
            <ul class="sidebar-list">
              <li class="sidebar-item">
                <a href={resolve('/inmybag/fitch')}>Fitch Ratings</a>
              </li>
              <li class="sidebar-item">
                <a href={resolve('/inmybag/intern')}>Internship</a>
              </li>
              <li class="sidebar-item">
                <a href={resolve('/inmybag/school-projects')}>Projects</a>
              </li>
            </ul>
          </div>
          <div class="sidebar-divider"></div>
          <div class="sidebar-section">
            <h4 class="sidebar-header">Academics</h4>
            <ul class="sidebar-list">
              <li class="sidebar-item">
                <a href={resolve('/inmybag/relevant-courses')}>Relevant Courses</a>
              </li>
              <li class="sidebar-item">
                <a href={resolve('/inmybag/university-orgs')}>University Orgs</a>
              </li>
              <li class="sidebar-item">
                <a href={resolve('/inmybag/mentor')}>Mentorship</a>
              </li>
            </ul>
          </div>
          <div class="sidebar-divider"></div>
          <div class="sidebar-section">
            <h4 class="sidebar-header">Personal</h4>
            <ul class="sidebar-list">
              <li class="sidebar-item">
                <a href={resolve('/inmybag/bag')}>In My Bag</a>
              </li>
            </ul>
          </div>
        </div>
      </aside>
  
      <div class="finder-content">
        <div class="top-bar">
          <div class="title">
            {title}
          </div>
        </div>
        <div class="content-area">
          <div class="file-grid">
            <slot />
          </div>
        </div>
      </div>
    </div>
  </main>
  
  <style>
    * {
      box-sizing: border-box;
    }
  
    main {
      display: flex;
      justify-content: center;
      padding: 2rem;
      /* background-color: #f5f5f7; */
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "SF Pro Text",
        sans-serif;
      color: #222;
    }
  
    /* prevent weird horizontal scrolling */
    main,
    .finder-window,
    .finder-content,
    .content-area {
      overflow-x: hidden !important;
    }
  
    /* finder window container */
    .finder-window {
      display: flex;
      flex-direction: row;
      width: 850px;
      height: 500px;
      border-radius: 16px;
      border: 1px solid #e2e2e6;
      background-color: #ffffff;
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.08);
      margin: 0 auto;
    }
  
    /* sidebar */
    .finder-sidebar {
      flex: 0 0 200px;
      width: 200px;
      background-color: #f5f5f7;
      border-right: 1px solid #e0e0e4;
      padding: 1rem;
      position: relative;
    }
  
    .sidebar-content {
      margin-top: 30px;
    }
  
    .sidebar-section {
      margin-bottom: 0.6rem;
    }
  
    .sidebar-header {
      font-size: 0.72rem;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      font-weight: 600;
      color: #a0a0a5;
      margin: 0 0 0.15rem 0;
    }
  
    .sidebar-list {
      list-style: none;
      margin: 0;
      padding: 0;
    }
  
    .sidebar-item {
      padding: 0.25rem 0.35rem;
      font-size: 0.95rem;
      color: #333;
      cursor: pointer;
      border-radius: 6px;
      transition: background-color 0.15s ease, color 0.15s ease;
    }
  
    .sidebar-item a {
      text-decoration: none;
      color: inherit;
      display: block;
    }
  
    .sidebar-item:hover,
    .sidebar-item a:hover {
      background-color: #e2e5f0;
      color: #222;
    }
  
    .sidebar-divider {
      border-bottom: 1px solid #e0e0e4;
      margin: 0.65rem 0;
    }
  
    /* window control lights */
    .control-lights {
      display: flex;
      gap: 0.5rem;
      position: absolute;
      top: 16px;
      left: 16px;
    }
  
    .control-lights .light {
      width: 12px;
      height: 12px;
      border-radius: 50%;
      background-color: #ddd;
    }
  
    .control-lights .light.red {
      background-color: #ff605c;
    }
  
    .control-lights .light.yellow {
      background-color: #ffbd44;
    }
  
    .control-lights .light.green {
      background-color: #00ca4e;
    }
  
    /* right side content */
    .finder-content {
      flex-grow: 1;
      display: flex;
      flex-direction: column;
      background-color: #ffffff;
    }
  
    /* top bar in the finder */
    .top-bar {
      display: flex;
      align-items: center;
      justify-content: flex-start;
      background-color: #f8f8fa;
      padding: 0.5rem 1.25rem;
      border-bottom: 1px solid #e3e3e7;
      height: 42px;
    }
  
    .title {
      font-size: 0.95rem;
      font-weight: 600;
      color: #555;
    }
  
    .content-area {
      flex-grow: 1;
      padding: 0; /* inner components decide spacing */
      overflow-y: auto;
      background-color: #ffffff;
    }
  
    /* simple wrapper by default */
    .file-grid {
      width: 100%;
      height: 100%;
    }
  
    /* mobile */
  
    @media (max-width: 768px) {
      main {
        padding: 1.5rem 1rem;
        align-items: center;
      }
  
      .finder-window {
        flex-direction: column;
        width: 100%;
        max-width: 600px;
        height: auto;
        min-height: 400px;
      }
  
      .finder-sidebar {
        width: 100%;
        border-right: none;
        border-bottom: 1px solid #e0e0e4;
        padding-top: 2.5rem;
      }
  
      .control-lights {
        top: 14px;
        left: 16px;
      }
  
      .top-bar {
        justify-content: center;
        padding: 0.4rem 0.75rem;
      }
  
      .content-area {
        padding: 0;
      }
    }
  
    @media (max-width: 480px) {
      main {
        padding: 1rem 0.75rem;
      }
  
      .finder-window {
        max-width: 100%;
        min-height: 360px;
      }
  
      .sidebar-item {
        font-size: 0.9rem;
        padding: 0.25rem 0.25rem;
      }
  
      .title {
        font-size: 0.92rem;
      }
    }
  </style>
  
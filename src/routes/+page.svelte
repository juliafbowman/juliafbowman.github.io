<!-- homepage -->
<script>
    import { asset } from '$app/paths';
  
    let isClosed = false;
    let isCollapsed = false;
    let isZoomed = false;
  </script>
  
  <main>
    <div class="page-container">
      <!-- left and right background flowers -->
      <div class="background">
        <div class="left-image">
          <img src={asset('/flowers/flower1.png')} alt="flower1 :3" />
        </div>
        <div class="left-image2">
          <img src={asset('/flowers/flower2.png')} alt="flower2" />
        </div>
        <div class="left-image3">
          <img src={asset('/flowers/flower3.png')} alt="flower3 :D" />
        </div>
        <div class="left-image4">
          <img src={asset('/flowers/flower18.png')} alt="flower4 :D" />
        </div>
  
        <div class="right-image">
          <img src={asset('/flowers/flower6.png')} alt="flower6 :O" />
        </div>
        <div class="right-image2">
          <img src={asset('/flowers/flower11.png')} alt="flower5 C:" />
        </div>
        <div class="right-image3">
          <img src={asset('/flowers/flower5.png')} alt="flower7 C:" />
        </div>
        <div class="right-image4">
          <img src={asset('/flowers/flower10.png')} alt="flower8 C:" />
        </div>
      </div>
  
      <!-- content -->
      <div class="content">
        {#if !isClosed}
          <div
            class="browser-container"
            class:zoomed={isZoomed}
            class:collapsed={isCollapsed}
          >
            <div class="top-bar">
              <div class="control-lights">
                <!-- red - close window -->
                <button
                  type="button"
                  class="light red"
                  aria-label="Close window"
                  on:click={() => {
                    isClosed = true;
                    isCollapsed = false;
                    isZoomed = false;
                  }}
                ></button>
  
                <!-- yellow - minimize (collapse content) -->
                <button
                  type="button"
                  class="light yellow"
                  aria-label="Minimize window"
                  on:click={() => {
                    isCollapsed = !isCollapsed;
                  }}
                ></button>
  
                <!-- green - zoom -->
                <button
                  type="button"
                  class="light green"
                  aria-label="Zoom window"
                  on:click={() => {
                    isZoomed = !isZoomed;
                  }}
                ></button>
              </div>
              <div class="title">
                {isCollapsed ? 'welcome (minimized)' : 'welcome'}
              </div>
            </div>
  
            <!-- content hides when collapsed -->
            {#if !isCollapsed}
              <div class="browser-box">
                <h1 class="welcome-title">Hi, I'm Julia Bowman</h1>

                <p class="intro-text">
                  Recent graduate from the
                  <strong>University of Illinois Chicago</strong>.
                </p>
                
                <p class="status-text">
                  B.S. in Computer Science · 
                  <span class="graduation" data-tooltip="Graduated Fall 2025">December 2025</span>
                </p>
  
                <hr class="divider" />
  
                <p class="explore-text">Feel free to take a look around :)</p>
              </div>
            {/if}
          </div>
        {:else}
          <button class="reopen-button" on:click={() => (isClosed = false)}>
            reopen window
          </button>
        {/if}
  
        <div class="title-container">
          <a
            href="https://www.linkedin.com/in/juliafbowman/"
            target="_blank"
            class="image-link linkedin"
          >
            <img
              src={asset('/icons/linkedin.png')}
              alt="linkedin logo here..."
              class="link-image linkedin"
            />
          </a>
          <a
            href="https://github.com/juliafbowman"
            target="_blank"
            class="image-link github"
          >
            <img
              src={asset('/icons/github.png')}
              alt="github logo here..."
              class="link-image github"
            />
          </a>
        </div>
      </div>
    </div>
  </main>
  
  <style>
    * {
      box-sizing: border-box;
    }
  
    main {
      font-family: -apple-system, BlinkMacSystemFont, "SF Pro Text", system-ui,
        sans-serif;
      padding: 2rem;
      min-height: 100vh;
    }
  
    .page-container {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 1rem;
      padding: 35px;
      width: 100%;
    }
  
    /* -------------------------
      background flowers
    -------------------------- */
    .background {
      position: absolute;
      inset: 0;
      pointer-events: none;
      z-index: -1;
    }
  
    /* add a littleee opacity to background flowers */
    .left-image {
      position: relative;
      margin-top: 100px;
      top: 30px;
    }
    .left-image img {
      width: 300px;
      transform: translateY(-10%);
      opacity: 0.92;
    }
  
    .left-image2 {
      position: relative;
      margin-left: 30px;
      top: 30px;
    }
    .left-image2 img {
      width: 300px;
      transform: translateY(-20%);
      opacity: 0.88;
    }
  
    .left-image3 {
      position: relative;
      margin-left: 230px;
      top: -370px;
    }
    .left-image3 img {
      width: 250px;
      transform: translateY(-50%);
      opacity: 0.85;
    }
  
    .left-image4 {
      position: relative;
      margin-left: 260px;
      top: -445px;
    }
    .left-image4 img {
      width: 340px;
      transform: translateY(-10%);
      opacity: 0.8;
    }
  
    .right-image img {
      width: 300px;
      transform: translateY(-50%);
      opacity: 0.92;
    }
    .right-image {
      position: absolute;
      top: 55%;
      right: 20px;
      transform: translateY(-50%);
    }
  
    .right-image2 img {
      width: 250px;
      opacity: 0.88;
    }
    .right-image2 {
      position: absolute;
      top: 70%;
      right: 80px;
      transform: translateY(-50%);
    }
  
    .right-image3 img {
      width: 200px;
      opacity: 0.85;
    }
    .right-image3 {
      position: absolute;
      top: 52%;
      right: 270px;
      transform: translateY(-50%);
    }
  
    .right-image4 img {
      width: 300px;
      opacity: 0.8;
    }
    .right-image4 {
      position: absolute;
      top: 10%;
      right: 270px;
      transform: translateY(-50%);
    }
  
    /* -------------------------
           content layout
    -------------------------- */
    .content {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 1.75rem;
      width: 100%;
    }
  
    /* -------------------------
          socials
    -------------------------- */
    .title-container {
      display: flex;
      gap: 1.5rem;
    }
  
    .image-link {
      display: inline-block;
      transition: transform 0.2s ease;
    }
  
    .link-image {
      opacity: 0.6;
      transition: transform 0.25s cubic-bezier(0.34, 1.56, 0.64, 1), 
                  opacity 0.25s ease;
      filter: grayscale(0.2);
    }
  
    .image-link:hover .link-image {
      opacity: 1;
      transform: translateY(-2px) scale(1.08);
      filter: grayscale(0);
    }
  
    .github {
      width: 36px;
    }
    .linkedin {
      width: 40px;
    }
  
    /* -------------------------
          browser window
    -------------------------- */
    .browser-container {
      display: flex;
      flex-direction: column;
      width: 100%;
      max-width: 540px; /* slightly wider */
      border-radius: 18px;
      border: 1px solid #e3e3e8;
      overflow: hidden;
      background: rgba(255, 255, 255, 0.96);
      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08),
                  0 2px 8px rgba(0, 0, 0, 0.04);
      transition: transform 0.18s ease, box-shadow 0.18s ease, opacity 0.18s ease;
    }
  
    .browser-container.zoomed {
      transform: scale(1.03);
      box-shadow: 0 12px 48px rgba(0, 0, 0, 0.12),
                  0 4px 12px rgba(0, 0, 0, 0.06);
    }
  
    /* height collapses, width stays the same bc of maxwidth/width above */
    .browser-container.collapsed .browser-box {
      display: none;
    }
  
    .top-bar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0.65rem 1.1rem;
      background: linear-gradient(to bottom, #fafafa, #f5f5f7);
      border-bottom: 1px solid #e0e0e4;
    }
  
    .control-lights {
      display: flex;
      gap: 0.5rem;
    }
  
    .control-lights .light {
      width: 12px;
      height: 12px;
      border-radius: 50%;
      background-color: #ddd;
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      border: none;
      padding: 0;
      outline: none;
      transition: transform 0.1s ease;
    }
  
    .control-lights .light:focus-visible {
      outline: 2px solid rgba(0, 0, 0, 0.55);
      outline-offset: 2px;
    }
  
    .control-lights .light:active {
      transform: scale(0.88);
    }
  
    .control-lights .light::before,
    .control-lights .light::after {
      content: "";
      position: absolute;
      opacity: 0;
      transition: opacity 120ms ease;
    }
  
    .control-lights:hover .light::before,
    .control-lights:hover .light::after {
      opacity: 0.7;
    }
  
    .control-lights .light.red {
      background-color: #fc635e;
    }
  
    .control-lights .light.red::before {
      content: "×";
      font-size: 10px;
      margin-top: -1px;
      color: rgba(0, 0, 0, 0.65);
    }
  
    .control-lights .light.yellow {
      background-color: #fdbc40;
    }
  
    .control-lights .light.yellow::before {
      content: "–";
      font-size: 12px;
      margin-top: -1px;
      color: rgba(0, 0, 0, 0.65);
    }
  
    .control-lights .light.green {
      background-color: #34c749;
    }
  
    /* top-left arrow (points ↙) */
    .control-lights .light.green::before {
      content: "";
      position: absolute;
      border-style: solid;
      border-width: 4px 4px 0 0;
      border-color: rgba(0, 0, 0, 0.65) transparent transparent transparent;
      transform: translate(-1px, -1px) rotate(0deg);
    }
  
    /* bottom-right arrow (points ↗) */
    .control-lights .light.green::after {
      content: "";
      position: absolute;
      border-style: solid;
      border-width: 0 0 4px 4px;
      border-color: transparent transparent rgba(0, 0, 0, 0.65) transparent;
      transform: translate(1px, 1px) rotate(0deg);
    }
  
    .title {
      font-size: 0.88rem;
      color: #6b6b75;
      font-weight: 500;
      letter-spacing: 0.01em;
    }
  
    /* -------------------------
           inner window 
    -------------------------- */
    .browser-box {
      padding: 1.8rem 2rem;
      background: linear-gradient(
        to bottom,
        rgba(255, 255, 255, 0.98),
        rgba(252, 252, 253, 0.95)
      );
    }
  
    .welcome-title {
      font-size: 1.85rem;
      font-weight: 600;
      color: #3f3f3f;
      margin: 0 0 0.8rem 0;
      letter-spacing: -0.02em;
    }
  
    .intro-text,
    .status-text,
    .explore-text {
      font-size: 1.08rem;
      color: #5c5c66;
      line-height: 1.65;
      margin: 0.5rem 0;
    }
  
    .intro-text strong {
      color: #3a3a44;
      font-weight: 600;
    }
  
    .divider {
      margin: 1.2rem 0;
      border: none;
      border-top: 1px solid #e8e8ec;
    }
  
    /* tooltip text */
    .graduation {
      color: #8b8b98;
      position: relative;
      cursor: pointer;
      border-bottom: 1px dotted #c4c4ce;
      transition: color 0.2s ease, border-color 0.2s ease;
    }
  
    .graduation:hover {
      color: #6b6b78;
      border-bottom-color: #9b9ba8;
    }
  
    .graduation::after {
      content: attr(data-tooltip);
      position: absolute;
      bottom: 135%;
      left: 50%;
      transform: translateX(-50%);
      background: rgba(255, 255, 255, 0.98);
      padding: 0.35rem 0.65rem;
      border-radius: 7px;
      border: 1px solid #dedee4;
      font-size: 0.78rem;
      box-shadow: 0 4px 16px rgba(0, 0, 0, 0.12);
      opacity: 0;
      visibility: hidden;
      transition: 0.2s ease;
      white-space: nowrap;
      pointer-events: none;
      backdrop-filter: blur(8px);
      -webkit-backdrop-filter: blur(8px);
    }
  
    .graduation:hover::after {
      opacity: 1;
      visibility: visible;
      transform: translateX(-50%) translateY(-2px);
    }
  
    .reopen-button {
      border-radius: 999px;
      border: 1px solid #d4d4dc;
      padding: 0.5rem 1.1rem;
      background: rgba(255, 255, 255, 0.92);
      font-size: 0.9rem;
      color: #5c5c66;
      font-weight: 500;
      cursor: pointer;
      box-shadow: 0 6px 20px rgba(0, 0, 0, 0.06);
      backdrop-filter: blur(8px);
      -webkit-backdrop-filter: blur(8px);
      transition: transform 0.2s ease, box-shadow 0.2s ease, opacity 0.2s ease;
      opacity: 0.95;
    }
  
    .reopen-button:hover {
      transform: translateY(-2px);
      box-shadow: 0 8px 28px rgba(0, 0, 0, 0.1);
      opacity: 1;
    }
  
    .reopen-button:active {
      transform: translateY(-1px);
    }
  
    /* -------------------------
        mobile
    -------------------------- */
    @media (max-width: 768px) {
      .page-container {
        flex-direction: column;
        align-items: center;
      }
      .background {
        position: fixed;
        inset: 0;
        z-index: -1;
      }
      .left-image2,
      .left-image3,
      .left-image4,
      .right-image3,
      .right-image4 {
        display: none;
      }
      .browser-container {
        max-width: 100%;
      }
    }
  
    @media (max-width: 480px) {
      .browser-box {
        padding: 1.5rem 1.6rem;
      }
      .welcome-title {
        font-size: 1.5rem;
      }
      .intro-text,
      .status-text,
      .explore-text {
        font-size: 1rem;
      }
    }
  </style>
<!-- homepage -->
<script>
  import { asset } from '$app/paths';
  </script>  

<main>
    <div class="page-container">
      <!-- left + right background flowers -->
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
        <div class="browser-container">
          <div class="top-bar">
            <div class="control-lights">
              <div class="light red"></div>
              <div class="light yellow"></div>
              <div class="light green"></div>
            </div>
            <div class="title">hello</div>
          </div>
  
          <div class="browser-box">
            <h1 class="welcome-title">Welcome</h1>
  
            <p class="intro-text">
              I’m <strong>Julia Bowman</strong>, a Computer Science student at the
              <strong>University of Illinois Chicago</strong>.
            </p>
  
            <p class="status-text">
              Currently at
              <span class="graduation" data-tooltip="Graduation Fall 2025"
                >senior standing</span
              >.
            </p>
  
            <hr class="divider" />
  
            <p class="explore-text">Feel free to take a look around : )</p>
          </div>
        </div>
  
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
      font-family: -apple-system, BlinkMacSystemFont, "SF Pro Text",
      system-ui, sans-serif;
      padding: 2rem;
      min-height: 100vh;
    }
  
    .page-container {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 1rem;
      padding: 35px;
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
  
    .left-image {
      position: relative;
      margin-top: 100px;
      top: 30px;
    }
    .left-image img {
      width: 300px;
      transform: translateY(-10%);
    }
  
    .left-image2 {
      position: relative;
      margin-left: 30px;
      top: 30px;
    }
    .left-image2 img {
      width: 300px;
      transform: translateY(-20%);
    }
  
    .left-image3 {
      position: relative;
      margin-left: 230px;
      top: -370px;
    }
    .left-image3 img {
      width: 250px;
      transform: translateY(-50%);
    }
  
    .left-image4 {
      position: relative;
      margin-left: 260px;
      top: -445px;
    }
    .left-image4 img {
      width: 340px;
      transform: translateY(-10%);
    }
  
    .right-image img {
      width: 300px;
      transform: translateY(-50%);
    }
    .right-image {
      position: absolute;
      top: 55%;
      right: 20px;
      transform: translateY(-50%);
    }
  
    .right-image2 img {
      width: 250px;
    }
    .right-image2 {
      position: absolute;
      top: 70%;
      right: 80px;
      transform: translateY(-50%);
    }
  
    .right-image3 img {
      width: 200px;
    }
    .right-image3 {
      position: absolute;
      top: 52%;
      right: 270px;
      transform: translateY(-50%);
    }
  
    .right-image4 img {
      width: 300px;
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
      gap: 1.5rem;
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
    }
  
    .link-image {
      opacity: 0.65;
      transition: transform 0.2s ease, opacity 0.2s ease;
    }
  
    .link-image:hover {
      opacity: 0.95;
      transform: translateY(-1px) scale(1.06);
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
      max-width: 520px;
      border-radius: 18px;
      border: 1px solid #e3e3e8;
      overflow: hidden;
      background: rgba(255, 255, 255, 0.85);
      backdrop-filter: blur(8px);
      box-shadow: 0 14px 30px rgba(0, 0, 0, 0.07);
    }
  
    .top-bar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0.55rem 1rem;
      background: linear-gradient(to bottom, #fafafa, #f2f2f5);
      border-bottom: 1px solid #dadade;
    }
  
    .control-lights {
      display: flex;
      gap: 0.45rem;
    }
  
    .control-lights .light {
      width: 12px;
      height: 12px;
      border-radius: 50%;
    }
  
    .light.red {
      background-color: #ff605c;
    }
    .light.yellow {
      background-color: #ffbd44;
    }
    .light.green {
      background-color: #00ca4e;
    }
  
    .title {
      font-size: 0.9rem;
      color: #555;
    }
  
    /* -------------------------
           inner window 
    -------------------------- */
    .browser-box {
      padding: 1.4rem 1.6rem;
      background: linear-gradient(
        to bottom,
        rgba(255, 255, 255, 0.98),
        rgba(250, 250, 250, 0.92)
      );
    }
  
    .welcome-title {
      font-size: 1.7rem;
      font-weight: 600;
      color: #505050;
      margin: 0 0 0.6rem 0;
      letter-spacing: -0.01em;
    }
  
    .intro-text,
    .status-text,
    .explore-text {
      font-size: 1.1rem;
      color: #666;
      line-height: 1.5;
      margin: 0.4rem 0;
    }
  
    .intro-text strong {
      color: #4c4c4c;
    }
  
    .divider {
      margin: 1rem 0;
      border: none;
      border-top: 1px solid #e4e4e4;
    }
  
    /* Tooltip text */
    .graduation {
      color: #9696a4;
      position: relative;
      cursor: pointer;
    }
  
    .graduation::after {
      content: attr(data-tooltip);
      position: absolute;
      bottom: 128%;
      left: 50%;
      transform: translateX(-50%);
      background: white;
      padding: 0.25rem 0.5rem;
      border-radius: 6px;
      border: 1px solid #ddd;
      font-size: 0.75rem;
      box-shadow: 0 3px 10px rgba(0, 0, 0, 0.15);
      opacity: 0;
      visibility: hidden;
      transition: 0.15s ease;
    }
  
    .graduation:hover::after {
      opacity: 1;
      visibility: visible;
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
      .welcome-title {
        font-size: 1.4rem;
      }
      .intro-text,
      .status-text {
        font-size: 1rem;
      }
    }
  </style>
  
<script>
    import { resolve } from '$app/paths';
    export let title = "My App";
  
    // split name into two parts
    const [firstPart, secondPart] = title.split(" ");
  </script>
  
  <header>
    <div class="logo">
      <a href="{resolve('/')}" class="title-part first">{firstPart}</a>
      {#if secondPart}
        <a href="{resolve('/')}" class="title-part second">{secondPart}</a>
      {/if}
    </div>
    <nav>
      <ul>
        <li><a href="{resolve('/')}">home</a></li>
        <li><a href="{resolve('/inmybag')}">get to know me</a></li>
        <li><a href="{resolve('/contact')}">contact</a></li>
      </ul>
    </nav>
  </header>
  
  <style>
    header {
      position: sticky;
      top: 0;
      z-index: 1000;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1.1rem 1.75rem;
      background: rgba(255, 255, 255, 0.7);
      backdrop-filter: blur(0px);
      -webkit-backdrop-filter: blur(0px);
      border-bottom: 1px solid rgba(220, 220, 230, 0.7);
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "SF Pro Text",
      sans-serif;
    }
  
    /* logo */
    .logo {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      gap: 0;
    }
  
    .title-part {
      text-decoration: none;
      font-weight: 600;
      letter-spacing: 0.02em;
    }
  
    .title-part.first {
      font-size: 1.55rem;
      color: #55565f;
    }
  
    .title-part.second {
      font-size: 1.5rem;
      color: #9a9aa3;
      text-indent: 10px;
      margin-top: -1.0rem;
    }
  
    .title-part:hover {
      text-decoration: none;
    }
  
    /* nav */
    nav ul {
      list-style: none;
      display: flex;
      gap: 1.3rem;
      margin: 0;
      padding: 0;
      align-items: center;
    }
  
    nav a {
      position: relative;
      text-decoration: none;
      font-size: 0.95rem;
      color: #80808a;
      text-transform: lowercase;
      padding: 0.15rem 0;
      transition: color 0.18s ease;
    }
  
    /* subtle underline on hover */
    nav a::after {
      content: "";
      position: absolute;
      left: 0;
      right: 0;
      bottom: -0.2rem;
      height: 2px;
      border-radius: 999px;
      background: #b4c3ff;
      opacity: 0;
      transform: scaleX(0.7);
      transition: opacity 0.18s ease, transform 0.18s ease;
    }
  
    nav a:hover,
    nav a:focus-visible {
      color: #4f5a9e;
    }
  
    nav a:hover::after,
    nav a:focus-visible::after {
      opacity: 1;
      transform: scaleX(1);
    }
  
    nav a:focus-visible {
      outline: none;
    }
  
    /* mobile */
    @media (max-width: 720px) {
      header {
        flex-direction: column;
        align-items: flex-start;
        padding: 0.9rem 1.1rem;
        gap: 0.4rem;
      }
  
      nav ul {
        gap: 0.9rem;
        flex-wrap: wrap;
      }
  
      nav a {
        font-size: 0.9rem;
      }
    }
  </style>
  
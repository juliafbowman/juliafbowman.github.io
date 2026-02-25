<!-- this is /inmybag/+layout.svelte -->
<script lang="ts">
    import Finder from '$lib/Finder.svelte';
    import { asset } from '$app/paths';
  </script>
  
  <main class="inmybag-main">
    <!-- bg flower -->
    <img
      src={asset('/flowers/flower12.png')}
      alt=""
      class="corner-flower"
    />
  
    <div class="page-container">
      <Finder>
        <slot />
      </Finder>
    </div>
  </main>
  
  <style>
    .inmybag-main {
      font-family: Arial, sans-serif;
      padding: 2rem;
      background-color: transparent;
      position: relative;
      min-height: 100vh;
    }

    @media (max-width: 768px) {
      .inmybag-main {
        padding: 1rem 0.75rem;
      }
    }
  
    .page-container {
      position: relative;
      z-index: 2; /* above the flower */
      background-color: #ffffff00;  /* no color behind finder */
      width: 100%;
    }
  
    .corner-flower {
      position: fixed;
      right: 2rem;
      bottom: -40px;
      right: -10px; 
      width: 350px;
      pointer-events: none;
      z-index: 1; /* between page bg and finder */
    }
  </style>
  
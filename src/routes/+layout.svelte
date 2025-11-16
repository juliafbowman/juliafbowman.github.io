<!-- homepage layout -->
<script>
    import '../app.css'; 
    import Header from '$lib/Header.svelte';
    import { resolve } from '$app/paths';
  </script>

  <svelte:head>
    <title>julia bowman</title>
  </svelte:head>
  
  <Header title="julia bowman" />
    <!-- content from +page.svelte appears here -->
  <slot />
  
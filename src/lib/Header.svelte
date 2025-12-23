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
        padding: 1.2rem 2rem;
        background: rgba(255, 255, 255, 0.765);
        backdrop-filter: blur(0.5px);
        -webkit-backdrop-filter: blur(0.5px);
        border-bottom: 1px solid rgba(220, 220, 230, 0.6);
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
        letter-spacing: 0.01em;
        transition: color 0.2s ease;
    }

    .title-part.first {
        font-size: 1.6rem;
        color: #4a4a54;
    }

    .title-part.first:hover {
        color: #3a3a44;
    }

    .title-part.second {
        font-size: 1.5rem;
        color: #8e8e98;
        text-indent: 10px;
        margin-top: -1.0rem;
    }

    .title-part.second:hover {
        color: #7a7a88;
    }

    /* nav */
    nav ul {
        list-style: none;
        display: flex;
        gap: 1.6rem;
        margin: 0;
        padding: 0;
        align-items: center;
    }

    nav a {
        position: relative;
        text-decoration: none;
        font-size: 0.98rem;
        color: #80808a;
        text-transform: lowercase;
        padding: 0.2rem 0;
        transition: color 0.2s ease;
        /* font-weight: 300; */
    }

    /* subtle underline on hover */
    nav a::after {
        content: "";
        position: absolute;
        left: 0;
        right: 0;
        bottom: -0.25rem;
        height: 2px;
        border-radius: 999px;
        background: linear-gradient(90deg, #a8b6ff 0%, #c4cfff 100%);
        opacity: 0;
        transform: scaleX(0.6);
        transition: opacity 0.25s cubic-bezier(0.34, 1.56, 0.64, 1), 
                    transform 0.25s cubic-bezier(0.34, 1.56, 0.64, 1);
    }

    nav a:hover,
    nav a:focus-visible {
        color: #4a5399;
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
            padding: 1rem 1.3rem;
            gap: 0.5rem;
        }

        nav ul {
            gap: 1.1rem;
            flex-wrap: wrap;
        }

        nav a {
            font-size: 0.92rem;
        }
    }
</style>
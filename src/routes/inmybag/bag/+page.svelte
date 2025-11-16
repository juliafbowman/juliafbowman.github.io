<script lang="ts">
    import { asset } from '$app/paths';
    // items in the window's main content
    const items = [
      { src: asset('/bag-stuff/blueline.png'), alt: "cta pass", caption: "cta-pass.png" },
      { src: asset('/bag-stuff/blackhoney.png'), alt: "liptint", caption: "liptint.png" },
      { src: asset('/bag-stuff/nailfile.png'), alt: "lilac nail file", caption: "nail-file.png" },
      { src: asset('/bag-stuff/headphones.png'), alt: "headphones", caption: "earphones.png" },
      { src: asset('/bag-stuff/wallet.png'), alt: "wallet", caption: "wallet.png" },
      { src: asset('/bag-stuff/bridgeofdreams.png'), alt: "currently reading", caption: "current-read.png" }
    ];
  </script>
  
  <div class="file-grid">
    {#each items as { src, alt, caption }}
      <div class="file-item">
        <div class="outer-frame">
          <div class="inner-frame">
            <img src={src} alt={alt} class="file-thumbnail" />
          </div>
        </div>
        <p class="caption">{caption}</p>
      </div>
    {/each}
  </div>
  
  <style>
.file-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 24px 32px;
  padding: 18px 24px;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "SF Pro Text",
    sans-serif;
}

.file-item {
  width: 96px;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.outer-frame {
  width: 72px;
  height: 72px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.inner-frame {
  width: 100%;
  height: 100%;
  border-radius: 10px;
  border: 1px solid #d5d5d8;
  background-color: #ffffff;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12);
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  padding: 4px;
}

.file-thumbnail {
  max-width: 100%;
  max-height: 100%;
  display: block;
  object-fit: contain;
}

/* filename under icon */
.caption {
  margin-top: 6px;
  padding: 2px 6px;
  max-width: 110px;
  font-size: 0.75rem;
  line-height: 1.2;
  color: #4a4a4f;
  border-radius: 6px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

/* Hover = subtle "selection" */
.file-item:hover .inner-frame {
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.18);
}

.file-item:hover .caption {
  background-color: #dbe3f8;
  color: #1a1a1f;
}

@media (max-width: 600px) {
  .file-grid {
    padding: 12px 12px;
    gap: 18px 20px;
  }

  .file-item {
    width: 84px;
  }

  .outer-frame {
    width: 64px;
    height: 64px;
  }

  .inner-frame {
    padding: 3px; /* slightly smaller padding on mobile */
  }

  .caption {
    font-size: 0.72rem;
    max-width: 96px;
  }
}

  </style>
  
<script lang="ts">
    const items = [
      { name: "WiCS", dateTaken: "2024 - Present", language: "Peer Mentor", link: "/480" },
      { name: "DPI: CAFECS", dateTaken: "2024 - 2025", language: "Mentor", link: "/480" },
    ];
  </script>
  
  <div class="file-container">
    <div class="file-header">
      <div class="header-cell">Organization</div>
      <div class="header-cell">Membership</div>
      <div class="header-cell">Role</div>
    </div>
  
    <div class="file-list">
      {#each items as { name, dateTaken, language }, index}
        <div class="file-row {index % 2 === 0 ? 'even' : 'odd'}">
          <div class="file-cell">{name}</div>
          <div class="file-cell">{dateTaken}</div>
          <div class="file-cell">{language}</div>
        </div>
      {/each}
    </div>
  </div>
  
  <style>
    .file-container {
      width: 100%;
      max-width: 800px;
      margin: -10px 0px ;
      padding: 0;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "SF Pro Text", sans-serif;
      color: #222;
      padding: 10px 0px;
    }
  
    .file-header {
      display: flex;
      align-items: center;
      /* background-color: #f7f7f7; */
      color: #6d6d6d;
      padding: 4px 8px;
      font-size: 0.72rem;
      text-transform: uppercase;
      letter-spacing: 0.06em;
      font-weight: 500;
      border-bottom: 1px solid #e2e2e2;
    }
  
    .header-cell {
      flex: 1;
      padding: 0 8px;
      text-align: left;
    }
  
    .file-list {
      display: flex;
      flex-direction: column;
    }
  
    .file-row {
      display: flex;
      align-items: center;
      padding: 6px 8px;
      /* border-bottom: 1px solid #efefef; */
      transition: background-color 0.15s ease;
      font-size: 0.9rem;
      border-radius: 10px;
    }
  
    .file-row.even { background-color: #ffffff; }
    .file-row.odd  { background-color: #fbfbfb; }
  
    .file-row:hover {
      background-color: #e9edf5;
    }
  
    .file-cell {
      flex: 1;
      padding: 2px 8px;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
    }
  
    .file-row .file-cell:nth-child(2),
    .file-row .file-cell:nth-child(3) {
      color: #777;
    }
  </style>
  
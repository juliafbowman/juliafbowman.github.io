<script lang="ts">
    const items = [
      { name: "Database Systems", dateTaken: "Fall 2025", language: "SQL / MySQL", link: "/480" },
      { name: "Language Design", dateTaken: "Fall 2025", language: "F# / Go", link: "/480" },
      { name: "Systems Programming", dateTaken: "Spring 2025", language: "C", link: "/361" },
      { name: "Computer Design", dateTaken: "Spring 2025", language: "C/C++", link: "/362" },
      { name: "Adv Data Structures", dateTaken: "Spring 2025", language: "Python", link: "/351" },
      { name: "Languages & Automata", dateTaken: "Fall 2024", language: "Theory", link: "/301" },
      { name: "Machine Organization", dateTaken: "Fall 2024", language: "Assembly", link: "/261" },
      { name: "Computer Algorithms I", dateTaken: "Fall 2024", language: "Theory", link: "/401" },
      { name: "Program Practicum", dateTaken: "Spring 2024", language: "C", link: "/211" },
      { name: "Data Structures", dateTaken: "Spring 2024", language: "C++", link: "/251" },
      { name: "Discrete Mathematics", dateTaken: "Fall 2023", language: "Theory", link: "/151" }
    ];
  </script>
  
  <div class="file-container">
    <div class="file-header">
      <div class="header-cell">Course</div>
      <div class="header-cell">Date Taken</div>
      <div class="header-cell">Language</div>
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
  
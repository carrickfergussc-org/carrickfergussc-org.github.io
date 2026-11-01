---
title: "Boat Details"
date: 2026-02-07 16:43:16
status: publish
id: 3998
slug: boat-details
parent: 0
type: page
---

<div id="my-sheet-table"></div>

<script>
  (function() {
    const script = document.createElement('script');
    script.src = 'https://github.com/atkinssk/embed-google-sheet/releases/download/v0.1.0/embed.js';
    script.onload = function() {
      EmbedGoogleSheet({
        csvLink: 'https://docs.google.com/spreadsheets/d/e/2PACX-1vQsgJEzFreRmxigwz7Pcc1UDHYzPjPWSQuzYj1zWCPeGIlipjkRCFtvePaima9AwAIa04KTA0e4d7Pe/pub?gid=1069007327&single=true&output=csv',
        containerId: 'my-sheet-table',
        sortable: true,
        filterable: true
      });
    };
    document.head.appendChild(script);
  })();
</script>
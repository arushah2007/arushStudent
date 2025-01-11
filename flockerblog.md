---
layout: page
title: Sprint 2
description: Home page
hide: true
---

### JavaScript Code: `openGarage` Function

Below is an example of a JavaScript function that can be used to dynamically modify a webpage:

```javascript
<script>
    // Makes function openGarage
    function openGarage() {

        // Selects element "garage-door" & adds "garage-open" CSS class to it
        document.getElementById("garage-door").classList.add("garage-open");

        // Selects element "car-showcase" & adds "showcase-visible" CSS class to it
        document.getElementById("car-showcase").classList.add("showcase-visible");
    }
</script>

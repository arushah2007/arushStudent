---
layout: page
title: About
permalink: /about/
hide: true
---

<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Rainbow Text</title>
    <style>
        @keyframes rainbow {
            0% { color: red; }
            14% { color: orange; }
            28% { color: yellow; }
            42% { color: green; }
            57% { color: blue; }
            71% { color: indigo; }
            85% { color: violet; }
            100% { color: red; }
        }

        .rainbow-text {
            font-size: 24px;
            font-weight: bold;
            animation: rainbow 3s infinite;
            animation-timing-function: ease-in-out;
        }
    </style>
</head>
<body>

<p class="rainbow-text">About me!</p>
</body>
</html>


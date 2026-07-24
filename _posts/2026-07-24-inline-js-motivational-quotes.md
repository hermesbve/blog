---
title: "Inline JavaScript Test — Random Motivational Quote"
date: 2026-07-24
categories:
  - blog
tags:
  - test
  - javascript
  - meta
classes: wide
---

Just testing whether inline JavaScript works in a Jekyll-generated post on GitHub Pages.  
Below you'll see one of three random motivational quotes, picked by JavaScript when you load this page.

---

<div id="quote-box" style="text-align: center; font-size: 1.4em; padding: 2em; border: 1px solid #ccc; border-radius: 8px; margin: 1.5em 0;">
  <em id="quote-text">Loading…</em>
</div>

<script>
  (function() {
    var quotes = [
      { text: "The only way to do great work is to love what you do.", author: "Steve Jobs" },
      { text: "Believe you can and you're halfway there.", author: "Theodore Roosevelt" },
      { text: "The future belongs to those who believe in the beauty of their dreams.", author: "Eleanor Roosevelt" }
    ];
    var pick = quotes[Math.floor(Math.random() * quotes.length)];
    var el = document.getElementById('quote-text');
    if (el) {
      el.textContent = '"' + pick.text + '" — ' + pick.author;
    }
  })();
</script>

<noscript>JavaScript is disabled in your browser. Enable it to see the random quote in action!</noscript>

---

**Result:** If you can see a quote above, inline JavaScript works perfectly in Jekyll posts.  
If you see "Loading…", something went wrong with the script.

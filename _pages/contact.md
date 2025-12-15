---
layout: single
title: "Contact"
permalink: /contact/
author_profile: true
---

If you would like to collaborate, discuss research, or connect about technology and social impact, feel free to reach out.

## Email

<div style="display:flex; gap: .75rem; flex-wrap: wrap; align-items: center;">
  <code id="email-text">mohiuddin.khan.shiam@gmail.com</code>
  <button id="copy-email" class="btn btn--primary" type="button">Copy email</button>
  <span id="copy-status" style="font-size: .95em;"></span>
</div>

## Social

- GitHub: https://github.com/mohiuddin-khan-shiam
- LinkedIn: https://www.linkedin.com/in/s-m-mohiuddin-khan-shiam/
- Google Scholar: https://scholar.google.com/citations?user=PxNOguMAAAAJ
- ResearchGate: https://www.researchgate.net/profile/S-M-Mohiuddin-Khan-Shiam
- ORCID: https://orcid.org/0009-0005-5504-2595
- X: https://x.com/Shiam_ID

<script>
  (function () {
    const btn = document.getElementById('copy-email');
    const text = document.getElementById('email-text');
    const status = document.getElementById('copy-status');

    function setStatus(message) {
      status.textContent = message;
      window.setTimeout(() => {
        status.textContent = '';
      }, 2000);
    }

    async function copyToClipboard(value) {
      if (navigator.clipboard && navigator.clipboard.writeText) {
        await navigator.clipboard.writeText(value);
        return;
      }

      const textarea = document.createElement('textarea');
      textarea.value = value;
      textarea.setAttribute('readonly', '');
      textarea.style.position = 'absolute';
      textarea.style.left = '-9999px';
      document.body.appendChild(textarea);
      textarea.select();
      document.execCommand('copy');
      document.body.removeChild(textarea);
    }

    btn.addEventListener('click', async function () {
      try {
        await copyToClipboard(text.textContent);
        setStatus('Copied.');
      } catch (e) {
        setStatus('Copy failed.');
      }
    });
  })();
</script>

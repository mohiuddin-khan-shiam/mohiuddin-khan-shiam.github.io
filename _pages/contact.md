---
layout: single
title: "Contact & Connect"
permalink: /contact/
author_profile: true
---

I am always delighted to discuss **graduate-level research opportunities**, **Ph.D. positions**, **upstream open-source collaborations**, or **applied machine learning projects**. Please feel free to reach out through any of the channels below.

<div class="contact-card-grid">

  <div class="contact-card contact-card--primary">
    <div class="contact-card__icon"><i class="fa-solid fa-envelope"></i></div>
    <div class="contact-card__body">
      <h3>Primary Email</h3>
      <p class="contact-card__desc">For research inquiries, Ph.D. discussions, and general communication:</p>
      <div class="copy-field">
        <code id="email-primary">mohiuddin.khan.shiam@gmail.com</code>
        <button id="copy-btn-primary" class="btn btn--primary btn--small" type="button" aria-label="Copy primary email"><i class="fa-regular fa-copy"></i> Copy</button>
      </div>
      <span id="status-primary" class="copy-feedback"></span>
    </div>
  </div>

  <div class="contact-card contact-card--academic">
    <div class="contact-card__icon"><i class="fa-solid fa-building-columns"></i></div>
    <div class="contact-card__body">
      <h3>Academic Email</h3>
      <p class="contact-card__desc">Institutional correspondence (BRAC University alumni):</p>
      <div class="copy-field">
        <code id="email-academic">mohiuddin.khan.shiam@g.bracu.ac.bd</code>
        <button id="copy-btn-academic" class="btn btn--info btn--small" type="button" aria-label="Copy academic email"><i class="fa-regular fa-copy"></i> Copy</button>
      </div>
      <span id="status-academic" class="copy-feedback"></span>
    </div>
  </div>

</div>

## Academic & Scientific Identifiers

<div class="identifiers-grid">
  <a href="https://scholar.google.com/citations?user=PxNOguMAAAAJ" target="_blank" rel="noopener noreferrer" class="identifier-pill">
    <i class="ai ai-google-scholar"></i>
    <span><strong>Google Scholar</strong>: Mohiuddin Khan Shiam</span>
  </a>
  <a href="https://orcid.org/0009-0005-5504-2595" target="_blank" rel="noopener noreferrer" class="identifier-pill">
    <i class="ai ai-orcid"></i>
    <span><strong>ORCID</strong>: 0009-0005-5504-2595</span>
  </a>
  <a href="https://www.scopus.com/authid/detail.uri?authorId=60712607800" target="_blank" rel="noopener noreferrer" class="identifier-pill">
    <i class="ai ai-scopus"></i>
    <span><strong>Scopus ID</strong>: 60712607800</span>
  </a>
  <a href="https://www.researchgate.net/profile/S-M-Mohiuddin-Khan-Shiam" target="_blank" rel="noopener noreferrer" class="identifier-pill">
    <i class="fab fa-researchgate"></i>
    <span><strong>ResearchGate</strong>: S-M-Mohiuddin-Khan-Shiam</span>
  </a>
  <a href="https://papers.ssrn.com/sol3/cf_dev/AbsByAuth.cfm?per_id=12781549" target="_blank" rel="noopener noreferrer" class="identifier-pill">
    <i class="ai ai-ssrn"></i>
    <span><strong>SSRN Author ID</strong>: 12781549</span>
  </a>
  <a href="https://sciprofiles.com/profile/mohiuddin-khan-shiam" target="_blank" rel="noopener noreferrer" class="identifier-pill">
    <i class="ai ai-sciprofiles"></i>
    <span><strong>SciProfiles</strong>: mohiuddin-khan-shiam</span>
  </a>
  <a href="https://bracu.academia.edu/shiam" target="_blank" rel="noopener noreferrer" class="identifier-pill">
    <i class="ai ai-academia"></i>
    <span><strong>Academia.edu</strong>: bracu.academia.edu/shiam</span>
  </a>
  <a href="https://figshare.com/authors/S_M_Mohiuddin_Khan_Shiam" target="_blank" rel="noopener noreferrer" class="identifier-pill">
    <i class="ai ai-figshare"></i>
    <span><strong>Figshare</strong>: S_M_Mohiuddin_Khan_Shiam</span>
  </a>
</div>

## Engineering & Development Platforms

<div class="identifiers-grid">
  <a href="https://github.com/mohiuddin-khan-shiam" target="_blank" rel="noopener noreferrer" class="identifier-pill">
    <i class="fab fa-github"></i>
    <span><strong>GitHub</strong>: mohiuddin-khan-shiam</span>
  </a>
  <a href="https://www.linkedin.com/in/s-m-mohiuddin-khan-shiam/" target="_blank" rel="noopener noreferrer" class="identifier-pill">
    <i class="fab fa-linkedin"></i>
    <span><strong>LinkedIn</strong>: s-m-mohiuddin-khan-shiam</span>
  </a>
  <a href="https://huggingface.co/mohiuddin-khan-shiam" target="_blank" rel="noopener noreferrer" class="identifier-pill">
    <i class="fa-solid fa-brain"></i>
    <span><strong>Hugging Face</strong>: mohiuddin-khan-shiam</span>
  </a>
  <a href="https://www.kaggle.com/smmohiuddinkhanshiam" target="_blank" rel="noopener noreferrer" class="identifier-pill">
    <i class="fab fa-kaggle"></i>
    <span><strong>Kaggle</strong>: smmohiuddinkhanshiam</span>
  </a>
  <a href="https://rosalind.info/users/shiam/" target="_blank" rel="noopener noreferrer" class="identifier-pill">
    <i class="fa-solid fa-dna"></i>
    <span><strong>Rosalind</strong>: shiam</span>
  </a>
  <a href="https://x.com/Shiam_ID" target="_blank" rel="noopener noreferrer" class="identifier-pill">
    <i class="fab fa-x-twitter"></i>
    <span><strong>X (Twitter)</strong>: @Shiam_ID</span>
  </a>
  <a href="https://medium.com/@mohiuddin.khan.shiam" target="_blank" rel="noopener noreferrer" class="identifier-pill">
    <i class="fab fa-medium"></i>
    <span><strong>Medium</strong>: @mohiuddin.khan.shiam</span>
  </a>
</div>

<script>
  (function () {
    async function copyText(text, statusElem, buttonElem) {
      try {
        if (navigator.clipboard && navigator.clipboard.writeText) {
          await navigator.clipboard.writeText(text);
        } else {
          const textarea = document.createElement('textarea');
          textarea.value = text;
          textarea.setAttribute('readonly', '');
          textarea.style.position = 'absolute';
          textarea.style.left = '-9999px';
          document.body.appendChild(textarea);
          textarea.select();
          document.execCommand('copy');
          document.body.removeChild(textarea);
        }
        statusElem.textContent = '✓ Copied to clipboard!';
        statusElem.classList.add('copy-success');
        const origHtml = buttonElem.innerHTML;
        buttonElem.innerHTML = '<i class="fa-solid fa-check"></i> Copied';
        setTimeout(() => {
          statusElem.textContent = '';
          statusElem.classList.remove('copy-success');
          buttonElem.innerHTML = origHtml;
        }, 2200);
      } catch (err) {
        statusElem.textContent = 'Copy failed. Please copy manually.';
      }
    }

    const btnPri = document.getElementById('copy-btn-primary');
    const txtPri = document.getElementById('email-primary');
    const stPri = document.getElementById('status-primary');
    if (btnPri && txtPri && stPri) {
      btnPri.addEventListener('click', () => copyText(txtPri.textContent.trim(), stPri, btnPri));
    }

    const btnAca = document.getElementById('copy-btn-academic');
    const txtAca = document.getElementById('email-academic');
    const stAca = document.getElementById('status-academic');
    if (btnAca && txtAca && stAca) {
      btnAca.addEventListener('click', () => copyText(txtAca.textContent.trim(), stAca, btnAca));
    }
  })();
</script>

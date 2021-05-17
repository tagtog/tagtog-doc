---
layout: page
title: OCR
sidebar_link: true
id: ocr
toc: true

api_ocr_url: http://localhost:7000/-ocr
---

<div class="page-section">
  <div class="two-third-col">
    <h2>Introduction</h2>

    <p>OCR (Optical Character Recognition) feature in tagtog is designed to help you transforming scanned documents in PDF format into searchable PDFs.</p>
    
    <p>What does it mean? When you scan a document and store it in PDF format, usually it's scanned PDF - images of whole pages embedded in the document. You can't annotate on it. With tagtog OCR, you can change it, so you can detect text on your scan and annotate!</p>
  </div>
</div>

<div class="page-section">
    <div class="two-third-col">
        <h2>Performing OCR on PDFs <code>POST</code></h2>
        <p>Import PDF scanned document and transform it to searchable PDF.</p>

        <p><strong>Optional Parameters</strong></p>
        <table style="width:100%;">
            <tr>
            <th>Name</th>
            <th>Default</th>
            <th>Example</th>
            <th>Description</th>
            </tr>
            <tr>
            <td><code>format</code></td>
            <td><code>pdf</code></td>
            <td>txt</td>
            <td><p>Format of the result document - it can be either "pdf" or "txt".</p>
            <small>Note: remember to save the document with the same extension as the output format - e.g. if you specify "format=pdf", you can't save the file with ".txt" extension.</small></td>
            </tr>
        </table>
    </div>
</div>

<div class="two-third-col">

  <h4>Examples: perform OCR on PDF</h4>

  <br/>
  <div id="tabs-container">
    <ul class="tabs-menu">
      <li class="current"><a href="#tab-ocr">cURL</a></li>
    </ul>
    <div class="tab">
    <p class="code-desc">This example performs OCR on PDF and stores the result file.</p>

<div id="tab-ocr" class="tab-content" style="display: block" markdown="1">
```shell
curl -X POST -F 'files=@/files/scanned_document.pdf' --output /files/searchable_document.pdf '{{ page.api_ocr_url }}'
```
</div>
</div>
</div>
---
layout: page
title: Foundation News
meta_description: |
  News
permalink: /news
section: news
intro_paragraph: |
  
---

<h5>Stay in the Loop! 🎉 Get the Latest Events & Updates First!</h5>
<div class="container" style="padding:0;">
  <div class="tabs">
    <div class="tab active" data-target="news-email">Email alerts</div>
    <div class="tab" data-target="news-sms">Text alerts</div>
  </div> 
  <div id="news-email" class="tab-content active">
    {% include brevo-email.html %}
  </div>
  <div id="news-sms" class="tab-content">
    {% include brevo-text.html %}
  </div> 
</div>


  <style>
    .tabs {
      display: flex;
      margin-bottom: 1em;
    }
    .tab {
      flex: 1;
      font-size: 18px;
      padding: 10px 20px;
      cursor: pointer;
      border-bottom: 2px solid #555;
      font-weight: 600; 
      text-align: center;
    }
    .tab.active {
      border-bottom: 2px solid #4c70bf;
      background: #f0f0f0;
    }
    .tab:hover {background: #eee;}
    .tab-content {
      display: none;
    }
    .tab-content.active {
      display: block;
    }
  </style>

  <script>
    const tabs = document.querySelectorAll('.tab');
    const contents = document.querySelectorAll('.tab-content');
    tabs.forEach(tab => {
      tab.addEventListener('click', () => {
        tabs.forEach(t => t.classList.remove('active'));
        contents.forEach(c => c.classList.remove('active'));
        tab.classList.add('active');
        document.getElementById(tab.dataset.target).classList.add('active');
      });
    });
  </script>
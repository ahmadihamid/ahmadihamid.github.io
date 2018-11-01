---
layout: page
title: Halaman Belakang
subtitle: Halaman Belakang AhmadiHam.id
comments: true
---

---

  <script>
  (function() {
    var container = document.querySelector('div');
        
    var pageUrl = new URL(window.location);
    var groupParams = halamanbelakang;

    var embedChat = function(chatIndex) {
      var quote = document.createElement('blockquote');
      quote.classList.add('telegram-post');
      quote.dataset.telegramPost = `${groupParams}/${chatIndex}`;
      quote.dataset.width = '100%';
        
      container.appendChild(quote);
    };
    
    var insertJs = function() {
      var script = document.createElement('script');
      script.src = 'https://telegram.org/js/telegram-widget.js';
      script.setAttribute('async', '');
      
      document.body.appendChild(script);
    };
    
    var fromParams = 852;
    var toParams = 893;
    var chatIndexesParams = ;
    
    
    if (groupParams && fromParams && toParams) {
      var from = parseInt(fromParams);
      var to = parseInt(toParams);
      
      for (var chatIndex = from; chatIndex <= to; chatIndex++) {
        embedChat(chatIndex);
      }
      insertJs();
    } else if (groupParams && chatIndexesParams) {
      var chatIndexes = chatIndexesParams.split(',');
      for (var chatIndex of chatIndexes) {
        embedChat(chatIndex.trim());
      }
      insertJs();
    } else {
      container.innerHTML = 'example: https://teleget.neocities.org/?group=pegelounge&from=1&to=10';
    }
  })();
  </script>
---

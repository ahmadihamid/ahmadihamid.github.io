---
layout: page
title: Halaman Belakang
subtitle: Halaman Belakang AhmadiHam.id
comments: true
permalink: /hb
---

---
<html>
  <div></div>
  <script>
  (function() {
    var container = document.querySelector('div');
        
    var pageUrl = new URL(window.location);
    var groupParams = halamanbelakang;

    var embedChat = function(chatIndex) {
      var quote = document.createElement('blockquote');
      quote.classList.add('telegram-post');
      quote.dataset.telegramPost = `${groupParams}`;
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

      var from = parseInt(fromParams);
      var to = parseInt(toParams);
      
      for (var chatIndex = from; chatIndex <= to; chatIndex++) {
        embedChat(chatIndex);
      }
      insertJs();
  })();
  </script>
</html>
---

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
var chatWrapper=document.getElementsByClassName('chat-wrapper')[0],
groupInput=halamanbelakang,
fromInput=851,
toInput=853;

var chatFrom=parseInt(fromInput.value),chatTo=parseInt(toInput.value),chatGroup=groupInput.value;
chatWrapper.innerHTML='';
for(var chatIndex=chatFrom;chatIndex<=chatTo;chatIndex++){var embededChat=document.createElement('script');
embededChat.src='https://telegram.org/js/telegram-widget.js';
embededChat.setAttribute('async','');
embededChat.dataset.telegramPost=`${chatGroup}/${chatIndex}`;
embededChat.dataset.width='100%';chatWrapper.appendChild(embededChat);}});
</script>

</html>
---

---
layout: page
title: Halaman Belakang
subtitle: Halaman Belakang AhmadiHam.id
comments: true
permalink: /hb
---

---
<html>
<div id=“container”></div>
<script>
 var container = document.getElementById('container')
    var username = 'halamanbelakang'
    let start = 1
    let end = 3
    function embedChat(index) {
     let script = document.createElement('script')
        script.src = 'https://telegram.org/js/telegram-widget.js'
        script.setAttribute('async', '')
        script.setAttribute('data-telegram-post', `${username}/${index}`)

        container.appendChild(script)
    }
    for (let index = start; index <= end; index++) {
     embedChat(index)
    }
</script>

</html>
---
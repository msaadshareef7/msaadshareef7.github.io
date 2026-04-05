---
layout: default
title: Contact
---

<div style="text-align:center; margin-top:100px;">
  <h1 id="typing"></h1>

  <p>Email: msaadshareef7@gmail.com</p>
  <p>Instagram: codedrifter</p>
  <p>WhatsApp: 03069821021</p>
  <p>Phone: 03040455975</p>
</div>

<script>
const text = "Stay Connected...";
let i = 0;

function typing(){
  if(i < text.length){
    document.getElementById("typing").innerHTML += text.charAt(i);
    i++;
    setTimeout(typing, 70);
  }
}

typing();
</script>

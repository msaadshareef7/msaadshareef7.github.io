---
layout: default
title: Contact-Me
permalink: /contact/
---

<div class="contact-container">

  <div class="contact-card">

    <h1 id="typing"></h1>

    <div class="contact-item">
      Email: <a href="mailto:msaadsahreef7@gmail.com">msaadsahreef7@gmail.com</a>
    </div>

    <div class="contact-item">
      Instagram: <a href="https://instagram.com/codedrifter" target="_blank">codedrifter</a>
    </div>

    <div class="contact-item">
      WhatsApp: <a href="https://wa.me/923069821021" target="_blank">03069821021</a>
    </div>

    <div class="contact-item">
      Phone: <a href="tel:03040455975">03040455975</a>
    </div>

    <div class="contact-item">
  <i class="fas fa-envelope"></i> 
  <a href="mailto:msaadsahreef7@gmail.com">msaadsahreef7@gmail.com</a>
    </div>

  </div>

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

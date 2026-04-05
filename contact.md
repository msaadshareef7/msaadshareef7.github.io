<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
---
layout: default
title: Contact
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>
body{
  background:#0f172a;
  color:white;
}

.contact-container{
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  margin-top:100px;
  text-align:center;
}

#typing{
  font-size:2.5rem;
  color:#00f2fe;
  font-weight:bold;
}

/* CARD */
.contact-card{
  margin-top:40px;
  background:rgba(255,255,255,0.05);
  backdrop-filter:blur(15px);
  padding:30px;
  border-radius:15px;
  width:320px;
  transition:0.3s;
}

.contact-card:hover{
  transform:translateY(-5px);
}

/* LINKS */
.contact-card a{
  display:flex;
  align-items:center;
  gap:10px;
  margin:15px 0;
  color:white;
  text-decoration:none;
  font-size:1.1rem;
  transition:0.3s;
}

.contact-card a:hover{
  color:#00f2fe;
}

.icon{
  font-size:18px;
}
</style>

<div class="contact-container">
  <div id="typing"></div>

  <div class="contact-card">
    <a href="mailto:msaadshareef7@gmail.com">
      <i class="fas fa-envelope icon"></i> Email
    </a>

    <a href="https://instagram.com/codedrifter" target="_blank">
      <i class="fab fa-instagram icon"></i> Instagram
    </a>

    <a href="https://wa.me/923069821021" target="_blank">
      <i class="fab fa-whatsapp icon"></i> WhatsApp
    </a>

    <a href="tel:03040455975">
      <i class="fas fa-phone icon"></i> Call
    </a>
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

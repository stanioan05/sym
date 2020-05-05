<template>
  <div id="contact">
    <h1 class="title line">Contact Us</h1>
    <form>
      <input class="name" type="text" placeholder="YOUR NAME" />
      <input class="email" type="email" placeholder="YOUR EMAIL" />
      <!-- <input class="tele" type="number" placeholder="your phone number" /> -->
      <textarea class="place" onkeyup="autoGrow(this);" placeholder="YOUR MESSAGE"></textarea>
      <button class="button">Send</button>
    </form>
    <div class="contact-info">
      <div class="card">
        <i class="card-icon far fa-envelope"></i>
        <p>symphonia.software@office.com</p>
      </div>
      <div class="card">
        <i class="card-icon fas fa-phone"></i>
        <p>0768326524</p>
      </div>
      <div class="card">
        <i class="card-icon fas fa-map-marker-alt"></i>
        <p>Bucharest, Romania</p>
      </div>
    </div>
  </div>
</template>
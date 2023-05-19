<template>
<div class="container text-center" id="footer">
  <div class="row" style="padding-top: 20%;">
    <div class="col d-flex align-items-center justify-content-center">
      <p>KONTAK</p>
    </div>
  </div>

  <div class="row">
    <div class="col d-flex align-items-center justify-content-center">
      <a href="https://www.instagram.com/dilectio.ca/" class="instagram" style="color: #0272F4;">Instagram</a>
    </div>
    <div class="col d-flex align-items-center justify-content-center">
      <a href="#" class="email" style="color: white;">lovrisca@student.ub.ac.id</a>
    </div>
  </div>

  <div class="row" style="padding-top: 3%;">
    <div class="col d-flex align-items-center justify-content-center">
      <p class="copyright">@2023 lovrisca</p>
    </div>
  </div>

</div>
</template>

<script>
export default {
    name: 'FooterComponent'
}
</script>

<style>
div {
    font-family: 'PT Sans', 'Roboto', sans-serif;
}
p{
    font-style: normal;
    font-weight: 700;
    font-size: 20px;
    line-height: 26px;
    text-align: center;
    color: #000000;
}
.instagram {
    border: 3px solid #0272F4;
    border-radius: 12px;
    padding-top : 8px;
    padding-bottom: 8px;
    padding-left: 100px;
    padding-right: 100px;
    text-decoration: none;
    
    text-align: center;
    color: #0272F4;
}

.email {
    background: #0272F4;
    border-radius: 12px;
    padding-top : 8px;
    padding-bottom: 8px;
    padding-left: 30px;
    padding-right: 30px;
    text-decoration: none;
}

.copyright {
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 21px;
    text-align: center;
    color: #000000;
}
</style>
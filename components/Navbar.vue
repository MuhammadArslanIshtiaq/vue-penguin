<!-- Please remove this file from your project -->
<template>

  <b-navbar toggleable="lg" class="navbar-background">
    <b-navbar-brand class="align-center" href="#">
      <img src="logo.png" class="d-inline-block align-top logo-img" alt="Kitten">
    </b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav class="m-auto">
        <b-nav-item class="menu_background" href="#">Home</b-nav-item>
        <b-nav-item class="menu_background" href="#">Pengcoin</b-nav-item>
         <b-nav-item class="menu_background" href="#">Guide</b-nav-item>
        <b-nav-item class="menu_background" href="#">Event</b-nav-item>
        <b-nav-item class="menu_background" href="#">F.A.Q</b-nav-item>
      </b-navbar-nav>

      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">

         <a href="#"><img src="arrow.png" class=" align-top arrow d-sm-none d-md-block d-none d-sm-block " alt="Kitten"></a>

      </b-navbar-nav>
    </b-collapse>
  </b-navbar>

</template>
<style>
@font-face {
  font-family: 'minecraft'; ;
  src: url('../static/fonts/MINECRAFTREGULAR-BMG3.otf');
}
.navbar-background{
  background-color: #ff7200;
  height: 20% !important;
}
.logo-img {
   position: absolute;
  z-index: 1;
  top: -1vw;
  width: 20%;
}
.arrow{
   position: absolute;
   right: 5vw;
  width: 10%;
  top: 0vw;
}
.navbar-nav{
  margin-left: 20vw !important;
}

.nav-link{
color: #7d19b9 !important;
}

.menu_background{
  display: inline;
  background: url("../static/menu_button.png") no-repeat ;
  background-size: cover;
  background-position: center;
  margin-left: 5vw;
  padding: 18px 18px;
  font-size: 1.0rem;
  font-family: 'minecraft';


}

  @media only screen and (max-width: 768px) {
   .menu_background{
     background:none;
   }
   .logo-img {
     display: block;
      margin: auto;
      width: 35%;
      position: absolute;
      left: 31%;
}

  }
</style>
<script>

export default {
  name: 'Navbar'
}
</script>

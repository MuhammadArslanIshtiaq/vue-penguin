<!-- Please remove this file from your project -->
<template>

  <b-navbar toggleable="lg" class="navbar-background">
    <b-navbar-brand href="#">
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
    </b-collapse>

    <a href="#"><img src="arrow.png" class=" align-top arrow d-sm-none d-md-block d-none d-sm-block " alt="Kitten"></a>
  </b-navbar>

</template>
<style>
@font-face {
  font-family: 'minecraft'; ;
  src: url('../static/fonts/MINECRAFTREGULAR-BMG3.otf');
}
.navbar-background{
  background-color: #ff7200;
  height: 60px !important;
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
  width: 15%;
  top: -1vw;
}
.navbar-nav{
margin-top: 3.5vh !important;
}

.nav-link{
color: #7d19b9 !important;
}

.menu_background{
  display: inline;
  background: url("../static/menu_button.png") no-repeat ;
  background-size: cover;
  background-position: center;
  padding: 18px 50px;
  font-size: 1.0rem;
  font-weight: bold;
  font-family: 'minecraft';


}

  @media only screen and (max-width: 768px) {
   .menu_background{
     background:none;
   }
   .logo-img {
     display: block;
      margin: auto;
      max-width: 50%;
      position: absolute;
      left: 20%;
      width: auto;
}

.navbar-toggler {
  margin-left: 70vw;
}

  }
</style>
<script>

export default {
  name: 'Navbar'
}
</script>

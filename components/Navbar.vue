<template>
  <div>
    <b-navbar toggleable="lg" class="navbar-background">
      <b-navbar-brand href="#">
        <img
          src="logo.png"
          class="d-inline-block align-top logo-img"
          alt="Kitten"
        />
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="m-auto">
          <b-nav-item class="menu_background" href="#">Home</b-nav-item>
          <b-nav-item class="menu_background" href="#">Guide</b-nav-item>
          <b-nav-item class="menu_background" href="#">F.A.Q</b-nav-item>
          <b-nav-item class="menu_background" v-b-modal.modal-1 v-if="!user">
            Connect
          </b-nav-item>
          <b-nav-item class="menu_background" v-if="user" @click="metamask"
            >Logout</b-nav-item
          >
        </b-navbar-nav>
      </b-collapse>

      <a href="#"
        ><img
          src="arrow.png"
          class="align-top arrow d-sm-none d-md-block d-none d-sm-block"
          alt="Kitten"
      /></a>
    </b-navbar>

    <b-modal id="modal-1" title="Connect Wallets" hide-footer>
      <b-container class="bv-example-row">
        <b-row>
          <b-col cols="12">
            <div class="text-center">
              <b-button class="metamask w-75" @click="metamask"
                >Connect with MetaMask</b-button
              >
            </div>
          </b-col>

          <b-col cols="12" class="mt-3">
            <div class="text-center">
              <b-button variant="primary w-75" @click="connectWallet"
                >Connect with WalletConnect</b-button
              >
            </div>
          </b-col>
        </b-row>
      </b-container>
    </b-modal>
  </div>
</template>
<style>
@font-face {
  font-family: "minecraft";
  src: url("../static/fonts/MINECRAFTREGULAR-BMG3.otf");
}
.navbar-background {
  background-color: #ff7200;
  height: 60px !important;
}
.logo-img {
  position: absolute;
  z-index: 1;
  top: -1vw;
  width: 20%;
}
.arrow {
  position: absolute;
  right: 5vw;
  width: 15%;
  top: -1vw;
}
.navbar-nav {
  margin-top: 3.5vh !important;
}

.nav-link {
  color: #7d19b9 !important;
}

.menu_background {
  display: inline;
  background: url("../static/menu_button.png") no-repeat;
  background-size: cover;
  background-position: center;
  padding: 18px 50px;
  font-size: 1rem;
  font-weight: bold;
  font-family: "minecraft";
}

.metamask {
  background-color: #f6851c !important;
  border-color: #f6851c !important;
}



@media only screen and (max-width: 768px) {
  .menu_background {
    background: none;
    text-align: center;
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
    .navbar-collapse{
    margin-top: 3vw;
    padding: 0;
    width: 800px !important;
  }

  .navbar-background{
    height: auto !important;
  }


}
 @media only screen and  (min-width: 576px) {
    .modal-dialog {
      max-width: 500px;
      margin: 17.75rem auto !important;
    }
  }
</style>
<script>
import Moralis from "moralis";
import Web3 from "web3";
import WalletConnectProvider from "@walletconnect/web3-provider";
const serverUrl = "https://tcqnxk4l54sy.usemoralis.com:2053/server";
const appId = "MH8356RqfyQSJWS8FCfeAhIHOjj1AqEH9U9IDG6T";
Moralis.start({ serverUrl, appId });

export default {
  name: "Navbar",
  data() {
    return {
      user: null,
    };
  },
  methods: {
    connectWallet() {
      Moralis.authenticate({
        provider: "walletconnect",
        mobileLinks: [
          "rainbow",
          "metamask",
          "argent",
          "trust",
          "imtoken",
          "pillar",
        ],
      }).then((user) => {
        this.user = user;
        this.$bvModal.hide("modal-1");
      });
    },
    metamask() {
      if (this.user) {
        Moralis.User.logOut().then(() => {
          this.user = null;
        });
        return;
      }
      Moralis.authenticate().then((user) => {
        this.user = user;
        this.$bvModal.hide("modal-1");
      });
    },
  },
};
</script>

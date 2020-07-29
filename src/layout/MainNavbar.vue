<template>
  <navbar
    position="fixed"
    type="info"
    :transparent="transparent"
    :color-on-scroll="colorOnScroll"
    menu-classes="ml-auto"
  >
    <template>
      <router-link v-popover:popover1 class="navbar-brand" to="/">
        <img height="35" src="/img/banner_logo.png" alt="NACS" class="rounded">
        <!-- <div
          class="image-container"
          style="background-image: url('img/nacs_log_clr.png')"
        ></div>
        ! -->
      </router-link>
      <el-popover
        ref="popover1"
        popper-class="popover"
        placement="bottom"
        width="200"
        trigger="hover"
      >
        <div class="popover-body">
         Niagara Aerial & Civil Services
        </div>
      </el-popover>
    </template>
    <template slot="navbar-menu">
      <li class="nav-item">
          <router-link class="nav-link" :to="{ name: 'photography'}"><p>Photography</p></router-link>
      </li>
      <li class="nav-item">
        <router-link class="nav-link" :to="{ name: 'videography'}"><p>Videography</p></router-link>
      </li>
      <li class="nav-item">
        <router-link class="nav-link" :to="{ name: 'civil'}"><p>Civil</p></router-link>
      </li> 
      <li class="nav-item">
        <router-link class="nav-link" :to="{ name: 'pricing'}"><p>Pricing</p></router-link>
      </li>
      <li class="nav-item">
        <router-link class="nav-link" :to="{ name: 'contact'}"><p>Contact</p></router-link>
      </li>
      <li class="nav-item">
        <a
          class="nav-link"
          rel="tooltip"
          title="Like us on Facebook"
          data-placement="bottom"
          href="https://www.facebook.com/NACS716"
          target="_blank"
        >
          <i class="fab fa-facebook-square"></i>
          <p class="d-lg-none d-xl-none">Facebook</p>
        </a>
      </li>
      <li class="nav-item">
        <a
          class="nav-link"
          rel="tooltip"
          title="Follow us on Instagram"
          data-placement="bottom"
          href="https://www.instagram.com/nacs716"
          target="_blank"
        >
          <i class="fab fa-instagram"></i>
          <p class="d-lg-none d-xl-none">Instagram</p>
        </a>
      </li>
      <li class="nav-item">
        <a
          class="nav-link"
          rel="tooltip"
          title="Follow us on Twitter"
          data-placement="bottom"
          href="https://twitter.com/nacs716"
          target="_blank"
        >
          <i class="fab fa-twitter"></i>
          <p class="d-lg-none d-xl-none">Twitter</p>
        </a>
      </li>
    </template>
  </navbar>
</template>

<script>
import { Navbar} from '@/components';
import { Popover } from 'element-ui';

export default {
  name: 'main-navbar',
  props: {
    transparent: Boolean,
    colorOnScroll: Number
  },
  components: {
    Navbar,
    [Popover.name]: Popover
  },

  methods: {
    goto() {
    	// var element = this.$els[refName];
      // var top = element.offsetTop;
      
      window.scrollTo(100, top);
    }
  }
};
</script>

<style scoped></style>

<template>
  <navbar
    position="fixed"
    type="primary"
    :transparent="transparent"
    :color-on-scroll="colorOnScroll"
    menu-classes="ml-auto"
  >
    <template>
      <router-link v-popover:popover1 class="navbar-brand" to="/">
        NACS
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
        <a
          class="nav-link"
          href=""
          target="_blank"
        >
          <p>Photography</p>
        </a>
      </li>
      <li class="nav-item">
        <a
          class="nav-link"
          href=""
          target="_blank"
        >
          <p>Videography</p>
        </a>
      </li>
      <li class="nav-item">
        <a
          class="nav-link"
          href=""
          target="_blank"
        >
          <p>Civil</p>
        </a>
      </li>
      <li class="nav-item">
        <a           
          class="nav-link"
          href="#pricing"
          target="_blank">
          <p>Pricing</p>
        </a>
      </li>
      <li class="nav-item">
        <a
          class="nav-link"
          href=""
          target="_blank"
        >
          <p>Contact</p>
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

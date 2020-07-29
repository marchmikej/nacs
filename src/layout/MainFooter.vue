<template>
  <footer
    class="footer"
    :class="{ [`footer-${type}`]: type }"
    :data-background-color="backgroundColor"
  >
    <div class="container">
      <nav>
        <ul>
          <li>
            <a href="mailto:nacs716@gmail.com">nacs716@gmail.com</a>
          </li>
          <li>
            <a href="tel:716-479-2927">716.479.2927</a>
          </li>
        </ul>
      </nav>
      <div class="copyright">
        &copy; NACS {{ year }}
      </div>
    </div>
  </footer>
</template>
<script>
export default {
  props: {
    backgroundColor: String,
    type: String
  },
  data() {
    return {
      year: new Date().getFullYear()
    };
  }
};
</script>
<style></style>

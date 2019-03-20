<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-light bg-light navbar-style ">
      <div class="container">
        <button
          class="navbar-toggler"
          type="button"
          data-toggle="collapse"
          data-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav ml-auto">
            <li class="nav-item">
              <a class="nav-link" href="#">How it works</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Login</a>
            </li>
            <li class="nav-item">
              <a class="nav-link">|</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Sign Up</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <br>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  }
};
</script>

<style scoped>
.navbar-style {
  background-color: #ffffff !important;
  box-shadow: 0px 4px 10px 0px rgb(216, 214, 214, 0.8);
}

ul.navbar-list {
  list-style: none;
  display: inline-flex;
  margin-left: 1000px;
  color: #fff;
  /* text-align-last: right */
}
</style>


<template>
  <!--<nav class="c1">
    <a href="" >Home &nbsp; </a> 
    <a href="">Posts &nbsp; </a>
    <a href="">Contact</a>
  </nav>-->

  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <a class="navbar-brand" href="#"></a>
    <span>Logo</span>

    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav mr-auto">

        <li class="w-nav__item">
          <router-link to="/Home" class="nav-item nav-link">
            Home
          </router-link>
        </li>

        <li class="w-nav__item">
          <router-link to="/Sgrade" class="nav-item nav-link">
            Student Grades
          </router-link>
        </li>

        <li class="nav-item dropdown">
          <a
            class="nav-link dropdown-toggle"
            href="#"
            id="navbarDropdown"
            role="button"
            data-toggle="dropdown"
            aria-haspopup="true"
            aria-expanded="false"
          >
            News
          </a>
          <div class="dropdown-menu" aria-labelledby="navbarDropdown"></div>
        </li>
      </ul>
      <form class="form-inline my-2 my-lg-0">
        <input
          class="form-control mr-sm-2"
          type="search"
          placeholder="Search"
          aria-label="Search"
        />
        <button class="btn btn-outline-success my-2 my-sm-0" type="submit">
          Search
        </button>
      </form>
    </div>
  </nav>
</template>

<script>
export default {};
</script>

<style>
.c1 {
  text-align: center;
  border: 3px solid rgb(248, 228, 237);
}

body {
  background-color: rgb(192, 192, 192);
}
</style>
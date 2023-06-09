<template>
  <div class="menu">
    <div class="menu-list">
      <nav class="navbar navbar-expand-lg navbar navbar-light static-top">
        <div class="container-fluid">
          <a href="/"><img class="logo" src="https://i.postimg.cc/QtS1W9tS/Quicloc8-logo.png" alt="logo"></a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
            aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse text-center" id="navbarSupportedContent">
            <ul class="navbar-nav mb-2 mb-lg-0">
              <li class="nav-item">
                <router-link to="/" class="nav-link">Home</router-link>
              </li>
              <li class="nav-item">
                <router-link to="/message" class="nav-link">Messages</router-link>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NavBar'
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}

.menu {
  margin-bottom: 40px;
}

.navbar-collapse {
  justify-content: center;
  align-items: center;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  margin: 0 10px;
}

.logo {
  width: 6em;
}

.menu-list li {
  padding: 0 5px;
}

.menu-list {
  list-style: none;
  font-size: 25px;
}

nav {
  background-color: white;
  box-shadow: 0px 0 10px rgba(1, 0, 0, 0.9);
  text-transform: uppercase;
}

a:hover {
  color: #f14026;
  border-radius: 5px;
}

a.router-link-active {
  color: #f14026;
  border-radius: 5px;
}

.nav-link {
  text-decoration: none;
  color: black;
}
</style>

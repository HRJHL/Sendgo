<!-- src/App.vue -->
<template>
  <div id="app" class="rol">
    <header class="header">
      <nav class="nav">
        <router-link to="/" class="logo">
          <img src="./assets/logo.png" alt="Logo" />
        </router-link>
        <div class="nav-links">
          <router-link to="/message">메시지</router-link>
          <router-link to="/credit">크레딧</router-link>
        </div>
      </nav>
    </header>
    <router-view />
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>

.header {
  padding:10px 20px;
  background-color: white;
  height: 70px;
  display: flex;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 10000;
  border-bottom: 1px solid #84848495;
  overflow-x: hidden;
}

.nav {
  display: flex;
  align-items: center;
  width: 100%;
}

.logo {
  margin-left: 10%;
  margin-right: 10%;
  height: 30px;
}

.logo img {
  height: 30px;
}

.nav-links {
  display: flex;
  gap: 100px;
}
.nav-links a {
  color: black;
  text-decoration: none;
  font-size: 16px;
}

.nav-links a.router-link-active {
  position: relative; 
  color: inherit;
}

.nav-links a.router-link-active::after {
  content: ''; 
  position: absolute; 
  left: -30px;
  bottom: -24px; 
  width: 260%; 
  height: 4px; 
  background-color: blue;
}


@media (max-width: 768px) {
  html,body{
    overflow-x: hidden;
    width: 100%;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
  }

  .header {
    position: fixed;
    z-index: 1000;
    background-color: white;
    height: 70px;
    align-items: center;
    border-bottom: 1px solid #84848495;
  }

.nav-links {
  display: flex;
  gap: 70px;
}

.logo {
  margin-left: 5%;
  margin-right: 10%;
  height: 30px;
}
}

</style>

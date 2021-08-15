<template>
  <header>
    <nav class="container">
      <a href="/">
        <img
          alt="WDEV"
          id="logo"
          src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/wdev.svg
"
      /></a>
      <img
        v-on:click="openMenu"
        alt="Abrir menu"
        id="menu-button"
        src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/menu.svg
"
      />
      <div v-on:click="closeMenu" id="menu-overlay" v-if="menuActive"></div>

      <div id="menu-items" :class="{ active: menuActive }">
        <ul>
          <img
            alt="WDEV"
            id="menu-logo"
            src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/wdev.svg
"
          />

          <li>
            <a href="/"> Home </a>
          </li>
          <li>
            <a href="/videos"> Videos </a>
          </li>
          <li>
            <a href="/sobre"> Sobre </a>
          </li>
          <li>
            <a href="/contato"> Contato </a>
          </li>
        </ul>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      menuActive: false,
    };
  },
  methods: {
    openMenu() {
      this.menuActive = true;
    },
    closeMenu() {
      this.menuActive = false;
    },
  },
};
</script>

<style scoped>
header {
  background-color: var(--color-background-nav);
  width: 100%;
  height: 50px;
  display: flex;
  justify-content: center;
  align-items: center;
}
nav {
  display: flex;
  justify-content: space-between;
}

#logo {
  width: 130px;
}

#menu-button {
  width: 30px;
}

nav {
  display: flex;
  justify-content: space-between;
  height: 60px;
  align-items: center;
}

#menu-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 40%;
  height: 100vh;
  background-color: #000;
  opacity: 0.8;
}

#menu-logo {
  width: 110px;
}
#menu-items {
  position: fixed;
  top: 0;
  right: 0;
  background-color: var(--color-background-nav);
  width: 60%;
  height: 100vh;
  display: none;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
}

#menu-items.active {
  display: flex;
}

ul {
  list-style: none;
}

ul li {
  margin: 20px 0px;
}

ul li a {
  color: var(--color-text-light);
}

@media (min-width: 700px) {
  #menu-button,
  #menu-logo,
  #menu-overlay {
    display: none;
  }
  #menu-items {
    display: flex;
    position: static;
    height: 50px;
    width: auto;
  }
  ul {
    display: flex;
    height: 60px;
    align-items: center;
  }
  ul li {
    margin: 0;
    margin-left: 20px;
  }
}
</style>

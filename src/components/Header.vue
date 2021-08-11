<template>
  <header>
    <nav>
      <a href="/">
        <img
          alt="WDEV"
          id="logo"
          src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/wdev.svg
"
      /></a>
      <img
        alt="Abrir menu"
        id="menu-button"
        src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/menu.svg
"
      />
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
header {
  background-color: var(--color-background-nav);
  width: 100%;
  heighy: 50px;
}
nav {
  display: flex;
  justify-contnt: space-between;
}

#logo {
  width: 130px;
}

#menu-button {
  width: 30px;
}

.container {
  width: 30%;
}
</style>

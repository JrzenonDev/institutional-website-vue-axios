<template>

  <header>

    <nav class="container">

      <a href="/">
        <img id="logo" src="../assets/images/logo.png" alt="Logo">
      </a>

      <img
        id="menu-button"
        src="../assets/images/menu.svg"
        alt="Abrir menu"
        @click="openMenu"
      >

      <div
        id="menu-overlay"
        v-if="menuActive"
        @click="closeMenu"
      >
      </div>

      <div
        id="menu-items"
        :class="{active:menuActive}"
      >
        <img id="menu-logo" src="../assets/images/logo.png" alt="Logo">
        <ul>
          <li><a href="/">Home</a></li>
          <li><a href="/">Sobre</a></li>
          <li><a href="/">Vídeos</a></li>
          <li><a href="/">Contato</a></li>
        </ul>
      </div>

    </nav>

  </header>

</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      menuActive: false
    }
  },
  methods: {
    openMenu: function() {
      this.menuActive = true;
    },
    closeMenu: function() {
      this.menuActive = false;
    }
  }
}
</script>

<style scoped>
  header {
    background-color: var(--color-background-nav);
    width: 100%;
    height: 60px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  nav {
    display: flex;
    justify-content: space-between;
    height: 60px;
    align-items: center;
  }

  #logo {
    height: 50px;
  }

  #menu-button {
    width: 40px;
  }

  .container {
    width: 90%;
  }

  #menu-overlay {
    top: 0;
    left: 0;
    position: fixed;
    width: 40%;
    height: 100vh;
    background-color: var(--color-black);
    opacity: 0.8;
  }

  #menu-logo {
    width: auto;
    height: auto;
    max-width: 55px;
    max-height: 50px;
    margin-top: 30px;
    margin-bottom: 10px;
  }

  #menu-items {
    position: fixed;
    top: 0;
    right: 0;
    width: 60vh;
    height: 100vh;
    background-color: var(--color-background-nav);
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
    text-align: center;
  }

  ul li {
    margin: 20px 0px;
  }

  ul li a {
    color: var(--color-text-light);
  }

  @media (min-width: 700px) {

    #menu-button, #menu-logo, #menu-overlay {
      display: none;
    }

    #menu-items {
      display: flex;
      position: static;
      height: 60px;
      width: auto;
    }

    ul {
      display: flex;
      height: 50px;
      align-items: center;
    }

    ul li {
      margin: flex;
    }

    ul li {
      margin: 0;
      margin-left: 20px;
    }

  }

</style>
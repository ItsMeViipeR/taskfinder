<template>
  <header class="header">
    <div class="logo">TaskFinder</div>
    <nav :class="{ nav: true, active: isMenuOpened }">
      <ul>
        <li><a href="#">Home</a></li>
      </ul>
    </nav>
    <div
      :class="{ 'menu-toggle': true, open: isMenuOpened }"
      @click="toggleMenu"
    >
      <span></span>
      <span></span>
      <span></span>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      isMenuOpened: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpened = !this.isMenuOpened;
    },
  },
};
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  background: linear-gradient(90deg, #3e66c3, #132445);
  color: #fff;
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 1000;
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
}

.nav ul {
  display: flex;
  list-style: none;
}

.nav ul li {
  margin-left: 1.5rem;
}

.nav ul li a {
  color: #fff;
  text-decoration: none;
  font-size: 1rem;
  transition: color 0.3s;
}

.nav ul li a:hover {
  color: #ff4081;
}

.menu-toggle {
  display: none;
  flex-direction: column;
  cursor: pointer;
}

.menu-toggle span {
  width: 25px;
  height: 3px;
  background: #fff;
  margin: 4px 0;
  transition: all 0.3s;
}

.menu-toggle.open span:nth-child(1) {
  transform: rotate(45deg) translate(5px, 10px);
}

.menu-toggle.open span:nth-child(2) {
  opacity: 0;
}

.menu-toggle.open span:nth-child(3) {
  transform: rotate(-45deg) translate(5px, -10px);
}

@media (max-width: 768px) {
  .nav {
    display: none;
  }

  .nav ul {
    flex-direction: column;
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    background: linear-gradient(90deg, #4b6cb7, #182848);
  }

  .nav ul li {
    margin: 1rem 0;
    text-align: center;
  }

  .menu-toggle {
    display: flex;
  }

  .nav.active {
    display: flex;
  }
}
</style>

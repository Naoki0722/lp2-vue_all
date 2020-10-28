<template>
  <header>
    <div class="header-b">
      <h1 class="header-title">estra inc.</h1>
      <nav class="header-nav">
        <ul>
          <li><a href="#">home</a></li>
          <li><a href="#">about</a></li>
          <li><a href="#">service</a></li>
          <li><a href="#">works</a></li>
          <li><a href="#">price</a></li>
          <li><a href="#" @click="contactpage">contact</a></li>
        </ul>
      </nav>
    </div>
    <div id="hamburger" @click="humberger()" :class="{'active':isClass}">
      <span></span>
      <span></span>
      <span></span>
    </div>
    <div class="humberger-menu" :class="{'open':isClass}">
      <p class="menu-title">estra.inc</p>
      <ul>
        <li>
          <a href="#">home</a>
        </li>
        <li>
          <a href="#">about</a>
        </li>
        <li>
          <a href="#">service</a>
        </li>
        <li>
          <a href="#">works</a>
        </li>
        <li>
          <a href="#">price</a>
        </li>
        <li>
          <a href="#">contact</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      isClass: false
    }
  },
  methods: {
    humberger() {
      this.isClass = !this.isClass;
    },
    contactpage() {
      let a = document.documentElement;
      let y = a.scrollHeight - a.clientHeight;
      window.scrollTo({
        top: y,
        left: 0,
        behavior: 'smooth'
      });
    }
  }
}
</script>

<style scoped>
.header-b {
  background-color: black;
  height: 100px;
  color: white;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.header-title {
  margin: 30px;
}

.header-nav ul {
  display: flex;
}

.header-nav li {
  margin: 0 15px;
  list-style: none;
}

.header-nav a {
  color: white;
  text-decoration: none;
}

.humberger-menu {
  display: none;
}

@media screen and (max-width: 768px) {
  #hamburger {
    width: 40px;
    height: 40px;
    position: absolute;
    top: 30px;
    right: 20px;
    cursor: pointer;
    transition: 0.5s;
  }

  #hamburger span {
    height: 2px;
    width: 80%;
    background-color: white;
    position: absolute;
    left: 2px;
  }

  #hamburger span:nth-last-of-type(1){
    top: 10px;
  }
  #hamburger span:nth-last-of-type(2){
    top: 20px;
  }
  #hamburger span:nth-last-of-type(3){
    top: 30px;
  }

  .header-nav {
    display: none; /* デスクトップのナビを消す */
  }

  .humberger-menu {
    display: block;
    position: fixed;
    top: 0;
    left: calc(-100% - 80px);
    z-index: 999;
    height: 100%;
    transition: 0.5s;
  }
  .humberger-menu.open {
    width: calc(100% - 80px);
    height: 100%;
    left: 0;
    background-color: rgb(207, 236, 203);
    box-shadow: 80px 0 rgba(38, 98, 213, 0.3);
  }
  .menu-title {
    font-size: 40px;
    margin: 30px 15px 50px;
    font-weight: bold;
  }
  .humberger-menu li {
    width: 60%;
    margin: 5% 5% 10%;
    padding-bottom: 10px;
    list-style: none;
    text-decoration: none;
    border-bottom: 2px solid blue;
  }

  .humberger-menu li a{
    font-size: 30px;
    color: blue;
    /* margin: 5% ; */
    list-style: none;
    text-decoration: none;
  }
}
</style>
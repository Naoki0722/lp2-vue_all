<template>
  <footer>
    <div class="footer-b">
      <h1 class="footer-title">estra inc.</h1>
      <nav class="footer-nav">
        <ul>
          <li><a href="#">home</a></li>
          <li><a href="#">about</a></li>
          <li><a href="#">service</a></li>
          <li><a href="#">works</a></li>
          <li><a href="#">price</a></li>
          <li><a href="#">contact</a></li>
        </ul>
      </nav>
    </div>
    <div class="foooter-info">
      <small>Copyright 2019 estra inc. All Rights Reserved.</small>
    </div>
  </footer>
</template>

<style scoped>
.footer-b {
  background-color: black;
  height: 100px;
  color: white;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

.footer-title {
  margin: 30px 0;
}

.footer-nav ul {
  display: flex;
  flex-wrap:wrap;
}

.footer-nav li {
  margin: 0 15px;
  list-style: none;
}

.footer-nav a {
  color: white;
  text-decoration: none;
}

.foooter-info {
  background-color: black;
  color: white;
  font-size: 13px;
  padding-bottom: 15px;
  text-align: center;
}

@media screen and (max-width: 768px) {
  .footer-nav {
    display: none; /* デスクトップのナビを消す */
  }

  .footer-title {
    margin: 0 auto;
  }

}
</style>
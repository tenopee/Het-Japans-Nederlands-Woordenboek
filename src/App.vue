<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router';
import SearchBox from './components/SearchBox.vue';
</script>

<template>
  <header>
    <div class="header-wrap">
      <img src="@/assets/logo.svg" alt="日蘭辞書 ロゴ" width="40" height="40" />
      <SearchBox></SearchBox>
    </div>
  </header>
  <nav>
    <ul>
      <li>
        <RouterLink to="/" class="icn home">home</RouterLink>
        <RouterLink to="/search" class="icn search">search</RouterLink>
      </li>
    </ul>
  </nav>
  <RouterView />
  <footer>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@24,400,0,0" />
    <div class="footer__wrap">
      <img src="@/assets/logo.svg" alt="日蘭辞書 ロゴ" width="30" height="30" />
      <div role="navigation">
        <ul>
          <li>
            <RouterLink to="/"><span class="icn-text-base icn-home">home</span></RouterLink>
            <RouterLink to="/search"><span class="icn-text-base icn-home"></span></RouterLink>
          </li>

        </ul>
      </div>
      <p class="">futta</p>
    </div>
  </footer>
</template>

<style scoped>
.header-wrap {
  display: grid;
  grid-template-rows: 1fr;
  grid-template-columns: 60px 600px auto;
  align-items: center;
  height: 40px;
  padding: 8px 30px;
  box-sizing: initial;
}
nav {
  background-color: var(--bgc-nav);
}

.icn-home {
  display: block;
  padding-top: 40px;
}
.icn-home::before {
  top: 0;
  right: 0;
  left: 0;
  width: 20px;
  height: 20px;
  margin: auto;
  background-color: #4e4e4e;
  mask: url("./assets/icn_home.svg") top center / 20px no-repeat;
}

/* @media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
  .footer__wrap {
    display: flex;
  }
} */
</style>

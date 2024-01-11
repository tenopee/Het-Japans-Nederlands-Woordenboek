<script setup lang="ts">

// function searchTextPaste(e) {
//   console.log(e.target.value + 'paste');
// }

// export default class Form extends Vue {
//   private message: string = ""

//   private searchTextKeydown(e): void{
//     this.disabled = true
//     console.log(e.target.value)
//   }
//   private deleteText(e): void{
//     this.disabled = true
//     console.log(e.target.value)
//   }
// }
</script>

<template>
  <search>
      <div class="search-box-wrap">
        <input type="text" placeholder="調べたい" class="search-box">
        <button title="削除" class="icn-text-base close-btn" aria-label="削除" aria-hidden="true"></button>
        <button title="検索" class="icn-text-base search-btn" aria-label="検索"></button>
      </div>
    </search>
</template>

<style scoped>
search {
  height: 100%;
}
.search-box-wrap {
  display: grid;
  grid-template-columns: 1fr 46px;
  height: 100%;
  position: relative;
  /* background: var(--bc-form); */
  border: 4px solid #154273;
  border-radius: 20px;
}
.search-box {
  padding: 0 46px 0 20px;
  border-radius: 20px;
  z-index: 200;
}
.close-btn[aria-hidden="false"] {
  position: absolute;
  top: 0;
  right: 60px;
  bottom: 0;
  width: 20px;
  height: 20px;
  margin: auto;
  z-index: 300;
}
.close-btn[aria-hidden="false"]::before {
  top: 0;
  left: 0;
  width: 20px;
  height: 20px;
  background-color: #154273;
  mask: url("../assets/icn_close.svg") center / 20px no-repeat;
}
.search-btn {
  position: absolute;
  top: -1px;
  right: 0;
  width: 62px;
  height: 34px;
  border-radius: 0 8px 8px 0;
  background-color: #154273;
}
.search-btn::before {
  top: 0;
  bottom: 0;
  right: 12px;
  width: 22px;
  height: 22px;
  margin: auto;
  background-color: #ffffff;
  mask: url("../assets/icn_search.svg") center / 22px no-repeat;
}
@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>

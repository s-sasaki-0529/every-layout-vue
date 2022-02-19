<template>
  <div class="sidebar-wrapper">
    <div class="sidebar">
      <slot name="sidebar"></slot>
    </div>
    <div class="not-sidebar">
      <slot name="not-sidebar"></slot>
    </div>
  </div>
</template>

<style scoped>
.sidebar-wrapper {
  /* 通常は横並びにするが、収まらない場合に折返しを許容することでレスポンシブに*/
  display: flex;
  flex-wrap: wrap;
}
.sidebar {
  /* サイドバーの理想サイズは 30ch とするが、横幅に過不足がある場合は増減できる*/
  flex-basis: 30ch;
  flex-grow: 1;
  flex-shrink: 1;
  background-color: gray;
}
.not-sidebar {
  /* サイドバーと幅の取り合いになった場合に、優先的にスペースをもらえるように flex-grow を高く設定 */
  flex-basis: 0;
  flex-grow: 9999;
  flex-shrink: 1;
  background-color: #ccc;
}
</style>

<template>
  <div class="heading">
    <h2 class="section-title" v-html="title"></h2>
    <div class="line"></div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
  },
};
</script>

<style lang="scss" scoped>
.heading {
  display: flex;
  align-items: center;

  h2.section-title {
    font-family: "Sen";
    font-size: 1.8rem;
    font-weight: 600;
    padding: 10px 10px 10px 0;

    &:before {
      content: "#";
      color: var(--font-color-light);
      padding-right: 5px;
    }
  }
  .line {
    flex: 1;
    height: 1px;
    background: var(--colour-pink);
  }

  @include respond-below(sm) {
    flex-direction: column;
    align-items: stretch;

    .line {
      flex: none;
      height: 1px;
    }
  }
}
</style>

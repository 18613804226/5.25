<template>
  <div class="item" @click="fn">
    <span v-if="flag">
      <slot name="img1"></slot>
    </span>
    <span v-else>
      <slot name="img2"></slot>
    </span>
    <p :class="{green:!flag}">{{txt}}</p>
  </div>
</template>

<script type="text/ecmascript-6">
export default {
  data() {
    return {};
  },
  components: {},
  props: ["txt", "currChild", "mask"],
  computed: {
    flag() {
      if (this.currChild == this.mask) {
        return false;
      }
      return true;
    }
  },
  methods: {
    fn() {
      this.$emit("change", this.mask);
      this.$router.push("/" + this.mask);
    }
  }
};
</script>

<style scoped lang="less">
.item {
  flex: 1;
  p {
    line-height: 30px;
    color: gray;
  }
  p.green {
    color: #42bd56;
  }
}

</style>

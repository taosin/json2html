<template>
  <div :is="item.name" v-bind="item.props" :class="item.classes">
    <template v-for="(child, index) in item.children">
      <componentItem :item="child" :key="index"></componentItem>
    </template>
  </div>
</template>

<script>
export default {
  name: "componentItem",
  props: ["item"],
  components: {},
  data() {
    return {};
  },
  methods: {},
};
</script>

<style scoped>
.class1 {
  width: 100px;
  height: 30px;
  border: 1px solid red;
}
.class2 {
  width: 200px;
  height: 30px;
  border: 1px solid orphans;
}
</style>

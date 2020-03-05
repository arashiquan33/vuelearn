<template>
  <div>
    <p>{{value}}</p>
    <input type="text" :value="value" v-on:input="write">
  </div>
</template>

<script>
export default {
  props: {
    value: {
      type: String,
      default: "默认数据"
    }
  },
  methods: {
    write($event) {
      this.$emit("input", $event.target.value);
    }
  }
};
</script>


<template>
  <div class="text-danger">
    <h1>Trying 2 h1 In page</h1>
    <p>First Message Is : {{ msg }}</p>
    <p>Second Message Is : {{ message }}</p>
  </div>
</template>

<script>
export default {
  name: "firstComponent",
  data() {
    return {
      msg: "hhh",
    };
  },
  props: {
    message: String,
  },
};
</script>
<style scoped lang="scss">
// lang will choose sass language
// scoped limit style just for Element in component
$green: green;
h1 {
  color: $green;
}
</style>

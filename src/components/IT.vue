<template>
  <div class="text-danger">
    <div>
      <h1>IT Department</h1>
      <div v-for="(item, index) in IT" :key="index">
        <p v-if="item.dep == 'IT'">
          {{ item.name }}
          <button @click="deleteIT(item.name)">Delete</button>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "IT",
  props: ["IT"],
  methods: {
    deleteIT(name) {
      this.$emit("delete", { name });
    },
  },
};
</script>
<style scoped lang="scss">
$green: green;
h2 {
  color: red;
}
h1 {
  color: $green;
}
</style>

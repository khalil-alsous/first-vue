<template>
  <div class="text-danger">
    <div>
      <h1>HR Department</h1>
      <div v-for="(item, index) in HR" :key="index">
        <p v-if="item.dep == 'HR'">
          {{ item.name }}
          <button @click="deleteHR(item.name)">Delete</button>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HR",
  props: ["HR"],
  methods: {
    deleteHR(name) {
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

<template>
  <div>
    <h1> {{name}} </h1>
    <button @click="changeName()">Change Name</button>
  </div>
</template>

<script>
export default {
  name: "lifecycleHooks",
  data() {
    return {
      name: "Khalil Alsous",
    };
  },
  methods: {
    changeName(){
        this.name = 'Mohammed Alsous';
    }
  },
  beforeCreate() {
    alert("before Create");
  },
  created() {
    alert("created");
  },
  beforeUpdate() {
    alert("before Update");
  },
  updated(){
    alert("updated");
  }
};
</script>

<template>
  <div class="about">
    <h1>This is an about page</h1>
    <firstComponent message="Vue JS Course" />
    <hr />
    <HRDep :HR="students" @delete="DeleteStudent" />
    <ITDep :IT="students" @delete="DeleteStudent" />
    <hr>
    <lifecycleHooks />
  </div>
</template>

<script>
// @ is an alias to /src
import firstComponent from "@/components/firstComponent.vue";
import HRDep from "@/components/HR.vue";
import ITDep from "@/components/IT.vue";
import lifecycleHooks from "@/components/lifecycleHooks.vue";

export default {
  name: "About",
  components: {
    firstComponent,
    HRDep,
    ITDep,
    lifecycleHooks,
  },
  data() {
    return {
      students: [
        { name: "khalil", dep: "IT" },
        { name: "Ahmed", dep: "HR" },
        { name: "Hasan", dep: "IT" },
        { name: "Zoher", dep: "HR" },
        { name: "Mohammed", dep: "IT" },
      ],
    };
  },
  methods: {
    DeleteStudent(name) {
      this.students = this.students.filter((item) => item.name != name.name);
    },
  },
};
</script>

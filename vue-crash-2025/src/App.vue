<script>
export default {
  data() {
    return {
      name: "SeangDev",
      status: "pending",
      tasks: ["Task One", "Task Two", "Task Three"],
      link: "https://landing.hexcode.anbschool.org",
    };
  },
  methods: {
    toggleStatus() {
      if (this.status === "active") {
        this.status = "pending";
      } else {
        this.status = "active";
      }
    },
  },
};
</script>

<template>
  <div>
    <!-- Interpolation in Vue.js -->
    <p>Hello Vue.js from {{ name }}</p>

    <!-- Conditional rendering with v-show -->
    <p v-if="status === 'active'">SeangDev is Active</p>
    <p v-else-if="status === 'pending'">SeangDev is Pending</p>
    <p v-else>SeangDev is inactive</p>

    <!-- Looping through an array -->
    <ul>
      <li v-for="task in tasks" :key="task">{{ task }}</li>
    </ul>

    <!-- Binding attributes -->
    <a v-bind:href="link">Vottamean App</a>

    <br />
    <!-- Event handling -->
    <button @click="toggleStatus">Change Status</button>
  </div>
</template>

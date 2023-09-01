<script setup>

const app = new Vue({
  el: '#app',
  data: {
    categories: [
      // Categories data
    ],
    posts: [
      // Post list data
    ],
    selectedPost: null
  },
  methods: {
    // Handle the custom event to display post details
    showPostDetails(post) {
      this.selectedPost = post;
    }
  }
});

// Initialize data
app.categories = [
  // Categories data
];

app.posts = [
  // Post list data
];

</script>

<template>
  <div id="app">
  
  <post-categories :categories="categories"></post-categories>
  
  
  <post-list :posts="posts"></post-list>
  
  
  <post-details :post="selectedPost"></post-details>
</div>

  
</template>

<style scoped>

</style>

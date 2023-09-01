Vue.component('post-list', {
    props: ['posts'],
    template: `
      <div>
        <h2>Post List</h2>
        <ul>
          <li v-for="post in posts" :key="post.id">
            <div @click="showPostDetails(post)">{{ post.title }}</div>
          </li>
        </ul>
      </div>
    `,
    methods: {
      showPostDetails(post) {
        // Emit a custom event to notify the parent component
        this.$emit('show-details', post);
      }
    }
  });
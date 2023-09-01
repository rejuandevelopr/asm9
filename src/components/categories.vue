Vue.component('post-categories', {
    props: ['categories'],
    template: `
      <div>
        <h2>Post Categories</h2>
        <ul>
          <li v-for="category in categories" :key="category.id">{{ category.name }}</li>
        </ul>
      </div>
    `
  });
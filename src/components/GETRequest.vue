<template>
  <div>
    <h2>
      GET Request from Json Placeholder
    </h2>

    <div v-for="post in posts"
                :key="post.id"
                class="posts">

      <div class="post">
        <h4>
          {{post.title}}
        </h4>

        <article>
          {{post.body}}
        </article>
      </div>

    </div>

  </div>
</template>

<script>
export default {
  name: 'GETRequest',
  data() {
    return {
      posts: []
    }
  },
  created() {
    this.$http.get('https://jsonplaceholder.typicode.com/posts')
      .then(function(data){
        this.posts = data.body.slice(0,10);
      })
  }

}
</script>

<style scoped>
  .posts {
    text-align: justify;
    width: 100%;
    margin-top: 20px;
  }
  .post {
    max-width: 800px;
    margin: auto;
    padding: 5px 15px 15px 15px;
    background-color: #eee;
    border-radius: 10px;
  }
</style>
<template>
  <div class="home">
    <h1>Home</h1>
    <div v-if="error">{{ error }}</div>
    <div v-if="posts.length"></div>
    <div v-else>Loading posts...</div>
    <PostList :posts="posts" v-if="showPosts" />
    <button @click="showPosts = !showPosts">toggle posts</button>
    <button @click="posts.pop()">delete a post</button>
  </div>
</template>

<script>
import { ref } from "vue";
import PostList from "../components/PostList.vue";
import getPosts from "../composables/getPosts"
export default {
  name: "HomeView",
  components: { PostList },
  setup() {
    const { posts, error, load } = getPosts()
    load()

    const showPosts = ref(true);

    return { posts, showPosts, error };
  },
};
</script>

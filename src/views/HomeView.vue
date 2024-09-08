<template>
  <div class="home">
    <h1>Home</h1>
    <PostList :posts="posts" v-if="showPosts"/>
    <button @click="showPosts = !showPosts">toggle posts</button>
    <button @click="posts.pop()">delete a post</button>
  </div>
</template>

<script>
import { ref } from "vue";
import PostList from "../components/PostList.vue"
export default {
  name: "HomeView",
  components: { PostList },
  setup() {
    const posts = ref([
      { title: "welcome to the blog", body: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolore accusantium magni ex, adipisci voluptas quisquam consectetur cupiditate quos temporibus aperiam doloremque non perspiciatis eveniet dignissimos sint et alias reprehenderit earum libero asperiores voluptatem doloribus sapiente voluptatum! Dignissimos amet, assumenda nam voluptatem aliquam beatae qui nemo harum, necessitatibus ut in nulla quisquam quia dolor distinctio aspernatur eveniet maiores natus inventore illo debitis eos atque tenetur. Suscipit quas tempora officiis nesciunt doloremque deserunt vero dolor aspernatur itaque commodi alias, provident, necessitatibus, consectetur reprehenderit rerum. Voluptatum provident quod, odit deserunt similique aperiam autem laboriosam quas incidunt nesciunt exercitationem consequatur. Ea distinctio eum laborum possimus eius aspernatur a, eos deleniti necessitatibus dignissimos, tempore labore omnis voluptatum eligendi sint, temporibus consequatur amet consectetur perferendis facere fugiat molestias? Dolores animi enim cumque illo accusantium, sed architecto aperiam corrupti commodi modi, voluptatibus sint temporibus repellat, odio distinctio libero perferendis quis? Incidunt vero reprehenderit, eligendi amet inventore corporis adipisci pariatur doloremque temporibus enim quia fugit eum rem obcaecati laboriosam error consequuntur veritatis neque asperiores nostrum molestias? Aut rem, quia nobis ipsam ullam temporibus? Reiciendis consectetur aliquam quasi aut aspernatur necessitatibus doloribus harum. Corrupti blanditiis quo ut excepturi. Adipisci voluptates porro quibusdam eos nemo corporis natus nobis earum repellendus?", id: 1 },
      { title: "top 5 CSS tips", body: "lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolore accusantium magni ex, adipisci voluptas quisquam consectetur cupiditate quos temporibus aperiam doloremque non perspiciatis eveniet dignissimos sint et alias reprehenderit earum libero asperiores voluptatem doloribus sapiente voluptatum! Dignissimos amet, assumenda nam voluptatem aliquam beatae qui nemo harum, necessitatibus ut in nulla quisquam quia dolor distinctio aspernatur eveniet maiores natus inventore illo debitis eos atque tenetur. Suscipit quas tempora officiis nesciunt doloremque deserunt vero dolor aspernatur itaque commodi alias, provident, necessitatibus, consectetur reprehenderit rerum. Voluptatum provident quod, odit deserunt similique aperiam autem laboriosam quas incidunt nesciunt exercitationem consequatur. Ea distinctio eum laborum possimus eius aspernatur a, eos deleniti necessitatibus dignissimos, tempore labore omnis voluptatum eligendi sint, temporibus consequatur amet consectetur perferendis facere fugiat molestias? Dolores animi enim cumque illo accusantium, sed architecto aperiam corrupti commodi modi, voluptatibus sint temporibus repellat, odio distinctio libero perferendis quis? Incidunt vero reprehenderit, eligendi amet inventore corporis adipisci pariatur doloremque temporibus enim quia fugit eum rem obcaecati laboriosam error consequuntur veritatis neque asperiores nostrum molestias? Aut rem, quia nobis ipsam ullam temporibus? Reiciendis consectetur aliquam quasi aut aspernatur necessitatibus doloribus harum. Corrupti blanditiis quo ut excepturi. Adipisci voluptates porro quibusdam eos nemo corporis natus nobis earum repellendus?", id: 2 }
    ])

    const showPosts = ref(true)

    return { posts, showPosts }
  },
};
</script>

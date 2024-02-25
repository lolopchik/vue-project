<script>
import BlogPost from './BlogPostTemplate.vue';
export default {
  components: {
    BlogPost
  },
  data() {
    return {
      posts: [
        {
          title: 'Как сделать lorum ipsum?',
          text: 'Для lorum ipsum нужно: Lorem ipsum, dolor sit amet consectetur adipisicing elit. Rem, earum consequatur debitis perferendis blanditiis quod deleniti ea officiis laudantium. Iste quae veritatis, nam atque iusto voluptatem asperiores libero fugiat incidunt.',
          author: 'Лорум Ипсум',
          date: '13.03.2024',
          comments: [
            'Круто!!!',
            'Недооценённый материал...',
            'Лучшее, что я читал.'
          ],
          image: 'post1'
        },
        {
          title: 'Как сделать lorum ipsum?',
          text: 'Для lorum ipsum нужно: Lorem ipsum, dolor sit amet consectetur adipisicing elit. Rem, earum consequatur debitis perferendis blanditiis quod deleniti ea officiis laudantium. Iste quae veritatis, nam atque iusto voluptatem asperiores libero fugiat incidunt.',
          author: 'Лорум Ипсум',
          date: '13.03.2024',
          comments: [
            'Круто!!!',
            'Недооценённый материал...',
            'Лучшее, что я читал.'
          ],
          image: 'post1'
        },
        {
          title: 'Как сделать lorum ipsum?',
          text: 'Для lorum ipsum нужно: Lorem ipsum, dolor sit amet consectetur adipisicing elit. Rem, earum consequatur debitis perferendis blanditiis quod deleniti ea officiis laudantium. Iste quae veritatis, nam atque iusto voluptatem asperiores libero fugiat incidunt.',
          author: 'Лорум Ипсум',
          date: '13.03.2024',
          comments: [
            'Круто!!!',
            'Недооценённый материал...',
            'Лучшее, что я читал.'
          ],
          image: 'post1'
        },
      ],
      fontSize: 16
    };
  },
  methods: {
    fontSizeDecrease() {
      this.fontSize--
    },
    fontSizeIncrease() {
      this.fontSize++
    },
    fontSizeSet(fontSize) {
      this.fontSize = fontSize
   }
  }
};
</script>

<template>
  <header class="mb-5">
    <nav class="navbar">
      <div class="container-fluid">
        <h1 class="navbar-brand text-white">Лучший блог на планете</h1>
      </div>
    </nav>
  </header>
  <main class="container">
    <h2>Посты:</h2>
    <div class="row g-2" >
      <!-- Вывод всех постов -->
      
      <div class="col-12" v-for="post in posts">
        <BlogPost :post="post" :fontSize="fontSize" @fontSizeIncrease="fontSizeIncrease" @fontSizeDecrease="fontSizeDecrease" @fontSizeSet="fontSizeSet"></BlogPost>
        <!-- Тут должен быть пост -->
      </div>
    </div>
  </main>
</template>

<style>
body {
  margin: 0;
}

.navbar {
  background-color: #008cd5;
  color: white;
}
</style>
<script setup lang="ts">
import blog1 from 'assets/images/blogs/blog1.png'
import blog2 from 'assets/images/blogs/blog2.png'
import blog3 from 'assets/images/blogs/blog3.png'
import blog4 from 'assets/images/blogs/blog4.png'
import PageTemplate from './PageTemplate.vue'

const cards = [
  {
    img: blog1,
    title: 'Красивая Италя, какая она в реальности?',
    about:
      'Для современного мира базовый вектор развития предполагает независимые способы реализации соответствующих условий активизации.',
    date: '01/04/2024',
  },
  {
    img: blog2,
    title: 'Долой сомнения! Весь мир открыт для вас!',
    about:
      'Для современного мира базовый вектор развития предполагает независимые способы реализации соответствующих условий активизации.',
    date: '01/07/2024',
  },
  {
    img: blog3,
    title: 'Как подготовиться к путешествию в одиночку? ',
    about: 'Для современного мира базовый вектор развития предполагает.',
    date: '01/06/2024',
  },
  {
    img: blog4,
    title: 'Индия ... летим?',
    about: 'Для современного мира базовый.',
    date: '01/05/2024',
  },
]
</script>

<template>
  <PageTemplate gray>
    <a-flex vertical align="center" class="blog__container">
      <BlockTitle
        title="Блог о путешествиях"
        pre-title="делимся впечатлениями"
      />
      <a-flex wrap="wrap" gap="20">
        <a-flex
          class="blog__card"
          gap="20"
          v-for="(c, i) in cards"
          :key="i"
          onclick="console.log('clicked')"
        >
          <img :src="c.img" :alt="c.title" class="blog__card-img" />
          <a-flex style="width: 294px; padding: 16px 0" vertical gap="24">
            <p class="blog__card-title">{{ c.title }}</p>
            <p>{{ c.about }}</p>
            <a-flex
              align="center"
              justify="space-between"
              style="margin-top: auto"
            >
              <p class="blog__card-date">{{ c.date }}</p>
              <a-typography-link class="blog__card-link"
                >читать статью</a-typography-link
              >
            </a-flex>
          </a-flex>
        </a-flex>
      </a-flex>
      <a-button type="primary" style="margin-top: 50px"
        >Другие материалы</a-button
      >
    </a-flex>
  </PageTemplate>
</template>

<style scoped>
.blog__container {
  max-width: 1180px;
  margin: 0 auto;
}
.blog__card {
  padding: 16px;
  border-radius: 10px;
  background-color: rgba(253, 253, 253, 1);
  font-size: 14px;
  line-height: 20px;
  color: rgba(24, 18, 30, 1);
}
.blog__card:hover {
  cursor: pointer;
}
.blog__card-img {
  height: 280px;
  object-fit: contain;
}
.blog__card-title {
  font-size: 24px;
  font-weight: 700;
  line-height: 32px;
  transition: all 1s ease;
  text-decoration-color: transparent;
}
.blog__card-title:hover {
  color: rgba(26, 62, 62, 1);
  text-decoration: underline rgba(26, 62, 62, 1);
}
.blog__card-date {
  font-weight: 700;
  color: rgba(242, 190, 34, 1);
}
.blog__card-link {
  font-weight: 700;
  color: rgba(26, 62, 62, 1);
}
</style>

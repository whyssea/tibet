<script setup lang="ts">
import vid1 from 'assets/images/vid/vid1.png'
import vid2 from 'assets/images/vid/vid2.png'
</script>

<template>
  <PageTemplate>
    <a-flex gap="120" style="width: 1180px; margin: 0 auto">
      <div>
        <img :src="vid2" alt="Видео 2" />
        <img :src="vid1" alt="Видео 1" class="about__video" />
      </div>
      <div>
        <BlockTitle
          title="Исследуйте все горные массивы мира вместе с нами"
          pre-title="о нашем походе"
        />
        <p class="about__par">
          Его корни уходят в один фрагмент классической латыни 45 года н.э., то
          есть более двух тысячелетий назад. Ричард МакКлинток, профессор латыни
          из колледжа Hampden-Sydney, штат Вирджиния, взял одно из самых
          странных слов в Lorem Ipsum, "consectetur"и занялся его поисками в
          классической латинской литературе.
        </p>
        <a-button type="primary">Программа тура</a-button>
      </div>
    </a-flex>
  </PageTemplate>
</template>

<style scoped>
.about__par {
  font-size: 18px;
  line-height: 27px;
  margin-bottom: 40px;
}
.about__video {
  width: 350px;
  height: 400px;
  border-radius: 24px;
}
.about__video:last-of-type {
  margin-top: -225px;
  margin-left: 130px;
}
</style>

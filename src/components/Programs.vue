<script setup lang="ts">
import prog1 from 'assets/images/progs/prog1.png'
import prog2 from 'assets/images/progs/prog2.png'
import prog3 from 'assets/images/progs/prog3.png'
import prog4 from 'assets/images/progs/prog4.png'
import experience from 'assets/images/experience.svg'
import prices from 'assets/images/prices.svg'
import secure from 'assets/images/secure.svg'
import PageTemplate from './PageTemplate.vue'

const programs = [prog1, prog2, prog3, prog4]
const pars = [
  {
    title: 'Опытный гид',
    text: 'Для современного мира базовый вектор развития предполагает независимые способы реализации соответствующих условий активизации.',
    img: experience,
  },
  {
    title: 'Безопасный поход',
    text: 'Для современного мира базовый вектор развития предполагает независимые способы реализации соответствующих условий активизации.',
    img: secure,
  },
  {
    title: 'Лояльные цены',
    text: 'Для современного мира базовый вектор развития предполагает независимые способы реализации соответствующих условий активизации.',
    img: prices,
  },
]
</script>

<template>
  <PageTemplate gray>
    <a-flex class="programs__container" align="center" gap="90">
      <div>
        <BlockTitle
          pre-title="наше предложение"
          title="Лучшие программы для тебя"
        />
        <p class="programs__text">
          Его корни уходят в один фрагмент классической латыни 45 года н.э., то
          есть более двух тысячелетий назад. Ричард МакКлинток, профессор латыни
          из колледжа.
        </p>
        <a-flex gap="40" vertical class="programs__props">
          <a-flex v-for="(p, i) in pars" :key="i" gap="16" align="center">
            <img class="programs__prop-img" :src="p.img" :alt="p.title" />
            <div class="programs__prop-container">
              <p class="programs__prop-title">{{ p.title }}</p>
              <p class="programs__prop-text">{{ p.text }}</p>
            </div>
          </a-flex>
        </a-flex>
        <a-button type="primary">Стоимость программ</a-button>
      </div>
      <a-flex gap="10" wrap="wrap" style="height: min-content; width: 100%">
        <img
          class="programs__image"
          :class="{ programs__image_reverse: i === 1 || i === 2 }"
          v-for="(p, i) in programs"
          :key="i"
          :src="p"
          alt="Программа {{i}}"
        />
      </a-flex>
    </a-flex>
  </PageTemplate>
</template>

<style scoped>
.programs__container {
  width: 1180px;
  margin: 0 auto;
}
.programs__text {
  font-size: 18px;
  line-height: 27px;
  margin-bottom: 40px;
}
.programs__props {
  margin-bottom: 40px;
}
.programs__prop-img {
  width: 50px;
  height: 50px;
}
.programs__prop-container {
  font-size: 18px;
  line-height: 20px;
}
.programs__prop-title {
  font-weight: 700;
  letter-spacing: 0.012em;
  margin-bottom: 4px;
}
.programs__prop-text {
  font-size: 14px;
}
.programs__image {
  width: 250px;
  height: 250px;
  border-radius: 0 50px 0 50px;
}
.programs__image_reverse {
  border-radius: 50px 0 50px 0;
}
</style>

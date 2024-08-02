<script setup lang="ts">
import telega from 'assets/images/telegram.svg'
import vk from 'assets/images/vk.svg'
import pin from 'assets/images/pinterest.svg'
import skype from 'assets/images/skype.svg'
const services = [
  'Прогулки в горы летом',
  'Зимние походы в горы',
  'Посещение храмов в горах',
  'Экстремальные виды туризма',
  'Походы в джунглях Амазонии',
  'Поездка в Африку',
]
const notes = [
  'Как собрать в долгий поход?',
  'Жизненно важные предметы для похода',
  'Медицинская страховка, гарантии безопасности',
  'Если вы врач - загляните сюда',
]
const icons = [telega, vk, pin, skype]
</script>

<template>
  <PageTemplate
    style="background-color: rgba(26, 62, 62, 1); padding: 180px 0 80px 0"
  >
    <a-flex class="footer__container" justify="space-between">
      <a-flex class="footer__contacts" vertical :gap="16">
        <p class="footer__title">Компания «РумТибет»</p>
        <p>
          Его корни уходят в один фрагмент классической латыни 45 года н.э., то
          есть более двух тысячелетий назад. Ричард МакКлинток, профессор латыни
          из колледжа Hampden-Sydney.
        </p>
        <div style="margin-top: auto">
          <a-typography-link
            style="margin-right: 24px; text-decoration: underline"
            >info@domain.com</a-typography-link
          >
          <a-typography-link style="text-decoration: underline"
            >+7 (123) 456-78-90</a-typography-link
          >
          <a-flex style="margin-top: 32px" :gap="16">
            <a-typography-link v-for="(e, i) in icons" :key="i"
              ><img :src="e" alt="Иконка"
            /></a-typography-link>
          </a-flex>
        </div>
      </a-flex>
      <a-flex vertical :gap="16">
        <p class="footer__title">Наши услуги</p>
        <a-typography-link v-for="(s, i) in services" :key="i"
          >> {{ s }}</a-typography-link
        >
      </a-flex>
      <a-flex style="max-width: 280px" vertical :gap="16">
        <p class="footer__title">Важно для путешествий</p>
        <a-typography-link v-for="(n, i) in notes" :key="i"
          >> {{ n }}</a-typography-link
        >
      </a-flex>
    </a-flex>
  </PageTemplate>
</template>

<style scoped>
.footer__container {
  width: 100%;
  max-width: 1180px;
  color: rgba(243, 245, 244, 1);
  font-size: 14px;
  line-height: 20px;
  margin: 0 auto;
}
.footer__title {
  font-size: 20px;
  font-weight: 700;
  line-height: 24px;
  margin-bottom: 4px;
}
.footer__contacts {
  max-width: 460px;
}
</style>

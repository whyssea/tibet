<script setup lang="ts">
import card1 from 'assets/images/cards/card1.png'
import card2 from 'assets/images/cards/card2.png'
import card3 from 'assets/images/cards/card3.png'
import star from 'assets/images/ic_round-star.svg'

const cards = [
  {
    img: card1,
    title: 'Озеро возле гор',
    about: 'романтическое приключение',
    price: 480,
    rate: 4.9,
  },
  {
    img: card2,
    title: 'Ночь в горах',
    about: 'в компании друзей',
    price: 500,
    rate: 4.5,
  },
  {
    img: card3,
    title: 'Йога в горах',
    about: 'для тех, кто забоится о себе',
    price: 230,
    rate: 5.0,
  },
]
</script>

<template>
  <PageTemplate>
    <a-flex vertical align="center" justify="center" class="routes__container">
      <BlockTitle
        title="Популярные направления"
        pre-title="по версии отдыхающих"
      />
      <a-flex wrap="wrap" justify="center" gap="20">
        <a-flex
          v-for="(c, i) in cards"
          :key="i"
          class="routes__card"
          :style="{ backgroundImage: 'url(' + c.img + ')' }"
        >
          <a-flex align="center" gap="4" class="routes__card-rate">
            <img alt="Звезда" :src="star" />
            <p>{{ c.rate.toFixed(1) }}</p>
          </a-flex>
          <div
            class="routes__card_blur"
            :style="{ backgroundImage: 'url(' + c.img + ')' }"
          />
          <a-flex
            justify="space-between"
            align="center"
            class="routes__card-content"
          >
            <div>
              <p class="routes__card-title">{{ c.title }}</p>
              <p class="routes__card-text">{{ c.about }}</p>
            </div>
            <div class="routes__card-price-container">
              <p>{{ c.price }} $</p>
            </div>
          </a-flex>
        </a-flex>
      </a-flex>
      <a-button style="margin-top: 50px" type="primary"
        >Рейтинг направлений</a-button
      >
    </a-flex>
  </PageTemplate>
</template>

<style scoped>
.routes__container {
  max-width: 1180px;
  margin: 0 auto;
}
.routes__card {
  position: relative;
  width: 380px;
  height: 500px;
  border-radius: 32px;
  overflow: hidden;
}
.routes__card-rate {
  position: absolute;
  top: 50px;
  right: 0;
  background-color: rgba(253, 253, 253, 0.4);
  padding: 4px 8px;
  border-radius: 4px 0 0 4px;
}
.routes__card_blur {
  position: absolute;
  bottom: 0;
  height: 90px;
  width: 100%;
  background-position: 0 90px;
  border-radius: 0 0 32px 32px;
  filter: blur(8px);
}
.routes__card-content {
  position: relative;
  margin-top: auto;
  background: rgba(255, 255, 255, 0.2);
  border-radius: 0 0 32px 32px;
  padding: 20px 32px;
  width: 100%;
  color: white;
}
.routes__card-title {
  font-size: 24px;
  font-weight: 700;
  line-height: 29px;
}
.routes__card-text {
  font-size: 14px;
  line-height: 18px;
}
.routes__card-price-container {
  background-color: rgba(255, 255, 255, 0.3);
  font-size: 20px;
  line-height: 24px;
  border-radius: 4px;
  padding: 8px 16px;
}
</style>

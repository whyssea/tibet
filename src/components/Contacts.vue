<script setup lang="ts"></script>

<template>
  <PageTemplate
    style="
      padding: 0;
      margin-bottom: -100px;
      z-index: 1;
      background-color: transparent;
    "
  >
    <a-flex class="contacts__container" :gap="64">
      <a-flex vertical>
        <p class="contacts__pre">актуально</p>
        <a-typography-title :level="3" class="contacts__title">
          Получайте полезные рассылки о путешествиях
        </a-typography-title>
      </a-flex>
      <a-flex vertical :gap="8">
        <p class="contacts__form-label">Введите e-mail адрес</p>
        <a-form style="width: 100%; align-items: center" layout="inline">
          <a-form-item>
            <a-input
              type="email"
              placeholder="name@domain.com"
              style="
                background-color: rgba(243, 245, 244, 1);
                color: rgba(24, 18, 30, 1);
              "
            />
          </a-form-item>
          <a-form-item>
            <a-button type="primary" html-type="submit"
              >Подписаться на новости</a-button
            >
          </a-form-item>
        </a-form>
        <p class="contacts__form-caption">
          подписываясь на новости, вы автоматически соглашаетесь с условиями
          обработки персональных данных и правилами рекламных рассылок
        </p>
      </a-flex>
    </a-flex>
  </PageTemplate>
</template>

<style scoped>
.contacts__container {
  max-width: 1180px;
  margin: 0 auto;
  padding: 40px 100px;
  box-shadow: 0 0 15px 0 rgba(24, 18, 30, 0.12);
  color: rgba(24, 18, 30, 1);
  border-radius: 6px;
  background-color: white;
}
.contacts__pre {
  color: rgba(242, 190, 34, 1);
  font-size: 18px;
  line-height: 20px;
  margin-bottom: 8px;
}
.contacts__title {
  font-weight: 800;
}
.contacts__form-label {
  font-size: 16px;
  font-weight: 600;
  line-height: 20px;
}
.contacts__form-caption {
  font-size: 14px;
  font-weight: 600;
  line-height: 18px;
}
</style>

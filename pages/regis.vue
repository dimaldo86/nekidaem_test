<template>
  <section class="regis">
    <div class="regis__header">
        <h1>Регистрация</h1>
        <nuxt-link to="/" class="link">На главную</nuxt-link>
    </div>
    <form action="#" class="regis__form form">
        <ui-input
            name="email"
            placeholder="email"

        />
        <ui-input
            type="password"

        />
        <ui-input/>
    </form>
  </section>
</template>

<script setup>
definePageMeta({
  layout: "empty",
});
</script>

<style scoped>
.regis {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 200px auto;
  max-width: max-content;
  background: var(--gray);
  padding: 20px;
}
.regis__header {
    display: flex;
    align-items: center;
    column-gap: 40px;
}
.form {
    margin-top: 40px;
    display: flex;
    flex-direction: column;
    row-gap: 20px;
}
</style>

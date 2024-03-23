<template>
  <header class="header">
    <div class="container">
      <nav class="header__nav nav">
        <nuxt-link to="/" class="nav__logo"> Logo</nuxt-link>
        <menu class="nav__menu">
			<nuxt-link to="/" class="link">Главная</nuxt-link>
			<nuxt-link to="/about" class="link">О нас</nuxt-link>
        </menu>
        <nuxt-link to="/regis" class="nav__btn">Регистрация</nuxt-link>
      </nav>
    </div>
  </header>
</template>

<script setup></script>

<style scoped>
.header {
  position: sticky;
  top: 0;
  left: 0;
  width: 100%;
  transition: var(--transition);
  z-index: 1000;
  background-color: var(--secondary);
}
.header__nav {
  height: 60px;
  display: flex;
  align-items: center;
  column-gap: 40px;
}
.nav__logo {
  color: var(--green);
  font-weight: 700;
  font-size: 24px;
  transition: var(--transition);
}
.nav__logo:hover {
  text-shadow: 5px 5px 5px var(--gray);
}
.nav__menu {
  display: flex;
  align-items: center;
  column-gap: 20px;
  height: 100%;
  margin-left: auto;
}
.nav__link {
  color: var(--primary);
  padding: 10px 10px;
  font-weight: 500;
  position: relative;
  transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}
.nav__link::before {
  content: "";
  position: absolute;
  bottom: 0;
  right: 0;
  width: 0;
  height: 2px;
  background-color: var(--primary);
  transition: width 0.6s cubic-bezier(0.25, 1, 0.5, 1);
}
.nav__link::before:hover {
  left: 0;
  right: auto;
  width: 100%;
}

@media (hover: hover) and (pointer: fine) {
  .nav__link:hover::before {
    left: 0;
    right: auto;
    width: 100%;
  }
}
.router-link-active {
  color: var(--green);
}
.nav__btn {
	padding: 10px 20px;
	background-color: var(--greenDark);
	border: none;
	border-radius: 8px;
	color: var(--primary);
	transition: var(--transition);
}
.nav__btn:hover {
	transform: translateY(-2px);
	box-shadow: 5px 2px 5px var(--gray);
}
</style>

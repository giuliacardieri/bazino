<template>
  <header class="header">
    <h1 class="header__h1">
      <NuxtLink class="header__link" to="/">Matheus Baz</NuxtLink>
    </h1>
    <nav class="header__nav">
      <ul class="header__ul">
        <li class="header__li">
          <NuxtLink
            class="header__navlink"
            exactActiveClass="header__navlink--active"
            to="/sobre"
            >Sobre</NuxtLink
          >
        </li>
        <li class="header__li">
          <NuxtLink
            class="header__navlink"
            exactActiveClass="header__navlink--active"
            to="/trabalho"
            >Trabalho</NuxtLink
          >
        </li>
        <li class="header__li">
          <NuxtLink
            class="header__navlink"
            exactActiveClass="header__navlink--active"
            to="/contato"
            >Contato</NuxtLink
          >
        </li>
      </ul>
    </nav>
  </header>
</template>
<style scoped>
.header {
  background-color: var(--white);
  box-sizing: border-box;
  padding: 16px var(--size-padding);
  position: sticky;
  top: 0;
  width: 100%;
  z-index: 2;
}

@media (min-width: 1024px) {
  .header {
    align-items: center;
    display: flex;
    justify-content: space-between;
  }
}

.header__h1 {
  color: var(--black);
  font-size: 24px;
  font-weight: normal;
}

.header__ul {
  display: flex;
  gap: 48px;
  padding: 0;
}

.header__li {
  list-style: none;
}

.header__link,
.header__navlink {
  color: var(--black);
  text-decoration: none;
  text-transform: uppercase;
}

.header__navlink--active {
  opacity: 0.5;
}
</style>

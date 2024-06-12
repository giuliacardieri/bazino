<template>
  <CHeader />
  <main class="main"><slot /></main>
  <CFooter />
</template>

<style>
.main {
  box-sizing: border-box;
  padding: 16px var(--size-padding);
}

.main__h2 {
  color: var(--black);
  font-size: 18px;
  font-weight: normal;
  margin: 0 0 16px 0;
  text-transform: uppercase;
}

.main__p {
  margin: 0;
}

.main__p + .main__p {
  margin-top: 18px;
}
</style>

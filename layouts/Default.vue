<template>
  <div class="layout">
    <CHeader />
    <main class="main"><slot /></main>
    <CFooter />
  </div>
</template>

<style>
.layout {
  display: grid;
  grid-template-rows: 128px auto 80px;
}

.main {
  box-sizing: border-box;
  padding: 16px var(--size-padding);
  position: relative;
}

.main__h2 {
  color: var(--black);
  font-size: 18px;
  font-weight: 400;
  margin: 0 0 16px 0;
  text-transform: uppercase;
}

.main__p {
  margin: 0;
}

.main__p + .main__p {
  margin-top: 18px;
}

@media (max-width: 1024px) {
  :root {
    --size-padding: 16px;
  }
}
</style>

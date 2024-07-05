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
  grid-template-rows: 128px minmax(calc(100vh - 176px), auto) 48px;
}
@media (max-width: 1023px) {
  .layout {
    grid-template-rows: 128px minmax(calc(100vh - 208px), auto) 80px;
  }
}

.main {
  box-sizing: border-box;
  padding: 16px var(--size-padding);
  position: relative;
}

.main__h2 {
  color: var(--black);
  font-size: 18px;
  font-weight: 300;
  margin: 0 0 16px 0;
  text-transform: uppercase;
}

.main__h2--bold {
  font-weight: 400;
}

.main__p {
  margin: 0;
}

.main__p--small {
  font-size: 14px;
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

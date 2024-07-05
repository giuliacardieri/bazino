<template>
  <div class="images">
    <ImageButton
      id="cecilia"
      link="/familia"
      src="cecilia.png"
      alt="Retrato de uma mulher com expressão séria com colagens cor magenta em seu rosto"
    />
    <ImageButton
      id="rafaela"
      link="/bonecas"
      src="rafaela.png"
      alt="Retrato de uma mulher sorridente de corpo inteiro com um vestido azul"
    />
  </div>
</template>

<style scoped>
.images {
  position: relative;
}

@media (max-width: 1023px) {
  .images {
    display: grid;
    gap: 16px;
  }
}
</style>

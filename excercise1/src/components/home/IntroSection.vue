<template>
  <section class="intro">
    <div class="intro__overlay">
      <div class="intro__title">Hello Developer!</div>
      <div class="intro__description mt-2">Lorem ipsum dolor sit amet, consectetur adipiscing elit</div>
    </div> 
  </section>
</template>

<style scoped lang="scss">
.intro {
  height: 600px;
  background: #888;
  background-image: url(@/assets/600x600.svg);
  background-repeat: no-repeat;
  background-size: cover; 
  background-position: center;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;

  &__overlay {
    text-align: center;
  }

  &__title {
    font-size: 72px;
    font-weight: bold;
    padding: 0 24px;
  }

  &__description {
    font-size: 42px;
    padding: 0 24px;
  }
}

@media (min-width: 768px) {
  .intro {
    height: 650px;
    background-image: url(@/assets/1920x650.svg);
  }

  .intro__title {
    font-size: 96px;
  }
}
</style>
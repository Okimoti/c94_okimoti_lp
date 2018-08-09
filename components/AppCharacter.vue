<template>
  <div class="character">
    <img src="~/assets/hito.png">
  </div>
</template>

<style scoped>
.character {
  display: flex;
  justify-content: flex-end;
  align-items: flex-end;
  width: 100vw; height: 100vh;
  position: relative;
}

img {
  display: block;
  width: 500px; height: auto;
  opacity: 0;
  animation: fadeIn 2s ease 6.8s forwards;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
    transform: translateY(700px);
  }
  100% {
    opacity: 1;
  }
}
</style>

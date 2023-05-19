<template>
  <div class="ticket" :style="`background-image: url(${imgUrl})`">
  </div>
</template>

<script>
const IMG_URL = 'https://image.tmdb.org/t/p/w200'

export default {
  name: 'MovieCard',
  props:{
    movie : Object,
  },
  computed: {
    imgUrl(){
      return `${IMG_URL}` + this.movie.poster_path
    }
  },
}

window.addEventListener("DOMContentLoaded", () => {
  const ticket = document.querySelector(".ticket");
  const ticketWidth = ticket.offsetWidth;
  const ticketHeight = ticket.offsetHeight;

  const circle = document.querySelector(".ticket::before");
  const circleSize = circle.offsetWidth;

  const offsetX = ticketWidth / 2 - circleSize / 2;
  const offsetY = ticketHeight / 2 - circleSize / 2;

  circle.style.transform = `translate(${offsetX}px, ${offsetY}px)`;
});

</script>

<style scoped>
.ticket {
  width: 170px;
  height: 300px;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  position: relative;
  overflow: hidden;
}

.ticket::before {
  content: "";
  position: absolute;
  width: 30px;
  height: 30px;
  background-color: #fff;
  border-radius: 50%;
}

.ticket::after {
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: -1;
  border: 2px solid #000;
  border-radius: 25px;
  box-sizing: border-box;
}
</style>
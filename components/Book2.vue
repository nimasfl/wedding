<template>
  <div :class="cardClass">
    <div class="imgBox">
      <div class="bark">
        <p>hello beautiful</p>
      </div>
      <img src="/paper.jpg" style="width: 400px; height: 500px; max-height: max-content; max-width: 500px" alt="."/>
    </div>
    <div class="details">
    </div>
  </div>
</template>

<script>
export default {
  name: 'Book2',
  data: () => ({
    cardClass: 'card'
  }),
  mounted() {
    setTimeout(() => {
      this.cardClass += ' card-hover'
    },0)
  }
}
</script>

<style scoped>
::selection {
  background: transparent;
}

h4 {
  font-size: 26px;
  line-height: 1px;
  font-family: 'Amatic SC', cursive !important;
}

.color1{color:#1BBC9B}/*MOUNTAIN MEADOW*/
.color2{color:#C0392B/*TALL POPPY*/}

.card {
  color: #013243; /*SHERPA BLUE*/
  position: absolute;
  top: 50%;
  left: 50%;
  width: 400px;
  height: 500px;
  background: #e0e1dc;
  transform-style: preserve-3d;
  transform: translate(-50%,-20%) perspective(2000px);
  box-shadow: inset 300px 0 50px rgba(0,0,0,.5), 300px 0 50px rgba(0,0,0,.5);
  transition: 3s;
}

.bark {
  position: absolute;
  top: 20%;
  left: 50%;
  width: 400px;
  height: 500px;
  transform-style: preserve-3d;
  transform: translate(-50%,-20%) perspective(4000px);
  box-shadow: inset 300px 0 50px rgba(0,0,0,.5), 60px 0 20px rgba(0,0,0,.5);
  transition: 3s;
}

.bark p {
  transform: rotateY(180deg);
}

.card-hover {
  transform: translate(0%,-50%) perspective(2000px) scale(1.4);
  box-shadow: inset 10px 0 50px rgba(0,0,0,.5), 10px 0 50px rgba(0,0,0,.5);
}

/*.card:before {*/
/*  content:'';*/
/*  position: absolute;*/
/*  top: -5px;*/
/*  left: 0;*/
/*  width: 100%;*/
/*  height: 5px;*/
/*  background: #BAC1BA;*/
/*  transform-origin: bottom;*/
/*  transform: skewX(-45deg);*/
/*}*/


/*.card:after {*/
/*  content: '';*/
/*  position: absolute;*/
/*  top: 0;*/
/*  right: -5px;*/
/*  width: 5px;*/
/*  height: 100%;*/
/*  background: #92A29C;*/
/*  transform-origin: left;*/
/*  transform: skewY(-45deg);*/
/*}*/

.card .imgBox {
  width: 100%;
  height: 100%;
  position: relative;
  transform-origin: left;
  transition: .7s;
}

.card .bark {
  position: absolute;
  background: #e0e1dc;
  width: 100%;
  height: 100%;
  opacity: 0;
  transition: 3s;
}

.card .imgBox img {
  min-width: 250px;
  max-height: 400px;
}

.card-hover .imgBox {
  transform: rotateY(-180deg);
  transition: 3s;
}

.card-hover .bark {
  opacity: 1;
  transition: 3s;
  box-shadow: inset 10px 0 50px rgba(0,0,0,.5);
}

.details {
  background-image: url("/frontpage.jpeg");
  background-size: cover;
  height: 500px;
  width: 400px;
  position: absolute;
  top: -70px;
  left: 0;
  box-sizing: border-box;
  padding: 0 0 0 10px;
  z-index: -1;
  margin-top: 70px;
}

.card .details p {
  font-size: 15px;
  line-height: 5px;
}

.card .details h4 {
  text-align: center;
}

.text-right {
  text-align: right;
}
</style>

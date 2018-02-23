<template>
  <div class="container">
      <div class="triangle">
        <img src="../assets/triangle1.png"/>
        <h1><span class="harry-potter">M</span> <span class="and">&</span> <span class="star-wars">W</span></h1>
      </div>
      <div class="top"></div>
      <div class="bottom"></div>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped lang="scss">
    @import "../style/variables.scss";

    @font-face {
      font-family: HarryPotter;
      src: url('../assets/harryp.ttf')  format('truetype'), /* Safari, Android, iOS */
    }

    @font-face {
      font-family: StarWars;
      src: url('../assets/starjedi.ttf')  format('truetype'), /* Safari, Android, iOS */
    }

    .container {
        height: 4.4375rem;
        background-color: $secondary;

        .triangle {
          z-index: 100;
          position: absolute;
          left: 50%;
          margin-left: -123.5px;

          .harry-potter {
            font-family: 'HarryPotter', Fallback, sans-serif;
          }

          .and {
            font-size: 1.2rem;
            font-family: Optima;
          }

          .star-wars {
            font-family: 'StarWars', Fallback, sans-serif;
          }

          h1 {
            position: absolute;
            top: 2px;
            left: 68px;
            font-size: 2.5rem;
            line-height: 2.5rem;
            color: $secondary;
            letter-spacing: -2px;
          }
        }

        .top {
            background-color: $primary;
            height: 2.5rem;
        }

        .bottom {
            background-color: $secondary-darker;
            height: 1rem;

            background-image: url('../assets/fleur-de-lis-border.png');
            background-repeat: repeat-x;

            -webkit-transition: -webkit-transform .15s linear;
            -webkit-box-shadow: 0 1px 4px rgba(0,0,0,.25);
            -moz-box-shadow: 0 1px 4px rgba(0,0,0,.25);
            transition: -webkit-transform .15s linear;
            box-shadow: 0 1px 4px rgba(0,0,0,.25);
        }
    }
</style>

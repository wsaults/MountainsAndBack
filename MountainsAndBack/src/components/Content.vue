<template>
  <div class="container">
    <div class="intro-content">
      <h1>A Really Nice Header</h1>
      <h2>Our Journey</h2>
      <div class="content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
      </div>
      <div class="divider"></div>
    </div>
    <div class="timeline">
      <div class="line"></div>
      <div class="established">
        <h1><span>ESTABLISHED</span></h1>
        <h2>2016</h2>
      </div>
      <ul class="polaroids">
        <li>
          <a href="" title="September 9th, 2016"><img src="../assets/2016-09-04.jpg" alt="Test" title="Test"/></a>
          <p>Ridng the cable car in Aspen! Seriously, it's really cool!</p>
        </li>
        <li>
          <a href="" title="September 9th, 2016"><img src="../assets/2016-09-04-1.jpg" alt="Test" title="Test"/></a>
          <p>Made it to the top of the mountain!</p>
        </li>
        <li>
          <a href="" title="January 1st, 2000"><img src="../assets/me.jpeg" alt="Test" title="Test"/></a>
          <p>Some really awesome stuff that I want to talk about. Seriously, it's really cool.</p>
        </li>
        <li>
          <a href="" title="January 1st, 2000"><img src="../assets/me.jpeg" alt="Test" title="Test"/></a>
          <p>Some really awesome stuff that I want to talk about. Seriously, it's really cool.</p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Content',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "../style/variables.scss";

  h1, h2 {
    font-weight: normal;
  }

  .container {
    background-image: url('../assets/diamond_grid.png');
    background-repeat: repeat;
    z-index: -5;
  }

  .intro-content {
    background-color: $secondary;
    background-image: url('../assets/bg-pattern.png');
    background-repeat: repeat;

    h1 {
      padding-top: 1rem;
      font-size: 3rem;
      line-height: 3rem;
      font-family: Futura;
    }

    h2 {
      color: $primary-lighter;
      font-size: 1.8rem;
      padding-top: 1rem;
    }

    p:first-child:first-letter {
      color: $primary-lighter;
      float: left;
      font-family: Georgia;
      font-size: 75px;
      line-height: 60px;
      padding-top: 4px;
      padding-right: 8px;
      padding-left: 3px;
    }
  }

  .content {
    // display: flex;

    p {
      margin: 2rem 1.5rem;
      color: primary-darker;
    }
  }

  .divider {
    background-color: $secondary-darker;
    height: 1rem;

    background-image: url('../assets/texas-star-border.png');
    background-repeat: repeat-x;
  }

  .timeline {
    margin-top: 1rem;
    margin-bottom: 20rem;
    display: flex;
    flex-flow: column;

    .line {
      position: absolute;
      left: 49%;
      top: 0;
      bottom: 0;
      width: 10px;
      background: $primary;
      z-index: -2;
    }

    ul.polaroids {
      padding: 0;
      margin-top: 6rem;
    }

    ul.polaroids a:after {
      content: attr(title);
    }

    ul.polaroids li {
      background-color: white;
      margin: 1.5rem auto;
      margin-bottom: 5rem;
      padding: 1.5rem;
      max-width: 320px;

      a {
        text-decoration: none;
        color: $primary;
        font-size: 1.8rem;
      }

      p {
        padding-top: .5rem;
        line-height: 1.2rem;
      }
    }

    ul.polaroids img {
      margin-bottom: 1rem;
    }

    /* By default, we tilt all our images -2 degrees */
    ul.polaroids li {
      -webkit-transform: rotate(-2deg);
      -moz-transform: rotate(-2deg);
      transform: rotate(-2deg);
    }

    /* Rotate all even images 2 degrees */
    ul.polaroids li:nth-child(even) {
      -webkit-transform: rotate(2deg);
      -moz-transform: rotate(2deg);
      transform: rotate(2deg);
    }

    /* Don't rotate every third image, but offset its position */
    ul.polaroids li:nth-child(3n) {
      -webkit-transform: none;
      -moz-transform: none;
      transform: none;
      position: relative;
    }

    /* Rotate every fifth image by 5 degrees and offset it */
    ul.polaroids li:nth-child(5n) {
      -webkit-transform: rotate(5deg);
      -moz-transform: rotate(5deg);
      transform: rotate(5deg);
      position: relative;
    }

    /* Add drop shadows and smooth out the transition (Safari only) */
    ul.polaroids li {
      -webkit-transition: -webkit-transform .15s linear;
      -webkit-box-shadow: 0 3px 6px rgba(0,0,0,.25);
      -moz-box-shadow: 0 3px 6px rgba(0,0,0,.25);
      transition: -webkit-transform .15s linear;
      box-shadow: 0 3px 6px rgba(0,0,0,.25);
    }

    .established {
      align-self: center;
      background-color: $secondary;
      margin-top: -1rem;
      padding-top: 2rem;
      padding-bottom: 1rem;
      z-index: 0;

      h1 {
        border-bottom: 1px solid $secondary-darker;
        line-height: 0.1em;
        font-size: 1rem;
        margin: .7rem auto;
        font-family: Futura;

        span {
          background: $secondary;
          padding:0 5px;
        }
      }

      h2 {
        color: $primary-lighter;
        font-size: 5.5rem;
        font-weight: bold;
        line-height: 5.5rem;
        height: 6rem;
        font-family: Futura;
      }
    }
  }
</style>

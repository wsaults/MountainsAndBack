<template>
  <div class="container">
    <div class="intro-content">
      <h1>A Really Nice Header</h1>
      <h2>A Really Nice Subtitle</h2>
      <div class="divider"></div>
    </div>
    <div class="timeline">
      <div class="established">
        <h1><span>ESTABLISHED</span></h1>
        <h2>2000</h2>
      </div>
      <ul class="polaroids">
        <li>
          <a href="" title="January 1st 2000"><img src="../assets/me.jpeg" alt="Test" title="Test"/></a>
        </li>
        <li>
          <a href="" title="January 1st 2000"><img src="../assets/me.jpeg" alt="Test" title="Test"/></a>
        </li>
        <li>
          <a href="" title="January 1st 2000"><img src="../assets/me.jpeg" alt="Test" title="Test"/></a>
        </li>
        <li>
          <a href="" title="January 1st 2000"><img src="../assets/me.jpeg" alt="Test" title="Test"/></a>
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

  .divider {
    background-color: $secondary-darker;
    height: 0.5rem;
  }

  .timeline {
    margin-top: 1rem;
    display: flex;
    flex-flow: column;

    ul.polaroids {
      padding: 0;
    }

    ul.polaroids a:after {
      content: attr(title);
    }

    ul.polaroids li {
      background-color: white;
      margin: 1.5rem auto;
      padding: 1.5rem;
      max-width: 420px;

      a {
        text-decoration: none;
        color: $primary;
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
      top: -5px;
    }

    /* Rotate every fifth image by 5 degrees and offset it */
    ul.polaroids li:nth-child(5n) {
      -webkit-transform: rotate(5deg);
      -moz-transform: rotate(5deg);
      transform: rotate(5deg);
      position: relative;
      right: 5px;
    }

    /* Add drop shadows and smooth out the transition (Safari only) */
    ul.polaroids li {
      -webkit-transition: -webkit-transform .15s linear;
      -webkit-box-shadow: 0 3px 6px rgba(0,0,0,.25);
      -moz-box-shadow: 0 3px 6px rgba(0,0,0,.25);
      transition: -webkit-transform .15s linear;
      box-shadow: 0 3px 6px rgba(0,0,0,.25);
    }
  }

  .established {
    align-self: center;
    h1 {
      border-bottom: 1px solid $secondary-darker;
      line-height: 0.1em;
      font-size: 1rem;
      margin: .7rem auto;

      span {
        background: $secondary;
        padding:0 5px;
      }
    }

    h2 {
      color: $primary;
      font-size: 5.5rem;
      font-weight: bold;
      line-height: 5.5rem;
      height: 6rem;
    }
  }
</style>

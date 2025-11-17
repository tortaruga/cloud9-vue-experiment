<script>
import ScrollAnimation from '../ScrollAnimation.vue';

export default {
  components: {ScrollAnimation}
}
</script>

<template>
    <section id="philosophy">
        <div>

        <h1>Our philosophy</h1>
        <div class="box">
          <ScrollAnimation> 
        <p>our motto Dove ti porta il vento ("wherever the wind may take you") explains it best: cloud9 is a travelling agency that firmly believes that <span>life is about journeys, not destinations.</span></p>
          </ScrollAnimation>
        
        </div>

        <div class="box">
          <ScrollAnimation>
        <p>If you are tired of the usual boring vacation and you seek to live magical, unforgettable moments, the wind has taken you to the right place: <span>what we offer is not just a trip—what we give you is the experience of a lifetime.</span></p>
          </ScrollAnimation>
        </div>

        <div class="box">
          <ScrollAnimation>
        <p>Other agencies specialize in travel—<span>we specialize in dreams.</span></p>

          </ScrollAnimation>
        </div>

        <div class="box">
        
          <ScrollAnimation>
        <p>What are you waiting for? <span>Your perfect moment awaits you on cloud nine!</span></p>
          </ScrollAnimation>

        </div>

        <div class="box">
          <ScrollAnimation>
          <p class="redirect">(don't just take our word for it: <a href="#reviews">see what they say about us!</a>)</p>

          </ScrollAnimation>

        </div>
        </div>

    </section>
</template>

<style scoped>

  #philosophy {
    text-align: center;
    min-height: 100vh; 
    padding: 1rem; 
    max-width: 1100px;
    margin: auto; 
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 1.5rem;
  }

  h1 {
    font-weight: normal;
    font-size: 3rem;
    margin-bottom: 7rem;
    background: linear-gradient(90deg, hsla(312, 77%, 86%, 1) 0%, hsla(220, 61%, 79%, 1) 100%);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  .box {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .box:first-of-type {
    align-items: flex-start;
    height: 60vh;
  }

  p {
    font-size: 2rem;
    max-width: 700px;
  }

  span {
    background: linear-gradient(90deg, hsla(333, 100%, 53%, 1) 0%, hsla(33, 94%, 57%, 1) 100%);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  .redirect a {
    background: hsla(312, 77%, 86%, 1);
    background: linear-gradient(90deg, hsla(312, 77%, 86%, 1) 0%, hsla(220, 61%, 79%, 1) 100%);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent; 
  }

  .redirect a:hover {
    text-decoration: underline; 
    text-decoration-color: hsla(220, 61%, 79%, 1);
  }
</style>
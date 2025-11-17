<script>
import reviewData from '../../data/reviewData';
import ReviewCard from '../ReviewCard.vue';

  export default {
    components: { ReviewCard },
    data() {
        return {
            reviews: reviewData,
        }
    }
  }
</script>

<template>
    <section id="reviews">
        <h1>our customers' reviews</h1>

        <div class="container">
            <ReviewCard v-for="review in reviews"
                :key="review.id"
                :text="review.text"
                :user="review.userName"
                :avatar="review.avatar"
                :rating="review.rating"
                :index="review.id"
                :credits="review.credits" />
        </div>
    </section>
</template>

<style scoped>
   #reviews {
    max-width: 1300px;
    margin: 3rem auto;
    min-height: 100vh;
    padding-inline: 1rem;
   }

   h1 {
    font-weight: normal;
    text-align: center;
    background: linear-gradient(90deg, hsla(333, 100%, 53%, 1) 0%, hsla(33, 94%, 57%, 1) 100%);
    -webkit-background-clip: text;
    background-clip: text;
   -webkit-text-fill-color: transparent;
   }

   .container {
    display: flex;
    gap: 1rem;
    margin-top: 8rem;
    overflow: hidden;
    position: relative;
    height: 420px;
    width: 100%;
    pointer-events: none; 
    padding-block: 1rem;
    mask-image: linear-gradient(to right, transparent, black 5%, black 95%, transparent);
   }

</style>
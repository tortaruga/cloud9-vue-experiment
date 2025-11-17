<script>
   export default {
    props: {
        text: String,
        avatar: String,
        user: String,
        rating: Number,
        index: Number,
        credits: String,
    }
   }
</script>

<template>
    <div class="review-card" :style="{'--index': index}">
         <header>
            <a :href="credits"><img :src='avatar' alt="user avatar"></a>
            <p>{{ user }}</p>
         </header>
         <div class="rating">
            <img v-for="i in rating"  src="/images/star.svg" alt="star icon">
         </div>
        <p>{{ text }}</p>
    </div>
</template>

<style scoped>
  .review-card {
    background: linear-gradient(-45deg, #2121211c,#212121b0);
    color: grey;
    padding: 2rem;
    border-radius: 1rem;
    width: 40%;
    flex-shrink: 0;
    animation: scroll 90s infinite linear;
    animation-delay: calc(90s / 5 * (5 - var(--index)) * -1);    
    position:absolute;
    left: 100%;
    pointer-events: auto;
    min-width: 300px; 
    height: 95%;
    box-shadow: -.3rem -.2rem 10px rgba(137, 43, 226, 0.142),
    .3rem .2rem 5px rgba(0, 182, 249, 0.042);
    font-size: .9rem;
  }

header {
    display: flex;
    align-items: center;
    gap: .75rem;
    background: linear-gradient(90deg, rgb(216, 69, 136) 0%, rgb(255, 150, 23) 100%);
    -webkit-background-clip: text;
    background-clip: text;
   -webkit-text-fill-color: transparent;

    img {
        width: 3rem;
    }
}

.rating {
    display: flex;
    gap: .25rem;
    margin-block: 1rem 2rem;

    img {
        width: 1rem; 
    }
}

@keyframes scroll {
    to {
        left: -470%;
    }
}


@media screen and (min-width: 400px) {
 @keyframes scroll {
    to {
        left: -350%;
    }
}
}


@media screen and (min-width: 550px) {
 @keyframes scroll {
    to {
        left: -240%;
    }
}
}

@media screen and (min-width: 950px) {
    .review-card {
        font-size: 1rem;
    }

    @keyframes scroll {
    to {
        left: -150%;
    }
}
}

</style>
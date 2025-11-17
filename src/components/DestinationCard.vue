<template>
    <div class="destination-card">
        <img :src="img" alt="destination photo">
        
        <a :href="href" target="_blank">
        <h2>{{ name }}</h2>
        </a>
        
        <div class="info">
            <p>{{ description }}</p>
        </div>
    </div> 
</template>

<script>
  export default {
    props: {
        img: String,
        name: String,
        description: String,
        href: String,
    }
  }
</script>

<style scoped>

.destination-card {
    width: 100%; 
    align-items: stretch;
    flex: 1;
    transition: .3s;
    position: relative;
    overflow: hidden;
}

.destination-card::after  {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(to bottom, rgba(0, 0, 0, 0.084), rgba(0, 0, 0, 0.778));
    opacity: 0;
    transition: .3s;
}

img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    filter: grayscale(1) brightness(.3);
    transition: .3s;
}

.destination-card:hover {
    flex: 5;
}

.destination-card:hover img {
    filter: brightness(1) grayscale(0);
    transform: scale(1.3);
}

.destination-card:hover:after {
    opacity: 1;
}

h2 {
    position: absolute;
    bottom: 30%;
    left: 50%;
    transform: translateX(-50%);
    transition: .4s;
    color: grey;
    padding: .25rem .8rem;
    border-radius: .3rem;
    z-index: 1;
}

p {
    position: absolute;
    max-width: 500px;
    color: white;
    font-weight: bold;
    transition: .4s;
    opacity: 0;
    bottom: -150%;
    left: 50%;  
    transform: translateX(-50%);
    background: linear-gradient(90deg, hsla(312, 77%, 86%, 1) 0%, hsla(220, 61%, 79%, 1) 100%);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    z-index: 1;
    text-align: center;
    font-size: 1.3rem;
}


.destination-card:hover h2 {
  bottom: 60%;
  background: linear-gradient(90deg, hsla(348, 88%, 66%, 1) 0%, hsla(36, 89%, 68%, 1) 100%);      background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
   font-size: 3rem;
}

.destination-card:hover p {
    bottom: 10%;
    opacity: 1;
}

@media screen and (min-width: 650px) {
    .destination-card {
        width: calc(100% / 4);
    }
    
    .destination-card:nth-child(odd) {
       transform: translateY(-5%);
    }

    h2 {
        bottom: 45%;
    }

    .destination-card:hover h2 {
        bottom: 45%;
    }
}

</style>
<script>
import DestinationCard from '../DestinationCard.vue';

  export default {
    components: {DestinationCard},
    data() {
        return {
            destinations: [
                {
                    id: 0,
                    name: 'Japan',
                    img: '/images/japan.jpg',
                    description: "There's nothing like seeing Mount Fuji from above the crater",
                    credits: 'https://it.freepik.com/foto-gratuito/monte-fuji-con-via-lattea-di-notte_10695684.htm',
                },

                {
                    id: 1,
                    name: 'Thailand',
                    img: '/images/thailand.jpg',
                    description: 'Just think of landing right in the middle of those bright blue waters',
                    credits: 'https://it.freepik.com/foto-gratuito/vista-aerea-di-belle-montagne-nella-diga-di-ratchaprapha-al-parco-nazionale-di-khao-sok-provincia-di-surat-thani-thailandia_13180349.htm',
                },

                {
                    id: 2,
                    name: 'Iceland',
                    img: '/images/iceland.jpg',
                    description: "We're bringing you so close to the Northern Lights you'll be able to hold out a hand and grab them",
                    credits: 'https://it.freepik.com/foto-gratuito/northern-light-aurora-boreale-alla-cascata-godafoss-in-inverno-islanda_11769019.htm',
                },

                {
                    id: 3,
                    name: 'Turkey',
                    img: '/images/turkey.jpg',
                    description: 'Fairy chimneys–a classic!',
                    credits: 'https://it.freepik.com/foto-gratuito/citta-di-goreme-al-crepuscolo-in-cappadocia-turchia_11768865.htm',
                },
            ]
        }
    }
  }
</script>

<template>
    <section id="destinations">
        <h1>Popular destinations</h1>

        <div class="container">
            <DestinationCard v-for="destination in destinations" 
                :key="destination.index"
                :name="destination.name"
                :img="destination.img"
                :description="destination.description"
                :href="destination.credits" />
        </div>
    </section>
</template>

<style scoped>
   #destinations {
    min-height: 130vh; 
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    max-width: 1100px;
    margin: auto;
   }

   .container {
    display: flex;
    gap: 1rem;
    justify-content: center;
    height: 90vh;
    flex-direction: column;
   }

h1 {
    text-align: center;
    font-weight: normal;
    background: linear-gradient(90deg, hsla(312, 77%, 86%, 1) 0%, hsla(220, 61%, 79%, 1) 100%);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

@media screen and (min-width: 650px) {
    .container {
        flex-direction: row;
        min-height: 80vh;
    }
}
</style>
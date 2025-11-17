<template>
    <section id="events">
        <h2>Hurry! There are only few seats left for our next experiences</h2>

        <div class="container">
            <div v-for="(card, index) in cards" :key="index" class="event-card">
               <img :src="card.src" alt="random picture not necessarily linked to the actual destination...">
                <div class="content">
                
                <h3>{{ card.event }}</h3>

                <a :href="card.href" target="_blank">{{ card.desc }}</a>

                <button>book flight</button>
                </div>
            
            </div>
        </div>
        
    </section>
</template>

<script>
  export default {
    data() {
        return {
            cards: [

            {
                event: 'The world seen from Himalaya',
                date: 'from 01/06 to 12/06',
                src: 'images/totally-not-himalaya.jpg',
                desc: 'That is not a picture of Himalaya.',
                href: 'https://it.freepik.com/foto-gratuito/siluetta-del-fotografo-con-la-macchina-fotografica-e-il-blackground-della-via-lattea_13180504.htm',
            },

            {
                event: 'Bear riding in Siberia',
                date: 'from 23/04 to 30/04',
                src: 'images/not-siberia.jpg',
                desc: 'And that is definitely not Siberia.',
                href: 'https://it.freepik.com/foto-gratuito/bellissimo-paesaggio-al-tramonto-sul-parco-nazionale-deogyusan-in-inverno-corea-del-sud_11599644.htm'
            },

            {
                event: 'Magic nights in Istanbul',
                date: 'from 24/05 to 30/05',
                src: 'images/istanbul.jpg', 
                desc: 'Uncharacteristically, that is an actual picture of Istanbul.',
                href: 'https://it.freepik.com/foto-gratuito/vista-aerea-della-citta-di-istanbul-all-alba-in-turchia_11768849.htm',
            },
        ]
    }}
  }
</script> 

<style scoped>

#events {
    max-width: 1100px;
    margin: auto;
    min-height: 110vh; 
    padding: 3rem 1rem ;
    background-position: center;
    background-size: 100%;
}

img {
    height: 100%;
    object-fit: cover;
    position: absolute;
    transition: .3s ;
}

h2 {
    margin-bottom: 5rem;
    background: linear-gradient(90deg, hsla(312, 77%, 86%, 1) 0%, hsla(220, 61%, 79%, 1) 100%);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    font-weight: normal;
    text-align: center;
}

a {
    text-align: center;
    padding-inline: 2rem;
}

a:hover {
    text-decoration: underline;
}

.container {
    display: flex;
    flex-wrap: wrap;
    gap: 2rem;
    justify-content: space-around;
    align-items: center;
}

.content {
    position: absolute; 
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between; 
    height: 100%; 
    background: linear-gradient(rgba(0, 0, 0, 0.46), black);
    top: 70%;
    transition: .3s;
}

.event-card:hover .content {
    top: 0;
}

.event-card:hover img {
    transform: scale(1.5);
}

.event-card {
    border: 1px solid rgba(128, 128, 128, 0.26);
    border-radius: .5rem;
    aspect-ratio: 2/3;
    width: 300px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    box-shadow: 0 0 5px hsla(300, 100%, 50%, 0.2),
                .7rem .5rem 15px black;
    background: linear-gradient(45deg, hsla(312, 77%, 86%, .01) 0%, hsla(220, 61%, 79%, .1) 100%);
    transform: scale(.9); 
    transition: .3s;
    position: relative;
    overflow: hidden;
}


.event-card:hover {
    transform: scale(1);
}


.event-card:nth-child(2) {
    translate: 0 1.5rem;
}

.event-card:last-child {
   translate: 0 3rem;
}


header {
    padding: 1rem;
    border-radius: .5rem .5rem 0 0;
    text-align: center;
    color: grey;
}

h3 {
    font-size: 2rem;
    text-align: center;
    color: hsla(220, 61%, 79%, 1);
}

button {
    padding: 1rem 3rem;
    border: none;
    border-radius: .3rem;
    margin-bottom: 1.5rem; 
    width: 70%;
    align-self: center;
    font-weight: bold;
    text-transform: uppercase;
    color: rgb(230, 230, 218);
    background: linear-gradient(90deg, hsla(312, 77%, 86%, 1) 0%, hsla(220, 61%, 79%, 1) 100%);
    color: #212121;
    position: relative;
    z-index: 1;
    overflow: hidden;
}

button::after {
    content: '';
    position: absolute;
    inset: 0;
    z-index: -1;
    transition: .5s;
    opacity: 0;
    background: linear-gradient(90deg, hsla(333, 100%, 53%, 1) 0%, hsla(33, 94%, 57%, 1) 100%);
}

button:hover:after {
    opacity: 1;
}

button:hover {
      color: rgb(230, 230, 218);

} 
</style>
<script>
export default {
    data() {
        return {
            buttons: [{text: 'about us', id: '#philosophy'}, {text: 'explore destinations', id: '#destinations'}],
        }
    }
}
</script>

<template>
    <section id="intro">
        <div class="logo-section">
            <h1>cloud9</h1>
            <p class="motto">dove ti porta il vento</p>
        </div>

        <div class="desc">
            <p class="description">forget planes, cruise ships, and all that boring stuff: the new hot trend is air balloons!</p>
            <div class="buttons">
                <a v-for="(button, index) in buttons" :key="index" :href="button.id">{{ button.text }}</a>
            </div>
        </div>
    </section>
</template>

<style scoped>

#intro {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    max-width: 1200px;
    margin-inline: auto;
    margin-bottom: 7rem;
    min-height: 90vh;
    align-items: center;
    gap: 5rem;
    padding-inline: 1rem;
}

.logo-section {
    text-align: center;
}

.logo-section h1 {
    font-size: 5rem;
    margin: 0;
    background: linear-gradient(90deg, hsla(333, 100%, 53%, 1) 0%, hsla(33, 94%, 57%, 1) 100%);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
}

.logo-section p {
    font-size: 1.2rem;
    text-transform: uppercase;
}

.desc {
    text-align: center;
    font-size: 1.5rem;
    max-width: 600px;
}

.buttons {
    display: flex;
    gap: 1rem;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
}

.buttons a {
    background: hsla(220, 61%, 79%, 1);
    background: linear-gradient(90deg, hsla(312, 77%, 86%, 1) 0%, hsla(220, 61%, 79%, 1) 100%);
    color: #121212;
    border-radius: 2rem;
    padding: .3rem 1.5rem;
    text-decoration: none;
    border: 2px solid transparent;
    transition: .3s;
    font-size: 1.1rem;
    overflow: hidden;
    position: relative;
    z-index: 1;
}

.buttons a::after {
    content: '';
    inset: 0;
    position: absolute;
    background: linear-gradient(90deg, hsla(333, 100%, 53%, 1) 0%, hsla(33, 94%, 57%, 1) 100%);
    z-index: -1;
    opacity: 0;
    transition: .3s;
    
}

.buttons a:hover::after {
    opacity: 1;
}

.buttons a:hover {
    border: 2px solid #121212; 
}

.buttons a:last-child {
    background-color: transparent; 
    background: none;
    border: 2px solid  hsla(312, 77%, 86%, 1);
    color:hsla(312, 77%, 86%, 1);
}

.buttons a:last-child:hover {
    color: #121212;
    border: 2px solid transparent; 

}

@media screen and (min-width: 500px) {
    .logo-section h1 {
        font-size: 7rem;
    }
}

</style>
<script>
  export default {
    data() {
        return {
            navLinks: [{
                name: 'our philosophy',
                href: '#philosophy',
            },
        
            {
                name: 'popular destinations',
                href: '#destinations',
            },

            {
                name: 'reviews',
                href: '#reviews',
            },

            {
                name: 'events',
                href: '#events',
            },

            {
                name: 'contacts',
                href: '#contacts',
            },
        ],
        }
    }
  }
</script>

<template>
    <nav>
        <ul>
            <li class="logo">cloud9</li>
            <li v-for="(li, index) in navLinks" :key="index">
                <a :href="li.href">{{ li.name }}</a>
            </li>
        </ul>
    </nav>
</template>

<style scoped>
nav {
    background-color: #2121213b;
}

ul {
    list-style-type: none;
    display: flex;
    flex-wrap: wrap;
    gap: 1.5rem;
    justify-content: space-around;
    color: grey;
    margin: 0;
    padding: 2rem 1rem;
    align-items: center;
    font-size: .9rem;
}

li {
    padding-left: 0;
}

a {
    text-decoration: none;
    color: inherit;
    padding: .25rem .7rem;
    border-radius: 1rem;
}

a:hover {
    background-color: #333;
}

.logo {
    font-size: 1.7rem;
    background: hsla(333, 100%, 53%, 1);
    font-weight: bold;
    background: linear-gradient(90deg, hsla(333, 100%, 53%, 1) 0%, hsla(33, 94%, 57%, 1) 100%);
    -webkit-background-clip: text;
    background-clip: text;
   -webkit-text-fill-color: transparent;
}

</style>
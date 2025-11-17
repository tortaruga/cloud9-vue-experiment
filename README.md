## overview

This is a mock website for a travel agency, created as a way to practice using Vue for the first time.
I chose a simple project to get familiar with Vue’s syntax and core concepts. Overall, I found Vue's syntax to be more straightforward than React, though I’m more experienced with React and would still prefer it for most projects. 

For styling, I used `<style scoped>` to keep styles component-specific. While this method can be useful to avoid global style conflicts, I think it can become messy easily. In the future, I’d prefer using Sass to keep styles modular and separate from component logic.

### features

This single-page application includes the following sections: Intro, About, Popular Destinations, Customer Reviews, Upcoming Events, and Contacts.

- About Section: Features a simple scroll-triggered text animation, built using Vue’s ref and onMounted.
- Popular Destinations: Cards expand on hover to reveal brief descriptions, adding interactivity to the layout.
- Customer Reviews: Includes a CSS-only infinite scroll animation for a smooth, dynamic gallery experience.
- Upcoming Events: Event cards animate on hover.
- Disclaimer: Displayed using a classic marquee effect.


#### notes

As this was my first time using Vue, I expected to run into more challenges. Surprisingly, I found the syntax more approachable than anticipated.
I used the Options API, which worked well for a small project like this; however in future projects I’d like to explore the Composition API.
Since this project was mostly a practice in building components I kept things simple, but I'd like to explore more about reactive data and state management in Vue.

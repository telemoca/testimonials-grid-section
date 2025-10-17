<script setup lang="ts">
import { ref } from "vue";
import Testimonial from "./Testimonial.vue";

const persons = ref([
  {
    name: "Daniel Clifford",
    role: "Verified Graduate",
    title:
      "I received a job offer mid-course, and the subjects I learned were current, if not more so, in the company I joined. I honestly feel I got every penny's worth.",
    text: "“ I was an EMT for many years before I joined the bootcamp. I've been looking to make a transition and have heard some people who had an amazing experience here. I signed up for the free intro course and found it incredibly fun! I enrolled shortly thereafter. The next 12 weeks was the best - and most grueling - time of my life. Since completing the course, I've successfully switched careers, working as a Software Engineer at a VR startup. ”",
    img: "./image-daniel.jpg",
  },
  {
    name: "Jonathan Walters",
    role: "Verified Graduate",
    title: "The team was very supportive and kept me motivated",
    text: "“ I started as a total newbie with virtually no coding skills. I now work as a mobile engineer for a big company. This was one of the best investments I've made in myself. ”",
    img: "./image-jonathan.jpg",
  },
  {
    name: "Kira Whittle",
    role: "Verified Graduate",
    title: "Such a life-changing experience. Highly recommended!",
    text: "“ Before joining the bootcamp, I've never written a line of code. I needed some structure from professionals who can help me learn programming step by step. I was encouraged to enroll by a former student of theirs who can only say wonderful things about the program. The entire curriculum and staff did not disappoint. They were very hands-on and I never had to wait long for assistance. The agile team project, in particular, was outstanding. It took my learning to the next level in a way that no tutorial could ever have. In fact, I've often referred to it during interviews as an example of my developent experience. It certainly helped me land a job as a full-stack developer after receiving multiple offers. 100% recommend! ”",
    img: "./image-kira.jpg",
  },
  {
    name: "Jeanette Harmon",
    role: "Verified Graduate",
    title: "An overall wonderful and rewarding experience",
    text: "“ Thank you for the wonderful experience! I now have a job I really enjoy, and make a good living while doing something I love. ”",
    img: "./image-jeanette.jpg",
  },
  {
    name: "Patrick Abrams",
    role: "Verified Graduate",
    title:
      "Awesome teaching support from TAs who did the bootcamp themselves. Getting guidance from them and learning from their experiences was easy.",
    text: "“ The staff seem genuinely concerned about my progress which I find really refreshing. The program gave me the confidence necessary to be able to go out in the world and present myself as a capable junior developer. The standard is above the rest. You will get the personal attention you need from an incredible community of smart and amazing people. ”",
    img: "./image-patrick.jpg",
  },
]);
</script>

<template>
  <div class="container">
    <Testimonial :person="persons[0]!" class="testimonial"></Testimonial>
    <Testimonial :person="persons[1]!" class="testimonial"></Testimonial>
    <Testimonial :person="persons[2]!" class="testimonial"></Testimonial>
    <Testimonial :person="persons[3]!" class="testimonial"></Testimonial>
    <Testimonial :person="persons[4]!" class="testimonial"></Testimonial>
  </div>
</template>

<style>
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  height: 100vh;
  display: grid;
  place-content: center;
}

@media (max-width: 1150px) {
  body {
    display: block;
  }
}
</style>

<style scoped>
.container {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1.5rem;
  grid-template-areas:
    "one one two three"
    "four five five three";
  padding: 2rem;
  font-family: "Barlow Semi Condensed", sans-serif;
  width: clamp(370px, 80%, 1250px);
  margin: 0 auto;
}

.testimonial {
  border-radius: 15px;
  padding: 2rem;
  box-shadow: 0px 5px 25px -15px black;
}

.testimonial:nth-child(1) {
  color: white;
  grid-area: one;
  background-color: hsl(263, 55%, 52%);
  background-image: url("/bg-pattern-quotation.svg");
  background-repeat: no-repeat;
  background-position: 80% top;
}
.testimonial:nth-child(2) {
  color: white;
  grid-area: two;
  background-color: #49556b;
}
.testimonial:nth-child(3) {
  color: hsl(219, 29%, 14%);
  grid-area: three;
  background-color: white;
}
.testimonial:nth-child(4) {
  color: hsl(219, 29%, 14%);
  grid-area: four;
  background-color: white;
}
.testimonial:nth-child(5) {
  color: white;
  grid-area: five;
  background-color: #191f2d;
}

@media (max-width: 1150px) {
  .container {
    grid-template-areas:
    "one one"
    "two three"
    "four three"
    "five five";
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 700px) {
  .container {
    grid-template-areas:
      "one"
      "two"
      "three"
      "four"
      "five";
    grid-template-columns: 1fr;
  }
}
</style>

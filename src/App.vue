<template>
<div class="firstsection">
    <section class="first image section">
<nav class="level">
  <p class="level-item has-text-centered">
    <a class="link is-info">Home</a>
  </p>
  <p class="level-item has-text-centered">
    <a class="link is-info">Menu</a>
  </p>
  <p class="level-item has-text-centered">
    <a class="link is-info">Menu</a>
  </p>
  <p class="level-item has-text-centered">
    <a class="link is-info">Reservations</a>
  </p>
  <p class="level-item has-text-centered">
    <a class="link is-info">Contact</a>
  </p>
</nav>
</section>
</div>

<div class="hero-image">
  <div class="hero-text">
    <h1 style="font-size:50px">Minu porfoolio ootab tutvumist</h1>
    <h3>ja ma tegelen ka programmeerimisega</h3>
    <button>Hire me</button>
  </div>
</div>

<div class="container">
    <section class="section" >
        <button class="button is-primary" @click="active=true">Click me</button>
        <button class="button is-primary" @click="active2=true">Click me2</button>
        <modal 
            v-if="active"
            @close="active=false"
            url="https://bulma.io/images/placeholders/1280x960.png"
        >
        </modal>
        <modal 
            v-show="active2"
            @close="active2=false"
            url="https://placekitten.com/1280/960"
        >
        </modal>
    </section>
</div>


</template>

<script>
import Modal from './components/Modal.vue'
export default {
    components: { Modal },
    data(){
        return {
            active: false,
            active2: false
        }
    },
    methods: {
        
    }
}
</script>

<style>


</style>
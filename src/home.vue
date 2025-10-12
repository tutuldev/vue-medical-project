<template>
<div class="w3-bar w3-black">
  <button class="w3-bar-item w3-button" @click="myactivetab='london'">London</button>
  <button class="w3-bar-item w3-button" @click="myactivetab='paris'" >Paris</button>
  <button class="w3-bar-item w3-button" @click="myactivetab='tokyo'">Tokyo</button>
</div>
<component :is="myactivetab"></component>
</template>
<script>
    import london from './components/london.vue'
    import paris from './components/paris.vue'
    import tokyo from './components/tokyo.vue'

    export default {
        name: "home",
        components: {
            london,
            paris,
            tokyo
        },
        data() {
            return {
                myactivetab: 'london'
            }
        },
    }
</script>
<template>
  <div>
   <Hero/>
  </div>
</template>
<script>

  useHead({
    title:'CarTrader'
  });

  import Hero from '../components/Car/Hero.vue'
  export default {
    components:{
      Hero
  }
}
</script>

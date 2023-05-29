<script setup>
  const route = useRoute()
  useHead({
    title:toTitleCase(route.params.name)
  })

  function toTitleCase(str) {
  return str.replace(/\w\S*/g, function (txt){
    return txt.charAt(0).toUpperCase() + txt.substr(1).toLowerCase();
  });
}
  
</script>
<template>
  <div>
    <div class="mx-auto mt-4 max-w-7xl space-y-4 px-4 xs:px-8 sm:px-10 lg:px-16 pb-16 w-3/5">
        <DetailHero />
        <DetailAttributes />
        <DetailDescription title="lorem"/>
        <DetailContact />
    </div>    
  </div>
</template>

<script>
import DetailHero from '@/components/Detail/Hero.vue'
import DetailAttributes from '@/components/Detail/Attributes.vue'
import DetailDescription from '@/components/Detail/Description.vue'
import DetailContact from '@/components/Detail/Contact.vue'

export default {
    components:{
        DetailDescription,
        DetailHero,
        DetailAttributes,
        DetailContact
    }
}
</script>
<template>
  <div>
      <div class="mt-32 flex">
        <SideBar />
        <NuxtPage />
      </div>
    </div>

</template>

<script setup>

definePageMeta({
  layout: "custom",
});

const route = useRoute();

useHead({
  title: `${route.params.make ? toTitleCase(route.params.make):'Cars'} in ${toTitleCase(route.params.city)}`,
});

function toTitleCase(str) {
  return str.replace(/\w\S*/g, function (txt){
    return txt.charAt(0).toUpperCase() + txt.substr(1).toLowerCase();
  });
}
</script>

<script>
import SideBar from "@/components/Car/SideBar.vue";

export default {
  components: {
    SideBar,
  },
};
</script>
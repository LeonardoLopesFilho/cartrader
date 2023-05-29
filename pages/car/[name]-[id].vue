<script setup>
const route = useRoute();
useHead({
  title: toTitleCase(route.params.name),
});

definePageMeta({
  layout: "custom",
});

function toTitleCase(str) {
  return str.replace(/\w\S*/g, function (txt) {
    return txt.charAt(0).toUpperCase() + txt.substr(1).toLowerCase();
  });
}
</script>
<template>
  <DetailHero />
  <DetailAttributes />
  <DetailDescription title="lorem" />
  <DetailContact />
</template>

<script>
import DetailHero from "@/components/Detail/Hero.vue";
import DetailAttributes from "@/components/Detail/Attributes.vue";
import DetailDescription from "@/components/Detail/Description.vue";
import DetailContact from "@/components/Detail/Contact.vue";

export default {
  components: {
    DetailDescription,
    DetailHero,
    DetailAttributes,
    DetailContact,
  },
};
</script>
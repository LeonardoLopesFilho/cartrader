<template>
  <div class="font-serif w-[1000px] text-2xl rounded-full bg-white flex justify-between overflow-hidden drop-shadow-2xl mx-auto">
    <input type="text"
      class="py-3 px-5 w-full text-2xl rounded-full focus:outline-none"
      placeholder='Search by city....'
      :class="cityError ? 'border-red-500 border' : ''"
      v-model="city"
      />
    <button class="bg-sky-500 px-10 text-white"  @click="heandleSearch()">Search</button>
  </div>
</template>
<script>
export default {
  name: "SearchBar",
  data() {
    return {
      city:'',
      cityError:false
    };
  },
  methods: {
    heandleSearch() {
      if(!this.city){
        this.cityError = true
        return this.cityError
      }
      navigateTo(`/city/${this.city}/car`);
    },
  },
};
</script>


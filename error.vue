<template>
  <div class="flex h-screen justify-center items-center flex-col">
    <h1 class="text-9xl">404</h1>
    <p class="mt-7 text-4xl">Page Not Found</p>
    <button class="rounded mt-7 text-2cl bg-blue-400 px-7 py-4 text-white" @click="voltar()">
        Go Back
    </button>
  </div>
</template>

<script>
export default {
    methods:{
        voltar(){
            navigateTo("/")
        }
    }
}
</script>

<style>

</style>
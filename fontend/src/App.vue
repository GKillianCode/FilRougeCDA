<script>
export default{
  data(){
    return{

    }
  },
  methods: {

  }
}
</script>

<template>
  <div class="app">
    <NavigationComponent v-if="$route.name !== 'login'" />
    <router-view />
  </div>
</template>

<style lang="scss">
@import "@/css/main.css"; 
</style>

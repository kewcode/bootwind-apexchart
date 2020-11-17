<template>
<div :class="settings">
    <topheader />
    <settings class="z-50" />
    <main>
        <transition
          name="slide-fade"
        >
            <Nuxt />
        </transition>
    </main>
</div>        
</template>

<script>
export default {
  computed:{
    settings(){
      return this.$store.state.theme+" "+ this.$store.state.primaryColor;
    }
  },
}
</script>

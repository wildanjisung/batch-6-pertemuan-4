<template>
  <div class="about">
    <h1>This is an about page</h1>
    <HelloWorld pesan="Welcome to About Page" @update-ajah='doIncrement'/>
    <p>nilai: {{ nilai }} </p>
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'AboutView',
  data() {
    return {
      nilai: 0
    }
  },
  methods: {
    munculinTulisan() {
      console.log("haii saya tulisan");
    },
    doIncrement() {
      this.nilai++
    }
  },
  components: {
    HelloWorld
  },
  mounted() {
    console.log('halaman mounted');
    console.log('nilai semula: ', this.nilai);
    this.nilai++
    console.log('nilai sesudah: ', this.nilai);
  }
}
</script>
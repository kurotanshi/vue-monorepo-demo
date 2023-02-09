<script setup>
import { ref } from 'vue'
import { getNumber } from '@vueapps/utils'
import { Modal } from '@vueapps/components'

import HelloWorld from '/src/components/HelloWorld.vue';
import { HelloWorldVue as HW2 } from '@vueapps/v-app-2'
import { HelloWorldVue as HW3 } from '@vueapps/v-app-3'


const isModalShow = ref(false);
</script>

<template>
  <div id="app">
    <h1>Hello</h1>
    <h1>getNumber: {{ getNumber() }}</h1>
    
    <button @click="isModalShow = true">Show Modal</button>

    <Modal 
      :isShow="isModalShow"
      @close="isModalShow = false">
      <h1>Hello!</h1>
    </Modal>

    <HelloWorld />
    <HW2 />
    <HW3 />
  </div>
</template>

<style scoped>
#app {
  padding: 1rem;
}
</style>

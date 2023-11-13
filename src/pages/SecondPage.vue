<template>
    <q-page class="flex flex-center">
      <PipesCrm/>
    </q-page>
  </template>
  
  <script>
  import { defineComponent } from 'vue'
  import PipesCrm from 'src/components/Pipes-Crm.vue';
  
  export default defineComponent({
    name: 'SecondPage',
    components: {
      PipesCrm,
    }
  })
  </script>
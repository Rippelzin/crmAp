<template>
  <q-page class="flex flex-center">
    <PipesCrm :list="listaUsuarios" />
    <button @click="addUser">ADD USER</button>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import PipesCrm from "src/components/Pipes-Crm.vue";
import axios from "axios";

export default defineComponent({
  name: "IndexPage",
  components: {
    PipesCrm,
  },
  data() {
    return {
      listaUsuarios: [],
    };
  },
  mounted() {
    this.getUsers();
  },
  updated() {
    this.getUsers();
  },
  methods: {
    getUsers() {
      const url = "https://jsonplaceholder.typicode.com/users";
      axios.get(url).then((response) => (this.listaUsuarios = response.data));
    },

    addUser() {
      let newUser = {
        username: "teste",
        name: "teste",
        email: "email@eamil.com",
      };
      this.listaUsuarios.push(newUser);
      console.log(this.listaUsuarios);
    },
  },
});
</script>

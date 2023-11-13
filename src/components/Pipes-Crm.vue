<template>
  <q-page class="main">
    <div v-for="(item, index) in this.list" :key="index" class="pipe">
      <div>
        <p>{{ item.username }}</p>

        <p>{{ item.name }}</p>
        <p>{{ item.email }}</p>
      </div>
    </div>
  </q-page>
</template>
<script>
let leads = 10;
const type = "Leads";

export default {
  data() {
    return {
      titulo: "titulo",
      dados: leads,
      dadosType: type,
    };
  },
  props: {
    list: Object,
  },
  methods: {
    nextPage() {},
  },
};
</script>

<style>
.main {
  display: flex;
}
.pipe {
  display: grid;
  justify-content: center;
  align-items: center;
}
</style>

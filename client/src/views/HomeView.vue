<template >
  <div class="home">
     <Table :columns="columns" :rows="rows" />
  </div>
</template>

<script>
// @ is an alias to /src
import Table from '@/components/Table.vue'

export default {
  name: 'HomeView',
  components: {
    Table
  },
    data() {
    return {
      columns: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12],
      rows: [],
    };
  },

  mounted() {
    this.generateTable();
  },
  methods: {
    generateTable() {
      const rows = [];
      for (let i = 1; i <= 12; i++) {
        const row = [i];
        for (let j = 1; j <= 12; j++) {
          row.push(i * j);
        }
        rows.push(row);
      }
      this.rows = rows;
    },
  },
}
</script>

<template>
   <h2 class="text-center">Multiplication Table</h2>
  <div class="flex justify-center mt-4">
    <table class="h-96">
      <thead>
        <tr>
          <th></th>
          <th class="bg-yellow-400" v-for="(column, index) in columns" :key="index">{{ column }}</th>
        </tr>
      </thead>
      <tbody>
        <tr  v-for="(row, index) in rows" :key="index">
          <td class="p-4 bg-blue-300" >{{ row[0] }}</td>
          <td  class="p-4 bg-red-300" v-for="(column, index) in row.slice(1)" :key="index">
            {{ column }}
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "Table",
  props: {
    columns: {
      type: Array,
      required: true,
    },

    rows: {
      type: Array,
      required: true,
    },
  },
};
</script>
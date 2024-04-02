<template>
  <tr class="table-item__table-row">
    <td>{{ title }}</td>
    <td>{{ isbn }}</td>
    <td></td>
  </tr>
</template>

<style scoped>
.table-item__table td {
  padding: 12px 15px;
}
</style>

<script>
export default {
  name: "BookListRow",
  props: {
    title: String,
    isbn: Number,
  },
};
</script>

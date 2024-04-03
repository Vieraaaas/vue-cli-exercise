<template>
  <tr class="table-item__table-row">
    <td>{{ title }}</td>
    <td>{{ isbn }}</td>
    <td><BaseButton text="Add Bookmark" variant="secondary" /></td>
  </tr>
</template>

<style scoped>
.table-item__table td {
  padding: 12px 15px;
}
</style>

<script>
import BaseButton from "@/components/BaseButton.vue";
export default {
  name: "BookListRow",
  props: {
    title: String,
    isbn: String,
  },
  components: {
    BaseButton,
  },
};
</script>

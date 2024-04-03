<template>
  <tr class="table-item__table-row">
    <td>{{ title }}</td>
    <td>{{ isbn }}</td>
    <td>
      <BaseButton
        @ButtonClicked="toggleBookmarked"
        :text="bookMarkedText"
        variant="secondary"
      />
    </td>
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
    isBookmarked: {
      type: Boolean,
      default: false,
    },
  },
  components: {
    BaseButton,
  },
  computed: {
    bookMarkedText() {
      return this.isBookmarked ? "Remove Bookmark" : "Add Bookmark";
    },
  },
  methods: {
    toggleBookmarked() {
      this.$emit("bookmark-clicked", this.isbn);
    },
  },
};
</script>

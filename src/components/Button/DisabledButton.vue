<script>
export default {
  props: ["param", "size"],
};
</script>


<template>
  <button class="
          h-8
          px-4
          m-2
          text-sm
          disabled:opacity-50
          bg-gray-100
          border-2
          transition-colors
          duration-150
          rounded-lg
          focus:shadow-outline
        " id="myBtn" disabled style="margin: 5px">
    {{ param }}
  </button>
</template>
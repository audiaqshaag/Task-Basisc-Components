<script>
export default {
    name: 'MyShowPassword',
  props: ["value", "type", "togglePassword", "placeholder", "Attributes"],methods: {
      myFunction(){
          console.log('action ok')
          this.$emit('customFunction');
      }
  }
};
</script>


<template>
  <input
    class="border background-gray-100 border-black p-2 rounded-sm"
    type="checkbox"
    @change="myFunction"
  />
</template>




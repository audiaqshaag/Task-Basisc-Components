<script>
export default {
  props: ["value", "type",  "placeholder", ],
};
</script>


<template>
  <input 
  class="border background-gray-100 border-black p-2 rounded-sm"
   placeholder="Password" :type="computedType"  id="myInput"/>
</template>

<script>
  export default {
    name: 'MyPasswordInput',
    props: {
      isShowPassword: {
        type: Boolean,
        default: false
      }
    },
    computed: {
      computedType() {
        console.log(this.isShowPassword, 'props input')
        return this.isShowPassword ? 'text' : 'password'
      }
    }
  }
</script>




<script>
export default {
  name: 'MyUsernameInput',
  props: ["value", "type", "togglePassword", "placeholder", "Attributes"],
};
</script>


<template>
  <input 
  class="border background-gray-100 border-black p-2 rounded-sm"
   :placeholder="placeholder" type="type" togglePassword="value" id="myInput"/>
</template>


<script>
function myFunction() {
  var x = document.getElementById("myInput");
  if (x.type === "password") {
    x.type = "text";
  } else {
    x.type = "password";
  }
}
</script>

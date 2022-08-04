<template>
  <div id="app">
    <h1>Button</h1>
    <br />

    <div>
      <!-- size -->
      <MyButton
        class="
          h-8
          px-4
          m-2
          text-sm text-indigo-100
          transition-colors
          duration-150
          bg-indigo-700
          rounded-lg
          focus:shadow-outline
          hover:bg-indigo-800
        "
        param="Small"
      />
      <MyButton
        class="
          h-12
          px-6
          m-2
          text-lg text-indigo-100
          transition-colors
          duration-150
          bg-indigo-700
          rounded-lg
          focus:shadow-outline
          hover:bg-indigo-800
        "
        param="Large"
      />
      <MyButton
        class="
          h-16
          px-8
          m-2
          text-2xl text-indigo-100
          transition-colors
          duration-150
          bg-indigo-700
          rounded-lg
          focus:shadow-outline
          hover:bg-indigo-800
        "
        param="Extra Large"
      />
    </div>
    <br />
    <div>
      <!-- warna -->
      <MyButton
        class="
          h-8
          px-4
          m-2
          text-sm
          transition-colors
          duration-150
          rounded-lg
          focus:shadow-outline
        "
        param="Default"
      />

      <MyButton
        class="
          h-8
          px-4
          m-2
          text-sm
          bg-yellow-300
          transition-colors
          duration-150
          rounded-lg
          focus:shadow-outline
        "
        param="Yellow"
      />

      <MyButton
        class="
          h-8
          px-4
          m-2
          text-sm
          bg-green-300
          transition-colors
          duration-150
          rounded-lg
          focus:shadow-outline
        "
        param="Green"
      />

      <MyButton
        class="
          h-8
          px-4
          m-2
          text-sm
          bg-red-300
          transition-colors
          duration-150
          rounded-lg
          focus:shadow-outline
        "
        param="Red"
      />

      <MyButton
        class="
          h-8
          px-4
          m-2
          text-sm
          bg-gray-300
          transition-colors
          duration-150
          rounded-lg
          focus:shadow-outline
        "
        param="Gray"
      />
    </div>
    <br />
    <div>
      <!-- disabled button -->
      <DisButton param="Disabled Button" />
    </div>
    <br />
    <div>
      <!-- input -->
      <MyUsernameInput /><br>
      <MyPasswordInput :isShowPassword="isShow"/><br>
      <MyShowPassword @customFunction="myFunction"/> Show Password
    </div>
  </div>
</template>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<script>
import MyButton from "./components/Button/MyButton.vue";
import DisButton from "./components/Button/DisabledButton.vue";
import MyUsernameInput from "./components/Input/MyUsernameInput.vue";
import MyPasswordInput from "./components/Input/MyPasswordInput.vue";
import MyShowPassword from './components/Input/MyShowPassword.vue';

export default {
  name: 'App',
  components: {
    MyButton,
    DisButton,
    MyUsernameInput,
    MyPasswordInput,
    MyShowPassword,
  },
  data: () => {
    return {
      isShow: false
    }
  },
  watch: {
    isShow(value) {
      console.log(value, 'val')
    }
  },
  methods: {
    myFunction() {
      console.log('action parent ok')
      if (this.isShow) {
        this.isShow = false
      } else {
        this.isShow = true
      }
    }
  }
}
</script>
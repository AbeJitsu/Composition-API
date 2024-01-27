<template>
  <section class="container">
    <h2>{{ user.name }}</h2>

    <h3>{{ user.age }}</h3>
  </section>
</template>

<script>
import { reactive } from 'vue';

export default {
  setup() {
    // const uName = ref ( 'Abe');
    // const uAge = ref ( 46 );
    const user = reactive({
      name: 'Abe',
      age: 46,
    });

    
    setTimeout(function () {
      // uName.value = 'Abiezer',
      // uAge.value = 47
      (user.name = 'Abiezer'),
       (user.age = 46);
    }, 2000);

    return {
      
      user: user,
    };
  },
  // data() {
  //   return {
  //     userName: 'Maximilian',
  //   };
  // },
};
</script>

<style>
* {
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
}

body {
  margin: 0;
}

.container {
  margin: 3rem auto;
  max-width: 30rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  padding: 1rem;
  text-align: center;
}
</style>

<script>
export default {
  data() {
    return {
      conunterIncrease: 1,
      counter: 1,
    };
  },
  methods: {
    increaseCounter() {
      this.counter += parseInt(this.conunterIncrease);
    },
  },
};
</script>

<template>
  <main>
    <h1>
      {{ counter }}
    </h1>
    <div class="from_group">
      <input v-model="conunterIncrease" type="number" />
      <button @click="increaseCounter">Zwiększ o podaną wartość</button>
    </div>
  </main>
</template>

<style>
* {
  padding: 0;
  margin: 0;
  color: white;
  font-family: 'Tahoma' sans-serif;
}
h1 {
  font-size: 10rem;
}
main {
  background: #1e1e1e;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 4rem;
  height: 100vh;
}
.from_group {
  display: flex;
  gap: 1rem;
}
button,
input {
  padding: 1rem;
  border: 2px solid lime;
  background: transparent;
  border-radius: 10px;
  font-size: 24px;
  font-weight: 700;
}
input {
  color: white;
}
button {
  background: lime;
  color: #1e1e1e;
  cursor: pointer;
}
</style>

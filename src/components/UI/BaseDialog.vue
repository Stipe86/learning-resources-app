<template>
  <dialog open>
    <header>
      <slot name="header">
        <h2>{{ title }}</h2>
      </slot>
    </header>
    <section>
      <slot></slot>
    </section>
    <menu>
      <slot name="actions"></slot>
    </menu>
  </dialog>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: false,
    },
  },
};
</script>

<style scoped>
/* dialog {
  margin: 0;
  position: fixed;
  top: 20vh;
  left: 30%;
  width: 40%;
  background-color: white;
  box-shadow: 0 2px 8 px rgba(0, 0, 0, 0.26);
  padding: 1rem;
} */

dialog {
  position: fixed;
  top: 20vh;
  left: 10%;
  width: 80%;
  z-index: 100;
  border-radius: 12px;
  border: none;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  padding: 0;
  margin: 0;
  overflow: hidden;
}

header {
  background-color: #3a0061;
  color: white;
  width: 100%;
  padding: 1rem;
}

header h2 {
  margin: 0;
}

section {
  padding: 1rem;
}

menu {
  padding: 1rem;
  display: flex;
  justify-content: flex-end;
  margin: 0;
}

@media (min-width: 768px) {
  dialog {
    left: calc(50% - 20rem);
    width: 40rem;
  }
}
</style>

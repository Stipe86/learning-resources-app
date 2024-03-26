<template>
  <base-card>
    <form action="" @submit.prevent="addResource">
      <div class="form-control">
        <label for="title">Title</label>
        <input type="text" id="title" name="title" v-model="titleInput" />
      </div>

      <div class="form-control">
        <label for="description">Description</label>
        <textarea
          name="description"
          id="description"
          rows="3"
          v-model="descInput"
        ></textarea>
      </div>

      <div class="form-control">
        <label for="link">Link</label>
        <input type="url" id="link" name="link" v-model="linkInput" />
      </div>

      <div class="form-control">
        <base-button type="submit">Add Resource</base-button>
      </div>
    </form>
  </base-card>
</template>

<script>
export default {
  data() {
    return {
      titleInput: "",
      descInput: "",
      linkInput: "",
    };
  },

  methods: {
    addResource() {
      const resource = {
        id: Date.now().toString(),
        title: this.titleInput,
        description: this.descInput,
        link: this.linkInput,
      };
      this.$emit("add-resource", resource);
      this.titleInput = "";
      this.descInput = "";
      this.linkInput = "";
    },
  },
};
</script>

<style scoped>
label {
  font-weight: bold;
  display: block;
  margin-bottom: 0.5rem;
}

input,
textarea {
  display: block;
  width: 100%;
  font: inherit;
  padding: 0.15rem;
  border: 1px solid #ccc;
}

input:focus,
textarea:focus {
  outline: none;
  border-color: #3a0061;
  background-color: #f7ebff;
}

.form-control {
  margin: 1rem 0;
}
</style>

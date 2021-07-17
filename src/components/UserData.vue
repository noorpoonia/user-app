<template>
  <section>
    <form @submit.prevent="submitData">
      <input type="text" placeholder="Your name" v-model="enteredName" />
      &nbsp;
      <input type="text" placeholder="Your age" v-model="enteredAge" />
      <br>
      <br>
      <button>Set User Data</button>
    </form>
  </section>
</template>

<script>
export default {
  emits: ['set-data'],
  data() {
    return {
      enteredName: "",
      enteredAge: "",
    };
  },
  methods: {
    submitData() {
      this.$emit('set-data', this.enteredName, this.enteredAge);
    },
  }
};
</script>
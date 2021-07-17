// ActiveUser should output a username (h2) and age (h3)

<template>
  <li>
    <h2>{{ username }}</h2>
    <h3>{{ userage }} Years</h3>
  </li>
</template>

<script>
export default {
  props: {
    username: {
      type: String,
      required: true,
    },
    userage: {
      type: Number,
      required: true,
    },
  },
};
</script>

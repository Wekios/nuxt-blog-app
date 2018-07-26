<template>
  <h1>
    this is user, with id: {{ $route.params.id }}
  </h1>
</template>

<script>
export default {
  validate(data) {
    return /^\d+$/.test(data.params.id);
  },
  layout: "users"
};
</script>


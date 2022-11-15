<template>
  <div>{{ value }}</div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      value: "World"
    };
  },
  async mounted() {
    const { text } = await (await fetch("/api/message")).json();
    this.value = text;
  }
};
</script>

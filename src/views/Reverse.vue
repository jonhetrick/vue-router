<template>
  <div class="reverse">
    <h1>This is the Reverese Page</h1>
    <h2>Please Enter a string to reverse!</h2>
    <label>
      String:
      <!-- v-model is working on the input event, v-model.lazy is working on the change. -->
      <input type="text" id="string" v-model.lazy="message" />
    </label>
    <h2>The reverse message is:</h2>
    <p>{{ reversedMessage }}</p>
  </div>
</template>

<script>
export default {
  name: "Reverse",
  data() {
    return {
      message: ""
    };
  },
  computed: {
    reversedMessage() {
      return this.message
        .split("")
        .reverse()
        .join("");
    }
  }
};
</script>


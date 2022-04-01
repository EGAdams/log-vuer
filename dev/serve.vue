<script lang="ts">
import { defineComponent } from "vue";
import LogVuer from "../src/LogViewer.vue";

export default defineComponent({
  name: "ServeDev",
  components: {
    LogVuer,
  },
  data() {
    return {
      test_object_name: "log-vuer-tester",
      logs: [
        {
          id: "1",
          timestamp: 100,
          message: "test message 1",
          method: "test",
        },
        {
          id: "2",
          timestamp: 100,
          message: "test message 2",
          method: "test",
        },
      ],
    };
  },
});
</script>

<template>
  <div id="app">
    <log-vuer v-bind:object_name="test_object_name" v-bind:logs="logs"></log-vuer>
  </div>
</template>

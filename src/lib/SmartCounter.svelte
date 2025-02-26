<script lang="ts">
  let count = $state(0);
  let { step = 1 } = $props();
</script>

<button onclick={() => count++}>
  clicks: {count * step}
</button>

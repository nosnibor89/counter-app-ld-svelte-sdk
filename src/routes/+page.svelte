<script lang="ts">
  import { LDProvider, LDFlag } from "@nosnibor89/svelte-client-sdk";
  import { env } from "$env/dynamic/public";
  import SimpleCounter from "$lib/SimpleCounter.svelte";
  import SmartCounter from "$lib/SmartCounter.svelte";

  const context = {
    kind: "user",
    key: "example-guest-user",
    name: "Guest",
  };
</script>

<main>
  <LDProvider clientID={env.PUBLIC_CLIENT_ID ?? 'YOUR_DEFAULT_CLIENT_ID'} {context}>
    <LDFlag flag={'show-smart-counter'}>
      {#snippet off()}
        <SimpleCounter />
      {/snippet}
      {#snippet on()}
        <!-- Will increment by 5 -->
        <SmartCounter step={5} />
      {/snippet}
    </LDFlag>
  </LDProvider>
</main>

<style>
    main {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
    }
</style>

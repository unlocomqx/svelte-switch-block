<script>
  import { getContext } from "svelte"

  const matched = getContext("svelte-switch-block-matched")
</script>

{#if !$matched}
  <slot></slot>
{/if}

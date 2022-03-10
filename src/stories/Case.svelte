<script>
  import { getContext } from "svelte"

  export let value

  const expression = getContext("svelte-switch-block-expression")
  const matched = getContext("svelte-switch-block-matched")

  if (expression === value) {
    matched.set(true)
  }
</script>

{#if value === expression}
  <slot></slot>
{/if}

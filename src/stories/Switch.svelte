<script>
  import { setContext } from "svelte"
  import { writable } from "svelte/store"

  export let expression

  setContext("svelte-switch-block-expression", expression)
  setContext("svelte-switch-block-matched", writable(false))
</script>

<slot></slot>

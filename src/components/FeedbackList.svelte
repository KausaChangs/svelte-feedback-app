<script>
  export let feedBack = []
</script>


{#each feedBack as fb (fb.id)}
  {fb.text}
{/each}

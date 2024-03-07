<script>
    export let comments = [];
  </script>
  
  {#if comments.length > 0}
    <ul>
      {#each comments as { author, content }}
        <li><strong>{author}</strong>: {content}</li>
      {/each}
    </ul>
  {:else}
    <p>No hay comentarios aún.</p>
  {/if}
  
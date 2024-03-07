<script>
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher();
  
    let author = '';
    let content = '';
  
    function submitComment() {
      dispatch('addComment', { author, content });
      author = '';
      content = '';
    }
  </script>
  
  <form on:submit|preventDefault={submitComment}>
    <input placeholder="Tu nombre" bind:value={author} />
    <textarea placeholder="Tu comentario" bind:value={content}></textarea>
    <button type="submit">Enviar</button>
  </form>
  
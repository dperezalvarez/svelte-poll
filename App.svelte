svelte
<script>
  import CommentForm from './CommentForm.svelte';
  import CommentList from './CommentList.svelte';

  let comments = [];
  
  function addComment(comment) {
    comments = [...comments, comment];
  }
</script>

<main>
  <h1>Deja tu comentario</h1>
  <CommentForm on:addComment={addComment} />
  <CommentList {comments} />
</main>

<script>
    export let texto = "Test text"
    export let content
</script>
<div class="dropdown">
    <button type="button" class="btn dropdown-toggle" data-bs-toggle="dropdown">
      {texto}
    </button>
    <ul class="dropdown-menu">
      {content}
    </ul>
</div>
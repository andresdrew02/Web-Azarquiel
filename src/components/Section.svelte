<script>
  import FaAngleRight from "svelte-icons/fa/FaAngleRight.svelte";
  import FaChevronDown from 'svelte-icons/fa/FaChevronDown.svelte'
  export let nombre = "Default name";
  export let bottomArrow = false;

  const redirectHandler = () => {
    if (nombre === 'INICIO'){
      window.location.href = `${window.location.origin}`
    }
  }

</script>

<div class="principal" on:click={redirectHandler} on:keydown={null}>
  <div class="sec">
    <span><FaAngleRight /></span>
    <p>{nombre}</p>
  </div>
  {#if bottomArrow}
    <div class="sec">
      <span><FaChevronDown /></span>
    </div>
  {/if}
</div>

<style>
  .principal {
    color: white;
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    cursor:pointer;
  }
  .sec {
    display: flex;
  }
  span {
    width: 15px;
    height: 15px;
  }
</style>

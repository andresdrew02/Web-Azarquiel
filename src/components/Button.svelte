<script>
  import FaDownload from "svelte-icons/fa/FaDownload.svelte";
  export let nombre = "Default Button";
</script>

<button>
  <span>
    <svg>
      <FaDownload />
    </svg>
    {nombre}
  </span>
</button>

<style>
  svg {
    width: 20px;
    height: 20px;
    margin-right:1rem;
  }
  button {
    border: 2px solid #0071e2;
    background-color: transparent;
    transition: all ease-in-out 0.2s;
    padding: .8rem 1rem 1rem .8rem;
    font-size: 16px;
  }

  button span {
    display: flex;
    justify-content: center;
    align-items: center;
    color: rgb(38, 38, 38);
    font-size:1.2rem;
  }

  button:hover {
    background-color: #0071e2;
  }
  button:hover span{
    color: white;
  }
</style>

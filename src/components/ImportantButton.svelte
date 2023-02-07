<script>
  export let nombre = "Default button";
  export let url = "#"
  import TiInfoLargeOutline from "svelte-icons/ti/TiInfoLargeOutline.svelte";

    const redirectHandler = () => {
      window.location.href = `${window.location.origin}/${url}`
    }

</script>

<button on:click={redirectHandler}>
  <div class="svg-wrapper-1">
    <div class="svg-wrapper">
      <svg>
        <TiInfoLargeOutline />
      </svg>
    </div>
  </div>
  <span>{nombre}</span>
</button>

<style>
  
  svg{
    width: 30px;
    height: 30px;
  }

  button {
    font-family: inherit;
    font-size: 20px;
    background: royalblue;
    color: white;
    padding: 0.7em 1em;
    padding-left: 0.9em;
    display: flex;
    align-items: center;
    border: none;
    border-radius: 16px;
    overflow: hidden;
    transition: all 0.2s;
  }

  button span {
    display: block;
    margin-left: 0.3em;
    transition: all 0.3s ease-in-out;
  }

  button svg {
    display: block;
    transform-origin: center center;
    transition: transform 0.3s ease-in-out;
  }

  button:hover .svg-wrapper {
    animation: fly-1 0.6s ease-in-out infinite alternate;
  }

  @media (min-width:992px){
    button:hover svg {
      transform:translateX(4em);
    }
  }


  @media (max-width:992px){
    button:hover svg {
      transform:translateX(10em) !important;
    }
  }

  @media (max-width:360px){
    button:hover svg {
      transform:translateX(5em);
    }
  }

  @media (max-width:360px){
    button:hover svg {
      transform:translateX(4.5em) !important;
    }
  }

  button:hover span {
    transform: translateX(30em);
  }

  button:active {
    transform: scale(0.95);
  }

  @keyframes fly-1 {
    from {
      transform: translate(Y0.1em);
    }

    to {
      transform: translateY(-0.1em);
    }
  }
</style>

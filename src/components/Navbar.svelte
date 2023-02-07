<script lang="ts">
  import Header from "./Header.svelte";
  import GiHamburgerMenu from "svelte-icons/gi/GiHamburgerMenu.svelte";
  import IoMdClose from "svelte-icons/io/IoMdClose.svelte";
  import CustomInput from "./CustomInput.svelte";
  import OffNavSeparator from "./OffNavSeparator.svelte";
  import Section from "./Section.svelte";
  const sections = [
    {
      section: "inicio",
      arrow: false,
    },
    {
      section: "al día",
      arrow: true,
    },
    {
      section: "el loro",
      arrow: false,
    },
    {
      section: "el centro",
      arrow: true,
    },
    {
      section: "secretaría",
      arrow: true,
    },
    {
      section: "familias",
      arrow: true,
    },
    {
      section: "bolsa",
      arrow: false,
    },
  ];
</script>

<Header />
<div class="navbar sticky-top bg-light">
  <div class="logo">
    <a href="/" class="imgref"><img src="/images/logo.png" alt="" /></a>
  </div>
  <div class="desktop-menu d-none d-xl-flex">
    <a href="/">inicio</a>
    <div class="dropdown">
      <button
        type="button"
        class="btn dropdown-toggle"
        data-bs-toggle="dropdown"
      >
        Al dia
      </button>
      <div class="dropdown-menu animate slideIn">
        <div class="d-flex gap-5 p-4 justify-content-evenly">
          <div class="container col-4 mr-10">
            <h1 class="fs-5 fw-bold">Search</h1>
            <input type="text" class="form-control" />
          </div>
          <div class="fkbs">
            <a href=""><h1 class="fs-5 fw-bold">Al dia</h1></a>
            <a href="">Avisos del centro</a>
            <a href="">Blog y convocatoria</a>
          </div>
        </div>
      </div>
    </div>
    <a href="#">El loro</a>
    <div class="dropdown">
      <button
        type="button"
        class="btn dropdown-toggle"
        data-bs-toggle="dropdown"
      >
        El centro
      </button>
      <ul class="dropdown-menu animate slideIn">Contenido</ul>
    </div>
    <div class="dropdown">
      <button
        type="button"
        class="btn dropdown-toggle"
        data-bs-toggle="dropdown"
      >
        Secretaria
      </button>
      <ul class="dropdown-menu animate slideIn">Contenido</ul>
    </div>
    <div class="dropdown">
      <button
        type="button"
        class="btn dropdown-toggle"
        data-bs-toggle="dropdown"
      >
        familias
      </button>
      <ul class="dropdown-menu animate slideIn">Contenido</ul>
    </div>
    <a href="#">Bolsa</a>
  </div>
  <div class="ham">
    <button
      class="btn bg-light mt-4"
      type="button"
      data-bs-toggle="offcanvas"
      data-bs-target="#offcanvasRight"
      aria-controls="offcanvasRight"
    >
      <GiHamburgerMenu />
    </button>
  </div>
  <!--
    <div class="ham d-flex d-lg-none">
    <button class="btn" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasRight" aria-controls="offcanvasRight">
      <GiHamburgerMenu/>
    </button>
  </div>
-->
  <div
    class="offcanvas offcanvas-end"
    tabindex="-1"
    id="offcanvasRight"
    aria-labelledby="offcanvasRightLabel"
  >
    <div class="offcanvas-header bg-dark text-white">
      <h5 id="offcanvasRightLabel">Search</h5>
      <button
        type="button"
        class="bg-dark text-white close-btn"
        data-bs-dismiss="offcanvas"
      >
        <IoMdClose />
      </button>
    </div>
    <!--OFFCANVAS NAV-->
    <div class="offcanvas-body bg-dark">
      <div class="offcanvas-nav p-4">
        <CustomInput nombre="Search" />
        <OffNavSeparator />
        <div class="mt-4 d-flex flex-column gap-4">
          {#each sections as section}
            <Section
              nombre={section.section.toUpperCase()}
              bottomArrow={section.arrow}
            />
          {/each}
        </div>
      </div>
    </div>
  </div>
</div>

<style>
  .navbar {
    height: 5rem;
    padding: 1rem;
    gap: 1.25rem;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 6px -1px, rgba(0, 0, 0, 0.06) 0px 2px 4px -1px;
  }
  .offcanvas-nav {
    display: flex;
    flex-direction: column;
  }
  .dropdown-menu {
    min-width: 40rem !important;
    transform: translateX(-20rem) !important;
  }
  a:any-link:not(.imgref):hover , .dropdown-toggle:hover{
    background-color: #22b8f0;
    color: white;
    transition: all 0.5s;
  }
  .form-control {
    z-index: 999;
  }
  a:any-link {
    width: 6rem;
    padding-left: 1rem;
    padding-right: 1rem;
  }
  .close-btn {
    width: 25px;
    height: 25px;
    border: none;
  }
  @media (min-width: 768px) {
    .animate {
      animation-duration: 0.3s;
      -webkit-animation-duration: 0.3s;
      animation-fill-mode: both;
      -webkit-animation-fill-mode: both;
    }
  }
  @media (max-width: 990px) {
    .navbar {
      justify-content: space-between;
    }
  }

  @keyframes slideIn {
    0% {
      transform: translateY(0rem);
      opacity: 0;
    }

    100% {
      transform: translateY(1rem);
      opacity: 1;
    }

    0% {
      transform: translateY(0rem);
      opacity: 0;
    }
  }

  @-webkit-keyframes slideIn {
    0% {
      -webkit-transform: transform;
      -webkit-opacity: 0;
    }

    100% {
      -webkit-transform: translateY(0);
      -webkit-opacity: 1;
    }

    0% {
      -webkit-transform: translateY(1rem);
      -webkit-opacity: 0;
    }
  }

  .slideIn {
    -webkit-animation-name: slideIn;
    animation-name: slideIn;
  }
  .desktop-menu {
    gap: 2rem;
    text-transform: uppercase;
    transform: translateY(0.5rem);
  }
  a:any-link {
    text-decoration: none;
    font-size: 0.85rem;
    color: black;
  }
  .logo img {
    width: 15rem;
  }
  .ham {
    width: 1.5rem;
    transform: translateY(-0.2rem);
    cursor: pointer;
  }
  button {
    text-transform: uppercase;
    font-size: 0.85rem;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .fkbs {
    display: flex;
    flex-direction: column;
    width: 40%;
  }
  .fkbs a:any-link {
    width: 100%;
    font-size: 1rem;
  }
</style>

<script>
  import Saos from "saos";
</script>

<div
  class="container-fluid col-12 p-4 d-flex bg-primary text-white flex-column flex-md-row"
>
  <div class="col-12 col-md-5">
    <Saos animation={"slide-in-right .6s cubic-bezier(0.23, 1, 0.32, 1) both"}>
      <h1 class="fs-3 text-decoration-underline">
        ¿Para qué sirve en el mundo laboral?
      </h1>
      <p>
        Este profesional ejercerá su actividad en entidades de los sectores
        donde sea necesario establecer mecanismos y medidas para la protección
        de los sistemas de información y redes de comunicaciones.
      </p>
    </Saos>
  </div>
  <div
    class="col-2 d-none d-md-flex flex-column justify-content-center align-items-center"
  >
    <img
      class="arrow"
      src="/images/arrow-right.svg"
      alt="arrow to the right icon"
    />
    <p class="m-0 text-center">Puestos laborales</p>
  </div>
  <div class="col-12 col-md-5">
    <Saos animation={"slide-in-right 1.6s cubic-bezier(0.23, 1, 0.32, 1) both"}>
      <h1 class="fs-3 text-decoration-underline d-block d-none-md">
        Puestos de trabajo
      </h1>
      <ol>
        <li>Experto en ciberseguridad</li>
        <li>Auditor de ciberseguridad</li>
        <li>Consultor de ciberseguridad</li>
        <li>Hacker ético</li>
      </ol>
    </Saos>
  </div>
</div>

<style>
  .arrow {
    width: 75px;
  }
  ol li {
    list-style: lower-latin;
  }
  /* ----------------------------------------------
 * Generated by Animista on 2023-2-10 17:21:43
 * Licensed under FreeBSD License.
 * See http://animista.net/license for more info. 
 * w: http://animista.net, t: @cssanimista
 * ---------------------------------------------- */

  /**
 * ----------------------------------------
 * animation slide-in-right
 * ----------------------------------------
 */
  @-webkit-keyframes -global-slide-in-right {
    0% {
      -webkit-transform: translateX(1000px);
      transform: translateX(1000px);
      opacity: 0;
    }
    100% {
      -webkit-transform: translateX(0);
      transform: translateX(0);
      opacity: 1;
    }
  }
  @keyframes -global-slide-in-right {
    0% {
      -webkit-transform: translateX(1000px);
      transform: translateX(1000px);
      opacity: 0;
    }
    100% {
      -webkit-transform: translateX(0);
      transform: translateX(0);
      opacity: 1;
    }
  }
</style>

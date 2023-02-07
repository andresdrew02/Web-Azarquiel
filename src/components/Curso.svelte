<script>
    import Button from "./Button.svelte";
    import ImportantButton from "./ImportantButton.svelte";

    export let nombre = "Default name"
    export let url = "#"
    export let imageUrl = "https://images.unsplash.com/photo-1542751371-adc38448a05e?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80"
</script>

<div class="card">
    <div class="image">
        <img src={imageUrl} alt="Card">
    </div>
    <div class="card-content">
        <h1 class="fs-3">{nombre}</h1>
        <div class="card-buttons d-flex flex-column flex-lg-row">
            <ImportantButton nombre='Mas información' url={url}/>
            <Button nombre="Descargar folleto"/>
        </div>
    </div>
</div>

<style>
    .card{
        width:clamp(300px,100%,550px);
        height:100%;
    }
    img{
        width: 100%;
        height: 300px;
        border-radius: .25rem .25rem 0rem 0rem;
        object-fit: cover;
    }
    .card-content{
        display: flex;
        flex-direction: column;
        width: 100%;
        padding: 2rem;
        gap:1rem;
    }
    .card-buttons{
        display: flex;
        gap:1rem;
    }
</style>
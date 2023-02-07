<script>
    import FaFacebookF from 'svelte-icons/fa/FaFacebookF.svelte'
    import FaTwitter from 'svelte-icons/fa/FaTwitter.svelte'
    import FaYoutube from 'svelte-icons/fa/FaYoutube.svelte'
    import FaInstagram from 'svelte-icons/fa/FaInstagram.svelte'
    import FaFlickr from 'svelte-icons/fa/FaFlickr.svelte'
    import IoMdMail from 'svelte-icons/io/IoMdMail.svelte'
    import FaPhoneAlt from 'svelte-icons/fa/FaPhoneAlt.svelte'
</script>

<header>
    <div class="icons">
        <div class="icon">
            <FaFacebookF/>
        </div>
        <div class="icon">
            <FaTwitter/>
        </div>
        <div class="icon">
            <FaYoutube/>
        </div>
        <div class="icon">
            <FaYoutube/>
        </div>
        <div class="icon">
            <FaFlickr/>
        </div>
        <div class="icon">
            <FaInstagram/>
        </div>
    </div>
    <div class="contact">
        <div class="contact-icon">
            <div class="icon">
                <FaPhoneAlt/>
            </div>
            <a href="#">
                925284043
            </a>
        </div>
        <div class="contact-icon">
            <div class="icon">
                <IoMdMail/>
            </div>
            <a href="#">
                45003875.ies@edu.jccm.es
            </a>
        </div>
    </div>
</header>

<style>
    header{
        width: 100%;
        padding:.5rem;
        display: flex;
        font-weight: 300;
        justify-content: space-around;
        gap:15rem;
        align-items: center;
        background-color: rgb(233, 233, 233);
        z-index: 999;
    }
    .contact{
        display: flex;
        gap:0.5rem;
    }
    .contact-icon{
        display: flex;
        align-items: flex-start;
        gap:0.1rem;
    }
    a:any-link{
       font-size: .8rem;
       text-decoration: none;
       cursor: pointer;
       color:rgb(1, 123, 189);
    }
    .icons{
        display: flex;
        gap:0.5em;
    }
    .icon{
        width: 15px;
        height: 15px;
        color: gray;
        transform: translateY(-0.25rem);
    }
    @media screen and (max-width:575px){
        header{
            justify-content: flex-start;
            align-items: center;
            flex-direction: column;
            gap:.5rem;
        }
    }
</style>
<script>
    export let headerHeight;
</script>

<header bind:clientHeight={headerHeight}>
    <img src="/images/Logo.png" alt="" />
</header>

<style>
    header {
        background-image: url("/images/Header.png");
        background-size: cover;
        background-repeat: no-repeat;
        height: auto;
        width: 100%;
        text-align: center;
    }

    img {
        height: 150px;
        padding-top: 20px;
        /* padding-bottom: 20px; */
    }
</style>

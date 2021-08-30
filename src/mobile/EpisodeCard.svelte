<script>
    export let episode;
</script>

<div class="card">
    <div>
        <p>EP-{episode['number']} {episode['title']}</p>
    </div>
    <div class="links">
        <a href={episode['youtube']} target="_blank">
            <img
                src="/images/youtube.png"
                alt="Link to episode on YouTube"
                class="link-image"
            />
        </a>
        <a href={episode['spotify']} target="_blank">
            <img
                src="/images/spotify.png"
                alt="Link to episode on YouTube"
                class="link-image"
            />
        </a>
        <a href={episode['amazon']} target="_blank">
            <img
                src="/images/amazon.png"
                alt="Link to episode on YouTube"
                class="link-image"
            />
        </a>
    </div>
</div>

<style>
    .card {
        margin: 0px 12px 0px 12px;
        padding: 4px 6px 4px 6px;
        border: 1px solid white;
        border-radius: 6px;
        color: white;
        font-weight: 600;
        /* display: flex; */
        /* justify-content: space-between; */
    }

    .link-image {
        height: auto;
        max-width: 100%;
    }

    .links {
        display: flex;
        justify-content: space-evenly;
    }

    .links > a {
        margin: 2px;
    }
</style>

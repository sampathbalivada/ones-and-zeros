<script>
    export let episode;
</script>

<div class="card" style="margin-bottom: 12px">
    <div>
        <p>EP-{episode['number']} {episode['title']}</p>
    </div>
    <div>
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
        padding: 8px 12px 8px 12px;
        border: 2px solid white;
        border-radius: 6px;
        color: white;
        font-weight: 600;
        display: flex;
        justify-content: space-between;
    }

    .link-image {
        height: 50px;
    }
</style>

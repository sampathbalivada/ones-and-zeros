<script>
    import EpisodeCard from "./EpisodeCard.svelte";
    import _, {episodes} from "../Data.svelte"

    export let height;
</script>

<div style="--height-already-occupied: {height + 'px'}">
    {#each episodes as episode}
        <EpisodeCard {episode}/>
    {/each}
</div>

<style>
    div {
        overflow: auto;
        height: calc(100vh - var(--height-already-occupied) - 20px);
    }
</style>

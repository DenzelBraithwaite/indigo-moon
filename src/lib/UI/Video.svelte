<script>
    export let poster;
    export let src;
</script>

<style>
    video {
        display: block;
        width: 90%;
        margin: 5rem auto;
    }
</style>

<video
    controls
    {poster}
    {src}>
    <track kind="captions">
</video>
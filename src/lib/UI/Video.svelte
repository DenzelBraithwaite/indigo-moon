<script>
    export let poster;
    export let src;
    export let title;
</script>

<style>
    video {
        display: block;
        width: 90%;
        margin-top: 1rem;
        margin-bottom: 5rem;
        margin-left: auto;
        margin-right: auto;
        border-radius: 0.5rem;
    }

    .title {
        margin: 0 auto;
        text-align: center;
        margin-top: 5rem;
    }
</style>
<div class="container">
    <h1 class="title">{title}</h1>
    <video controls {poster} {src} {title}>
        <track kind="captions">
    </video>
</div>
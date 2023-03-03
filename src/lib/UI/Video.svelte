<script>
    export let poster;
    export let src;
    export let title;
</script>

<div class="container">
    <h1 class="title">{title}</h1>
    <video controls {poster} {src} {title}>
        <track kind="captions">
    </video>
</div>

<style>
    video {
        display: block;
        width: 80%;
        margin: 0 auto;
        border-radius: 0.5rem;
        box-shadow: 0 2px 10px #65466497; /* --secondary-purple, transparent */
    }

    .title {
        font-size: 2rem;
        margin: 0 auto;
        text-align: center;
        color: var(--secondary-purple);
    }
</style>
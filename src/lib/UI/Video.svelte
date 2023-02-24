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
        box-shadow: 0 2px 10px #65466497; /* --secondary-purple, transparent */
    }

    .title {
        font-size: 2rem;
        margin: 0 auto;
        text-align: center;
        margin-top: 5rem;
        color: var(--secondary-purple);
    }
</style>
<div class="container">
    <h1 class="title">{title}</h1>
    <video controls {poster} {src} {title}>
        <track kind="captions">
    </video>
</div>
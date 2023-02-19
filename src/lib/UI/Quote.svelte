<script>
    // JavaScript Below
export let text = '"Peace comes from within. Do not seek it without"';
export let author = "Buddha";
</script>

<style>
    /* CSS Below */
    section {
        background-color: #727557;
        height: 40vh;
        margin: 3rem 0;
        padding: 1rem;
    }
    
    .container {
        position: relative;
        width: 50%;
        margin: 0 auto;
        text-align: center;
        color: #fff;

        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .quote-icon {
        fill: #fff;
        scale: 0.5;
        transform: translate(3rem);
        line-height: 1;
    }

    .text {
        font-size: 1.25rem;
        font-weight: 400;
    }

    .author {
        font-size: 1rem;
        font-weight: 100;
    }
</style>

<!-- HTML Below -->
<section>
    <div class="container">
        <svg class="quote-icon">
            <path d="M89.9 51H51.6c-1.5 0-2.8 1.2-2.8 2.8v38.3c0 1.5 1.2 2.8 2.8 2.8h18.1c-.2 4.3-.9 9.1-3.2 15.2-2.3 5.9-11.1 13.1-16.3 16.2-.9.5-1.4 1.4-1.4 2.4v17.6c0 .9.5 1.8 1.3 2.3.5.3 1 .5 1.5.5.4 0 .8-.1 1.1-.2 9.1-4 16.7-9.4 22.6-15.9 5.8-6.5 10.2-13.8 13.1-21.6 2.9-7.8 4.3-19.1 4.3-33.7V53.8c0-1.5-1.2-2.8-2.8-2.8zm-2.8 26.6c0 13.9-1.3 24.6-4 31.8-2.6 7.1-6.7 13.8-12 19.8-4.5 5-10.1 9.3-16.7 12.7v-11.6c4.7-3 14.3-10.5 17.3-18.1 3.2-8.3 3.6-14.7 3.6-20 0-1.5-1.2-2.8-2.8-2.8H54.4V56.6h32.7v21z"></path>
            <path d="M148.4 51h-38.3c-1.5 0-2.8 1.2-2.8 2.8v38.3c0 1.5 1.2 2.8 2.8 2.8h18.1c-.2 4.3-.9 9.1-3.2 15.2-2.3 5.9-11.1 13.1-16.3 16.2-.9.5-1.4 1.4-1.4 2.4v17.6c0 .9.5 1.8 1.3 2.3.5.3 1 .5 1.5.5.4 0 .8-.1 1.1-.2 9.1-4 16.7-9.4 22.6-15.9 5.8-6.5 10.2-13.8 13.1-21.6 2.9-7.8 4.3-19.1 4.3-33.7V53.8c0-1.5-1.3-2.8-2.8-2.8zm-2.8 26.6c0 13.9-1.3 24.6-4 31.8-2.6 7.1-6.7 13.8-12 19.8-4.5 5-10.1 9.3-16.7 12.7v-11.6c4.7-3 14.3-10.5 17.3-18.1 3.2-8.3 3.6-14.7 3.6-20 0-1.5-1.2-2.8-2.8-2.8h-18.1V56.6h32.7v21z"></path>
        </svg>
        <h1 class="text">{text}</h1>
        <p class="author">{author}</p>
    </div>
</section>
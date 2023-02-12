<script>
    // JavaScript Below
export let text;
export let author;
</script>

<style>
    /* CSS Below */
    .card{
        position: relative;
        height: 350px;
        padding: 10px;
    }

    .quotes{
        position: relative;
        padding: 15px;
        height: 10%;
    }

    .text{
        position: relative;
        padding: 20px;
        height: 40%;
    }

    .author{
        position: relative;
        padding: 15px;
        height: 10%;
    }
</style>

<!-- HTML Below -->
<div class="card">
    <p class= "quotes"> 
        ''
    </p>
    
    <p class= "text"> 
        {text}
    </p>
    
    <p class= "author"> 
        {author}
    </p>
</div>

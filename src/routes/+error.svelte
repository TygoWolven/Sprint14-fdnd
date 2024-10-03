<script> 
    import { page } from '$app/stores';
</script>

<main>
    <h1>404 Error: Joke Not Found</h1>
    <p>Why do programmers prefer dark mode?</p>
    <p>Because the light attracts bugs!</p>
</main>

<style>
main {
    text-align: center;
    margin-top: 20vh;
    font-family: Arial, sans-serif;
}

h1 {
    color: #000000;
    font-size: 2em;
}

p:first-child   {
    color: #333;
    font-size: 1.2em;
}

p:last-child {
    color: #333;
    font-size: 1.2em;
    opacity: 0; 
    animation: fadeIn 4s forwards;
}

    @keyframes fadeIn {
        from {
            opacity: 0;
        }
        to {
            opacity: 1;
        }
    }

</style>
<script>
    import {goto, beforeNavigate, afterNavigate} from '$app/navigation';

    const handleClick = () =>{
        console.log('Placing your order');
        goto('/products');
    };

    beforeNavigate((navigation) => {
        console.log({ before: navigation});   
    });

    afterNavigate((navigation) => {
        console.log({ after: navigation});
    });

</script>

<h1>WELCOME HOME</h1>

<a href="/Blog">Blog</a>
<a href="/products">Products</a>

<button on:click={handleClick}>Place order</button>
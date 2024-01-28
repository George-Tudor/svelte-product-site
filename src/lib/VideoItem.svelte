<script>
    export let title;
    export let subtitle;
    export let cast;
    export let imageUrl;
    export let description;

</script>

<style>
    article {
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
        border-radius: 5px;
        background: #f9fbfc;
        margin: 1rem;
    }

    header,
    .content,
    footer {
        padding: 1rem;
        color: #1a1a1a;
    }

    .image {
        width: 100%;
        height: 28rem;
    }

    .image img {
        display: block;
        margin-left: auto;
        margin-right: auto;
        width: 65%;
    }

    h1 {
        font-size: 1.5rem;
        margin: 0.5rem 0;
        font-family: "Roboto Slab", sans-serif;
        color: #1a1a1a;
    }


    h2 {
        font-size: 1rem;
        color: #808080;
        margin: 0.5rem 0;
    }

    h3 {
        font-size: 1rem;
        margin: 0.5rem 0;
        font-family: "Roboto Slab", sans-serif;
        color: #1a1a1a;
    }

    p {
        font-size: 1.25rem;
        margin: 0;
    }

    div {
        text-align: right;
    }
</style>

<article>
    <header>
        <h1>{title}</h1>
        <h2>{subtitle}</h2>
        <h3>{cast}</h3>
    </header>
    <div class ="image">
        <img src={imageUrl} alt={title}>
    </div>
    <div class="content">
        <p>{description}</p>
    </div>
    <footer>
        <button>Add to Cart</button>
        <button>Show Details</button>
    </footer>
</article>

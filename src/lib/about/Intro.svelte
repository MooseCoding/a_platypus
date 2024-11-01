<script>
    import About from '$lib/pages/about_page.json'; 

    let name = About.About.Intro.Name;
    let imageSrc = `../../.././${About.About.Intro.SelfieName}`; // Update with the actual path to your image
</script>
  
<style>
    .intro {
        display: flex;
        align-items: center;
        padding: 1rem;
        border-radius: 8px;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    }

    .intro img {
        border-radius: 50%;
        width: 100px;
        height: 100px;
        margin-right: 1rem;
    }

    .intro h2 {
        margin: 0;
        font-size: 1.5rem;
    }

    .intro p {
        margin: 0.5rem 0 0;
        color: #666;
    }
</style>

<div class="intro" style="background-color: {About.About.Intro.BackgroundColor};">
    <img src={imageSrc} alt="{name}'s picture" />
    <div>
        <h2>{name}</h2>
        <p>{About.About.Intro.Description}</p>
    </div>
</div>
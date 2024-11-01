<script>
    import About from '$lib/pages/about_page.json';
</script>

<div class="p-8 text-center" style="background-color: {About.About.ExtraContent.BackgroundColor}; color: {About.About.ExtraContent.TextColor}">
    {#each About.About.ExtraContent.Paragraphs as par}
      <p class="mb-6 py-10">{par}</p>
    {/each}
</div>
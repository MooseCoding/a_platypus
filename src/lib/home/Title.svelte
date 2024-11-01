<script>
    import page from '$lib/pages/main_page.json'; 
  
    let src = `../../.././${page.Content.BackgroundFileName}`;
  </script>
  
<div class="relative h-screen w-full">
  <div class="absolute inset-0 bg-cover bg-center" style="background-image: url({src});"></div>

  <div class="absolute inset-0 bg-gradient-to-b from-transparent to-[{page.Content.BackgroundColor}]"></div>

    <div class="relative z-10 flex flex-col items-center justify-center h-screen text-center" style="color: {page.Content.TitleColor};">
      <h1 class="text-6xl font-bold">{page.Content.PageTitle}</h1>
    </div>
  </div>
  
  <div class="p-8 text-center" style="background-color: {page.Content.BackgroundColor}; color: {page.Content.ParagraphColor}">
    {#each page.Content.Paragraphs as par}
      <p class="mb-6 py-10">{par}</p>
    {/each}
  </div>
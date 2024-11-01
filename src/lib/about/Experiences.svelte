<script>
    import About from '$lib/pages/about_page.json';
</script>
  
  <style>
    .experience-card {
      border-radius: 8px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
      padding: 1.5rem;
      margin: 1rem 0;
      transition: box-shadow 0.3s;
    }
  
    .experience-card:hover {
      box-shadow: 0 4px 16px rgba(0, 0, 0, 0.2);
    }
  
    .experience-card h3 {
      margin: 0;
      font-size: 1.5rem;
    }
  
    .experience-card h4 {
      margin: 0.5rem 0;
      font-size: 1.2rem;
    }
  
    .experience-card p {
      margin: 0.5rem 0 0;
    }
  
    .duration {
      font-style: italic;
    }
</style>
  
{#each About.About.Experience.Jobs as job}
    <div class="experience-card" style="color: {job.TextColor}; background-color:{job.BackgroundColor}">
        <h3 class="font-bold">{job.Title}</h3>
        <h4 class="font-semibold">{job.Company}</h4>
        <p class="duration">{job.Duration}</p>
        <p class="text-center">{job.Description}</p>
    </div>
{/each}
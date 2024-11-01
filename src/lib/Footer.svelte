<script>
    import Footer from '$lib/pages/footer.json';
</script>

<footer style="background-color: {Footer.FooterBackgroundColor}; color: {Footer.FooterTextColor};">
    {Footer.Footer}
</footer>

<style>
    footer { /* Light background */
      text-align: center;
      padding: 1em;
      position: relative;
      bottom: 0;
      width: 100%;
    }
</style>
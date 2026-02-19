<script context="module">
      export const prerender = true;
</script>

<script>
	import Navigation from '$lib/components/Navigation.svelte';
    import Footer from '/src/lib/components/Footer.svelte'
    import Nav from '/src/lib/components/Navigation.svelte'
    import Hero from '$lib/components/Hero.svelte';
</script>

<!-- NAV -->
<div class="flex flex-col justify-start min-h-screen w-full bricolage-grotesque-600">
    <section>
        <Navigation />
    </section>
    
    <!-- HERO -->
    <Hero src="/images/customHero.png" alt="this is a hero"/>
    <!-- Netlify detection form (hidden) -->
    <form name="contact" method="POST" data-netlify="true" hidden>
        <input type="hidden" name="form-name" value="contact" />
        <input type="text" name="name" />
        <input type="email" name="email" />
        <input type="tel" name="phone" />
    </form>

    <!-- Services 3 icons / description -->
    
    <!-- Contact -->
    
    <!-- About us  -->
    
    <!-- Why choose us -->
    
    <!-- Testimonial -->
    
    <!-- Gallery -->
    
    <!-- Footer -->
    
     <Footer />
</div>

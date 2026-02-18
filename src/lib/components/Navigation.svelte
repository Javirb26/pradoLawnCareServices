<script>
    let active = $state(false);
    let { 
        logo,
        pages = ['Home', 'About', 'Pricing', 'Services', 'Contact'],
        services = ['Landscaping', 'Tree trimming', 'mulching', 'property clean ups']
     } = $props();

     let disappear = () => {
        if (active = false){

        }
     }
</script>

<nav class="flex justify-between w-full mx-auto bg-white">

    <div class="max-w-40">
        <img src="/images/pradoLogo.svg" alt="Prado Logo">
    </div>

    <ul class="flex px-4">
        {#each pages as page}
            {#if page == "Services"}
                <li class="px-4 flex items-center" >
                    <a 
                        href="{page}.svelte"
                        onmouseenter={() => {
                            active = true;
                        }}
                        onmouseleave={() => {
                            active = false;
                        }}
                    >
                        {page}
                    </a>
                    <span>^</span>

                    <div id="dropdown" class={active ? 'flex absolute top-21 transition-all transform duration-300 ease-in-out opacity-100 bg-white' : 'hidden' }>
                        <ul>
                            {#each services as service}
                                <li class="">
                                    <a href="{service}.svelte">{service}</a>
                                </li>
                            {/each}
                        </ul>
                    </div>
                </li>
                
            {:else}
                <li class="px-4 flex items-center">
                    <a href="{page}.svelte">{page}</a>
                </li>
            {/if}
        {/each}
    </ul>

</nav>
<script>
    let active = $state(false);
    let { 
        logo,
        pages = [
            {title: 'Home', path:"/"},
            {title: 'About', path:"/about"},
            {title: 'Pricing', path:"/pricing"},
            {title: 'Services', path:"/services"},
            {title: 'Contact', path:"/contact"},
            ],
        services = [
            {title: 'Landscaping', path:"/services/landscaping"},
            {title: 'Tree trimming', path:"/services/tree-trimming"},
            {title: 'mulching', path:"/services/mulching"},
            {title: 'property clean ups', path:"/services/property-clean-ups"},
        ]
     } = $props();

</script>

<nav class="bg-white">

    <div class="max-w-325 flex justify-between w-full mx-auto ">
        <div class="max-w-40">
            <img src="/images/pradoLogo.svg" alt="Prado Logo">
        </div>

        <ul class="hidden lg:flex px-4">
            {#each pages as page}
                {#if page.title == "Services"}
                    <li class="px-4 flex items-center"
                        onmouseenter={() => {
                                active = true;
                            }}
                            onmouseleave={() => {
                                active = false;
                            }} >
                        <a href="{page.path}" >
                            {page.title}
                        </a>
                        <span>^</span>

                        <div class={active ? 'flex absolute top-20 bg-white z-50' : 'hidden' }>
                            <ul>
                                {#each services as service}
                                    <li class="">
                                        <a href="{service.path}">{service.title}</a>
                                    </li>
                                {/each}
                            </ul>
                        </div>
                    </li>
                    
                {:else}
                    <li class="px-4 flex items-center">
                        <a href="{page.path}">{page.title}</a>
                    </li>
                {/if}
            {/each}
        </ul>
    </div>

</nav>
<script>
 export let icon;
 export let photo;
 export let name;
 export let int_link;
 export let description;
 export let dl_link;
 export let arch;
 export let is_testing;
</script>

<section class="container mt-2">
    <center>
            <div class="container">
                <a href="{int_link}">
                    <img class="mt-5 mb-1 img-fluid" width="100" src="{icon}" alt="{name}" />
                </a>
                <p class="h1 text-light">{name}</p>
                <p class="text-light m-2">{description}</p>
                {#if dl_link != ""}
                            <a href="https://sourceforge.net/projects/cereus-linux/"><img alt="Download Cereus LxQt" src="https://a.fsdn.com/con/app/sf-download-button" width=27.6% height=4.8% srcset="https://a.fsdn.com/con/app/sf-download-button?button_size=2x 2x"></a>
                {:else}
                            <p class="text-success">Downloads coming soon...</p>
                {/if}
                {#if is_testing == true}
                    <p>
                        <span class="badge bg-warning text-dark">Status: Testing</span>
                    </p>
                {/if}
                <img class="img-fluid m-1" alt="{name}" src="{photo}"/>
                <p class="h4 m-1 text-light small">
                    {name} is available for the following architectures: {arch}
                </p>
            </div>
    </center>
</section>

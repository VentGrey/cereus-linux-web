<script>
 const editions = [
     {
         "icon": "/images/lxqt-logo.png",
         "photo": "/images/lxqt.png",
         "name": "Cereus LxQt",
         "int_link": "/lxqt",
         "description": "LxQt is a lightweight environment that runs on low-resources",
         "dl_link": "https://sourceforge.net/projects/cereus-linux/",
         "arch": "i686 y amd64",
         "is_testing": true
     },
     {
         "icon": "/images/xfce-logo.png",
         "photo": "/images/xfce.png",
         "name": "Cereus Xfce",
         "int_link": "/xfce",
         "description": "Xfce is a lightweight environment that runs on low-resources PCs, different to LxQt, Xfce is more personalizable",
         "dl_link": "",
         "arch": "i686 y amd64",
         "is_testing": false
     },
     {
         "icon": "/images/plasma-logo.png",
         "photo": "/images/plasma.png",
         "name": "Cereus Plasma",
         "int_link": "/plasma",
         "description": "plasma is a modern and highly personalizable environment",
         "dl_link": "",
         "arch": "amd64",
         "is_testing": false
     },
     {
         "icon": "/images/cinnamon-logo.png",
         "photo": "/images/cinnamon.png",
         "name": "Cereus Cinnamon",
         "int_link": "/cinnamon",
         "description": "Cinnamon is a modern and Familiar environment",
         "dl_link": "",
         "arch": "amd64",
         "is_testing": false
     }
 ];
</script>

<section class="container text-white my-2">
    <center>
        <a href="index.html"><img width="33%" src="/images/textlogo.png"></a>
        <a href="index.html"><img width="11%" src="/images/logo.png"></a>
        <h1>Download Cereus Linux</h1>
        <br />
        <h2>Cereus Linux has 4 available editions:</h2>
    </center>
</section>

<section class="container mt-2">
    <center>
        {#each editions as edition}
            <div class="container">
                <a href="{edition.int_link}">
                    <img class="mt-5 mb-1 img-fluid" width="100" src="{edition.icon}" alt="{edition.name}" />
                </a>
                <p class="h1 text-light">{edition.name}</p>
                <p class="text-light m-2">{edition.description}</p>
                {#if edition.dl_link != ""}
                            <a href="https://sourceforge.net/projects/cereus-linux/"><img alt="Download Cereus LxQt" src="https://a.fsdn.com/con/app/sf-download-button" width=27.6% height=4.8% srcset="https://a.fsdn.com/con/app/sf-download-button?button_size=2x 2x"></a>
                {:else}
                            <p class="text-success">Downloads coming soon...</p>
                {/if}
                {#if edition.is_testing == true}
                    <p>
                        <span class="badge bg-warning text-dark">Status: Testing</span>
                    </p>
                {/if}
                <img class="img-fluid m-1" alt="{edition.name}" src="{edition.photo}"/>
                <p class="h4 m-1 text-light small">
                    {edition.name} is available for the following architectures: {edition.arch}
                </p>
            </div>
        {/each}
    </center>
</section>

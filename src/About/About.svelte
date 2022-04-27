<script>
 const contributors = [
     {
     "icon": "/images/kf.png",
     "name": "Kf_Art",
     "description": "FOSS enthusiast, artist and writer in process"
     },
     {
     "icon": "/images/david.png",
     "name": "David Castro",
     "description": "IT technician"
     },
     {
     "icon": "/images/slnx.png",
     "name": "ItzSelenux",
     "description": "Programmer and artist"
     }
 ]
</script>

<section class="container my-2">
    <center>
        <a href="https://sourceforge.net/projects/cereus-linux/" target="_blank" rel="noopener noreferrer"><img width="33%" src="/images/textlogo.png"></a>
        <a href="https://sourceforge.net/projects/cereus-linux/" target="_blank" rel="noopener noreferrer"><img width="11%" class="cereus-spin" src="/images/logo.png"></a>

        <div class="container text-light">
            <h1>About</h1>
            <h2>Cereus Linux is a project that tries to give user-friendy experience to Void Linux. Cereus Linux is developed by:</h2>
        </div>

        <table class="table table-dark text-center table-striped text-light">
            <tbody>
                {#each contributors as contributor}
                    <tr>
                        <td>
                            <figure>
                                <img src="{contributor.icon}" alt="{contributor.name}" />
                                <figcaption>{contributor.name}</figcaption>
                            </figure>
                        </td>
                        <td>
                            <p class="fs-2 fw-bold">{contributor.description}</p>
                        </td>
                    </tr>
                {/each}
            </tbody>
        </table>
        
    </center>
</section>

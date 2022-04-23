<script>
 const editions = [
     {
         "icon": "/images/lxqt-logo-mini.png",
         "name": "LxQt",
         "link": "/lxqt",
         "arch": "i686 & amd64",
         "status": "Testing"

    },
     {
        "icon": "/images/xfce-logo-mini.png",
         "name": "XFCE",
         "link": "/xfce",
        "arch": "i686 & amd64",
        "status": "Not Available"
    },
     {
        "icon": "/images/plasma-logo-mini.png",
         "name": "Plasma",
         "link": "/plasma",
        "arch": "amd64 only",
        "status": "Not Available"
    },
     {
        "icon": "/images/cinnamon-logo-mini.png",
         "name": "Cinnamon",
         "link": "/cinnamon",
        "arch": "amd64 only",
        "status": "Not Available"
    },
 ];
</script>

<style>
 .cereus-text {
     color: #4DB6AC;
 }

 .cereus-spin {
     transition: transform .9s ease-in-out;
 }
 .cereus-spin:hover {
     transform: rotate(360deg);
 }
</style>

<section class="container my-2">
    <center>
        <a href="https://sourceforge.net/projects/cereus-linux/" target="_blank" rel="noopener noreferrer"><img width="33%" src="/images/textlogo.png"></a>
        <a href="https://sourceforge.net/projects/cereus-linux/" target="_blank" rel="noopener noreferrer"><img width="11%" class="cereus-spin" src="/images/logo.png"></a>

        <div class="container text-light">
            <h1>Cereus Linux is a <span class="cereus-text">Void Linux </span>respin focused
                on giving a user-friendly experience
            </h1>
            <h2>We have 4 editions:</h2>
        </div>
        <table class="table table-dark text-center table-striped text-light">
            <thead>
                <tr>
                    <th scope="col">Edition</th>
                    <th scope="col">Architecture</th>
                    <th scope="col">Status</th>
                </tr>
            </thead>
            <tbody>
                {#each editions as edition}
                    <tr>
                        <td>
                            <a class="text-decoration-none" href="{edition.link}">
                                <figure>
                                    <img src="{edition.icon}" alt="{edition.name}" />
                                    <figcaption class="fw-bold text-light">{edition.name}</figcaption>
                                </figure>
                            </a>
                        </td>
                        <td>
                            <h2>{edition.arch}</h2>
                        </td>
                        <td>
                            <h2>{edition.status}</h2>
                        </td>
                    </tr>
                {/each}
            </tbody>
        </table>
        <h4 class="text-white small">Musl Versions are only available on x64, GlibC versions are available for both i686 & amd64</h4>
    </center>
</section>

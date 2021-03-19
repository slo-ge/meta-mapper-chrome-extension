<script lang="ts">
    let currentUrl = '';

    (chrome as any).browserAction?.setIcon({ path: "favicon-96x96.png" });
    (chrome as any).tabs?.query({active: true, lastFocusedWindow: true}, tabs => {
        currentUrl = tabs[0].url;
    });

</script>

<div class="extension">
<div class="heading">Meta-Mapper.com Extension</div>
<div>
<a target="_blank" href="https://meta-mapper.com/editor?adapter=meta_data&data={currentUrl}">Open this Page!</a>
</div>
</div>
<style>
    @import url('https://fonts.googleapis.com/css2?family=Archivo+Black&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300&display=swap');
    body {

    }
    .extension {
        background: linear-gradient(200deg,#fdc8f2, #26ffe6);
        margin: -10px;
        padding: 10px;
        font-family: 'Open Sans', sans-serif;
    }
    .heading {
        min-width: 300px !important;
        font-size: 24px;
        font-family: 'Archivo Black', sans-serif;
        margin-bottom: 15px;
    }

    a {
        font-size: 24px;
        color: black;
        font-weight: bold;
    }
</style>

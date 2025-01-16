<script>
    import Note from '../../components/note.svelte';
    let audNots = [
        {
            title: "Missing Show",
            body: "If the show your are looking for is not showing up please contact your theater"
        },
        {
            title: "Refunds",
            body: "We don't issue refunds through this portal. All refunds must be handled directly between theater and client."
        }
    ]
</script>

<div class="flex flex-col space-y-6">
    <h1>Help</h1>

    <h1>Audience</h1>
    <div class="flex flex-row">
        {#each audNots as {title, body}}
            <Note title={title} body={body} />
        {/each}
        
    </div>

    <h1>Theaters</h1>
    <p>If you are a theater and are experiencing issues with the Thea system please reach out to your Voodu Software representative</p>
</div>
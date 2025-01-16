<script>
    import SeatMap from '../../components/seatmap.svelte';

    let showSel = true;
    let seatSel = false;
    let paySel = false;
    let done = false;

    let show = "Show show";
    let seat = "seat Seat";
</script>

<div class="flex flex-col space-y-4 items-center">
    {#if showSel}
        <h1 class="text-4xl m-4">We found these shows!</h1>
        <div class="border-2 m-2">
            <h1 class="text-2xl">Shows</h1>
        </div>
        <button class="bg-white rounded-xl p-2 hover:scale-110 hover:shadow-xl" onclick={() => {showSel = false; seatSel = true}}>Next</button>
    {/if}
    {#if seatSel}
        <h1 class="text-4xl m-4">Now let's see where you'll sit</h1>
        <SeatMap title={"Seat"}/>
        <button class="bg-white rounded-xl p-2 hover:scale-110 hover:shadow-xl" onclick={() => {seatSel = false; paySel = true}}>Next</button>
    {/if}
    {#if paySel}
        <h1 class="text-4xl m-4">We gotta keep the lights on</h1>
        <button class="bg-white rounded-xl p-2 hover:scale-110 hover:shadow-xl" onclick={() => {paySel = false; done = true}}>Done</button>
    {/if}
    {#if done}
        <h1 class="text-4xl m-4">Your booking has been made!</h1>
        <p>{show}</p>
        <p>{seat}</p>
        <p class="text-2xl m-4">We have dispatched a confirmation email via carrier pigeon!</p>
    {/if}
</div>
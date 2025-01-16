<script>
    import Search from '../../components/search.svelte';
  
    let searchTerm = "";
    let message = "";
  
    function search() {
      if(searchTerm.length >= 4){
        console.log("Searching");
        message = "We are looking for y'ah...";
        window.location.href = '/selection';
      } else {
        message = "We need a bit more to go off of!"
      }
    }
  </script>
  
  <div class="flex flex-col items-center space-y-4">
      <h1 class="text-black">Search your theater</h1>
      <Search bind:name={searchTerm}>
        <button class="bg-white rounded-xl p-2 hover:scale-110 hover:shadow-xl" onclick={() => search()}>Search</button>
      </Search>
  
      <p>{message}</p>
  </div>
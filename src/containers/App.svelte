<script>

  import Header from "../components/Header.svelte";
  import Main from "../components/Main.svelte";
  import TimeLine from "../components/TimeLine.svelte";
  import Sidebar from "../components/Sidebar.svelte";

  const user = {
    nickname: "johndoe",
    name: "John Doe",
  };

</script>

<Header />
<Main>
  <TimeLine />
  <Sidebar {...user} />
</Main>

<style>
  @import url("https://fonts.googleapis.com/css?family=Pacifico&display=swap");
  @import url("https://fonts.googleapis.com/css?family=Lato:300,400,600&display=swap");

  :global(body) {
    background-color: #fafafa;
    color: rgba(38, 38, 38, 0.7);
    font-family: "Lato", sans-serif;
    margin: 0;
    padding: 0;
  }
  :global(h1, h2, h3) {
    margin: 0;
    padding: 0;
  }
</style>

<script>
 let user = {loggedIn:false};

  function toggle(){
    user.loggedIn = !user.loggedIn;
  }
</script>

<h1>Log in and log out</h1>

<!-- if logged in you can log out-->
{#if user.loggedIn}
<button on:click={toggle}>
  Log Out
</button>
{/if}

<!-- if logged out you can log in-->
{#if !user.loggedIn}
<button on:click={toggle}>
  Log In
</button>
{/if}
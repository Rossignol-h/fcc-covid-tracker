<script>
	let isOpen = false;
  export let segment;
  function toggleNav() {
    isOpen = !isOpen
		}
</script>

<!----------------------------------------------------------- HTML  ---->

<nav class="navbar" role="navigation" aria-label="main navigation">
  <div class="navbar-brand">
    <a class="navbar-item" href="/">
      <img src="logo.jpg" width="100" height="100" alt="logo">
				</a>

    <span
      class="navbar-burger"
      class:is-active={isOpen}
      on:click={toggleNav}
      aria-label="menu"
      aria-expanded="false">
      <span aria-hidden="true" />
      <span aria-hidden="true" />
      <span aria-hidden="true" />
    </span>
  </div>

  <div id="navbarBasicExample" class="navbar-menu"class:is-active={isOpen}>
    <div class="navbar-start">
      <a class="navbar-item" class:is-active={segment === undefined} href="/">
        Home
      </a>

      <a class="navbar-item" href="/">
        About
						</a>
      </div>
    </div>

    <div class="navbar-end">
      <div class="navbar-item">
        <div class="buttons">
          <a class="button is-primary" href="/">
            <strong>Sign up</strong>
          </a>
          <a class="button is-light" href="/">
            Log in
          </a>
        </div>
      </div>
    </div>

</nav>


<!----------------------------------------------------------- CSS  ---->

<style>
	nav {
		border-bottom: 1px solid rgba(255,62,0,0.1);
		font-weight: 300;
		padding: 0 1em;
	}

.navbar-item img {
	max-height: none;
}

	ul {
		margin: 0;
		padding: 0;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li {
		display: block;
		float: left;
	}

	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		background-color: rgb(255,62,0);
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
	}
</style>
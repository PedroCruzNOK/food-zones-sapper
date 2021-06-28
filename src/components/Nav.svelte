<script>
	export let segment;
</script>

<style>
	nav {
		border-bottom: 1px solid rgba(255,62,0,0.1);
		font-weight: 300;
		padding: 0 1em;
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
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Navbar</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Features</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Pricing</a>
        </li>
        <li class="nav-item">
          <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Disabled</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
<nav>
	<ul>
		<li><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">Casa</a></li>
		<li><a aria-current="{segment === 'colaboradores' ? 'page' : undefined}" href="colaboradores">Colaboradores</a></li>
		<li><a rel=prefetch aria-current="{segment === 'nosotros' ? 'page' : undefined}" href="nosotros">Nosotros</a></li>
		<li><a rel=prefetch aria-current="{segment === 'noticias' ? 'page' : undefined}" href="noticias">Noticias</a></li>
		<li><a rel=prefetch aria-current="{segment === 'pedido' ? 'page' : undefined}" href="pedido">Pedido</a></li>
		<li><a rel=prefetch aria-current="{segment === 'preguntas' ? 'page' : undefined}" href="preguntas">Preguntas</a></li>
		<li><a rel=prefetch aria-current="{segment === 'terminos' ? 'page' : undefined}" href="terminos">Términos</a></li>
		<li><a rel=prefetch aria-current="{segment === 'contacto' ? 'page' : undefined}" href="contacto">Contacto</a></li>
	</ul>
</nav>

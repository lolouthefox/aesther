<svelte:head>
	<title>Aesther SMP - Modpack Downloads</title>
	<meta
		name="description"
		content="Download the Aesther SMP modpack for Minecraft. Available in Full and Lite versions for different performance needs."
	/>
</svelte:head>

<div class="page-container">
	<header class="page-header">
		<h1>Aesther SMP</h1>
		<p class="version">Version 1</p>
	</header>

	<main class="packs-grid">
		<section class="pack full">
			<div class="pack-header">
				<img src="/branding/aesther-logo.png" alt="Aesther Logo" class="logo" />
			</div>
			<div class="pack-body">
				<p class="description">
					The full experience. Includes shaders, advanced visual effects like dynamic foliage, and
					Voxy for extended chunk rendering. A powerful computer is recommended.
				</p>
				<div class="links">
					<a
						href="https://github.com/lolouthefox/aesther/releases/download/v1.0-alpha/Aesther_modrinth.mrpack"
						rel="external"
					>
						Modrinth App
						<span>.mrpack</span>
					</a>
					<a
						href="https://github.com/lolouthefox/aesther/releases/download/v1.0-alpha/Aesther_prism.zip"
						rel="external"
					>
						Prism Launcher
						<span>.zip</span>
					</a>
					<a
						href="https://github.com/lolouthefox/aesther/releases/download/v1.0-alpha/Aesther_curseforge.zip"
						rel="external"
					>
						CurseForge
						<span>.zip</span>
					</a>
				</div>
				<p class="ram-note">Requires at least 10GB of RAM.</p>
			</div>
		</section>

		<section class="pack lite">
			<div class="pack-header">
				<img src="/branding/aesther-lite-logo.png" alt="Aesther Lite Logo" class="logo" />
			</div>
			<div class="pack-body">
				<p class="description">
					A lightweight version for less powerful computers. Shaders, advanced visual effects, and
					Voxy have been removed for performance, but the core experience remains.
				</p>
				<div class="links">
					<a
						href="https://github.com/lolouthefox/aesther/releases/download/v1.0-alpha/AestherLite_modrinth.mrpack"
						rel="external"
					>
						Modrinth App
						<span>.mrpack</span>
					</a>
					<a
						href="https://github.com/lolouthefox/aesther/releases/download/v1.0-alpha/AestherLite_prism.zip"
						rel="external"
					>
						Prism Launcher
						<span>.zip</span>
					</a>
					<a
						href="https://github.com/lolouthefox/aesther/releases/download/v1.0-alpha/AestherLite_curseforge.zip"
						rel="external"
					>
						CurseForge
						<span>.zip</span>
					</a>
				</div>
				<p class="ram-note">Requires at least 8GB of RAM.</p>
			</div>
		</section>
	</main>
</div>

<style>
	.page-container {
		width: 100%;
		max-width: 90rem;
		padding: 2rem;
	}

	.page-header {
		text-align: center;
		margin-bottom: 4rem;
	}

	.page-header h1 {
		font-size: 3rem;
		font-weight: 700;
		margin-bottom: 0.5rem;
	}

	.page-header .version {
		font-size: 1.2rem;
		color: #aaa;
	}

	.packs-grid {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 4rem;
		align-items: start;
	}

	.pack {
		display: flex;
		flex-direction: column;
		gap: 2rem;
		padding: 2rem;
		border-radius: 16px;
	}

	.pack.full {
		background: var(--primary-color);
		color: var(--light-color);
	}

	.pack.lite {
		background: var(--lite-primary-color);
		color: var(--lite-light-color);
	}

	.pack-header {
		text-align: center;
	}

	.pack .logo {
		width: 100%;
		max-width: 300px;
		height: auto;
	}

	.pack-body {
		display: flex;
		flex-direction: column;
		gap: 1.5rem;
		text-align: center;
	}

	.pack .description {
		font-size: 1rem;
		line-height: 1.6;
		opacity: 0.9;
		max-width: 50ch;
		margin: 0 auto;
	}

	.pack .links {
		display: grid;
		gap: 1rem;
		width: 100%;
		max-width: 400px;
		margin: 0 auto;
	}

	.pack a {
		display: block;
		padding: 1rem 1.5rem;
		text-decoration: none;
		font-weight: 700;
		border-radius: 12px;
		transition: all 0.2s ease;
	}

	.pack.full a {
		background-color: var(--light-color);
		color: var(--dark-color);
	}

	.pack.lite a {
		background-color: var(--lite-light-color);
		color: var(--lite-dark-color);
	}

	.pack a:hover {
		transform: scale(1.05);
	}

	.pack a span {
		font-size: 0.9rem;
		font-weight: 400;
		opacity: 0.8;
		display: block;
		margin-top: 0.25rem;
	}

	.pack .ram-note {
		font-size: 0.9rem;
		opacity: 0.7;
		margin-top: 1rem;
	}

	@media (max-width: 900px) {
		.packs-grid {
			grid-template-columns: 1fr;
		}
	}
</style>

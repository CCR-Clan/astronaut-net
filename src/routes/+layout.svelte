<script lang="ts">
	import '../app.css';
	import Topbar from '$lib/components/Topbar.svelte';
	let { children } = $props();
</script>

<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="anonymous" />
	<link
		href="https://fonts.googleapis.com/css2?family=Figtree:ital,wght@0,300..900;1,300..900&family=Syne:wght@400..800&display=swap"
		rel="stylesheet"
	/>
	<title>Astronaut — Discord protection from the stars</title>
	<meta
		name="description"
		content="Astronaut is a friendly Discord bot that watches your server from the stars to help prevent attacks and threats before they happen."
	/>
</svelte:head>

<div class="site relative min-h-screen">
	<div class="site-bg absolute inset-0 -z-10" aria-hidden="true">
		<div class="site-gradient"></div>
		<div class="site-dust"></div>
	</div>
	<div class="min-h-screen">
		<Topbar />
		<main class="relative">
			{@render children()}
		</main>
		<footer class="mt-8 border-t border-amber-500/15">
			<div class="mx-auto max-w-5xl px-4 py-14 sm:px-6">
				<div class="flex flex-col gap-10 sm:flex-row sm:justify-between">
					<div class="max-w-sm">
						<p class="font-display text-xl font-bold leading-[1.2] tracking-tight text-amber-300">
							Astronaut
						</p>
						<p class="mt-2 text-sm leading-relaxed text-stone-500">
							A friendly space bot watching Discord servers from the stars, stopping threats before they land!
						</p>
					</div>
					<div class="flex gap-16">
						<div>
							<p class="text-xs font-medium uppercase tracking-[0.18em] text-stone-500">Explore</p>
							<div class="mt-3 flex flex-col gap-2">
								<a href="/#prevention" class="text-sm text-stone-400 transition-colors hover:text-amber-300"
									>Prevention</a
								>
								<a href="/#strikes" class="text-sm text-stone-400 transition-colors hover:text-amber-300"
									>Strikes</a
								>
								<a href="/#reports" class="text-sm text-stone-400 transition-colors hover:text-amber-300"
									>Reports</a
								>
							</div>
						</div>
					</div>
				</div>
				<div class="mt-12 flex flex-col items-start justify-between gap-2 border-t border-amber-500/10 pt-6 sm:flex-row sm:items-center">
					<p class="text-xs text-stone-600">© 2026 CCR Clan</p>
					<a
						href="https://github.com/cattn"
						class="text-xs text-stone-600 transition-colors hover:text-amber-400/80"
						>by Cattn & Astra</a
					>
				</div>
			</div>
		</footer>
	</div>
</div>

<style>
	.site {
		font-family: 'Figtree', sans-serif;
	}

	.font-display {
		font-family: 'Syne', sans-serif;
	}

	.site-bg {
		background: #0c0a09;
	}

	.site-gradient {
		position: absolute;
		inset: 0;
		background:
			radial-gradient(ellipse 80% 50% at 50% -10%, rgba(245, 158, 11, 0.07), transparent 55%),
			radial-gradient(ellipse 60% 40% at 100% 50%, rgba(120, 53, 15, 0.06), transparent 50%),
			linear-gradient(180deg, #0c0a09 0%, #090807 100%);
	}

	.site-dust {
		position: absolute;
		inset: 0;
		opacity: 0.35;
		background-image:
			radial-gradient(1px 1px at 12% 18%, rgba(253, 230, 138, 0.35), transparent),
			radial-gradient(1px 1px at 48% 62%, rgba(255, 255, 255, 0.2), transparent),
			radial-gradient(1px 1px at 78% 28%, rgba(253, 230, 138, 0.25), transparent),
			radial-gradient(1px 1px at 33% 88%, rgba(255, 255, 255, 0.15), transparent);
		background-size: 100% 100%;
	}
</style>

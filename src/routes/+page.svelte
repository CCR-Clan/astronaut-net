<script lang="ts">
	import { Button } from '$lib/components/ui/button/index.js';
</script>

<section class="hero relative flex min-h-[100svh] flex-col justify-center overflow-hidden">
	<div class="starfield absolute inset-0 -z-10" aria-hidden="true">
		<div class="stars stars-a"></div>
		<div class="stars stars-b"></div>
		<div class="nebula"></div>
		<div class="horizon"></div>
	</div>

	<div class="hero-content mx-auto w-full max-w-5xl px-4 pb-24 pt-8 sm:px-6 sm:pb-32">
		<p class="brand-mark mb-4 text-5xl font-bold tracking-tight sm:text-7xl md:text-8xl">
			<span class="brand-gold">Astronaut</span>
		</p>
		<h1 class="max-w-2xl text-2xl font-semibold leading-[1.2] text-stone-100 sm:text-3xl md:text-4xl">
			Your friendly space bot, watching from the stars.
		</h1>
		<p class="mt-5 max-w-xl text-base leading-relaxed text-stone-400 sm:text-lg">
			I watch your server and others like it to help prevent attacks and threats before they happen.
		</p>
		<div class="mt-8 flex flex-wrap items-center gap-3">
			<Button
				href="/#prevention"
				class="bg-amber-400 text-stone-950 hover:bg-amber-300"
			>
				See how I work
			</Button>
			<Button
				href="/#strikes"
				variant="outline"
				class="border-amber-500/40 text-amber-200 hover:bg-amber-500/10 hover:text-amber-100"
			>
				Strike system
			</Button>
		</div>
	</div>
</section>

<section class="intro-voice mx-auto max-w-3xl px-4 py-20 sm:px-6 sm:py-28">
	<p class="font-display text-xl leading-relaxed text-stone-200 sm:text-2xl">
		Hello there! I'm Astronaut, your friendly space bot! I watch your server and others like it from
		the stars to help prevent attacks and threats before they happen! I function in this server
		automatically and if I miss a threat, I'll remember them for next time. I hope you have a great
		day!
	</p>
</section>

<section id="prevention" class="section-fade border-t border-amber-500/10 scroll-mt-20">
	<div class="mx-auto max-w-3xl px-4 py-20 sm:px-6 sm:py-28">
		<p class="mb-3 text-sm font-medium uppercase tracking-[0.2em] text-amber-400/80">Prevention</p>
		<h2 class="font-display text-3xl font-semibold text-stone-50 sm:text-4xl">
			Every message, checked in real time
		</h2>
		<p class="mt-5 text-base leading-relaxed text-stone-400 sm:text-lg">
			Whenever a message is sent in a server Astronaut can see, it runs a check on the message and
			the author's User ID and Message Content compared against its database immediately.
		</p>
		<ul class="mt-10 space-y-6 text-stone-300">
			<li class="border-l-2 border-amber-400/50 pl-5">
				<span class="font-medium text-amber-200">User ID</span>
				<p class="mt-1 text-stone-400">
					Too many strikes? Checked against the ban database and then removed from the server.
				</p>
			</li>
			<li class="border-l-2 border-amber-400/50 pl-5">
				<span class="font-medium text-amber-200">Message content</span>
				<p class="mt-1 text-stone-400">
					Harmful links and raid links are deleted, and raiders are removed.
				</p>
			</li>
		</ul>
		<p class="mt-10 text-sm text-stone-500">
			Advanced harmful-link checking is still developing and may not catch anything right now.
		</p>
	</div>
</section>

<section id="strikes" class="section-fade border-t border-amber-500/10 scroll-mt-20">
	<div class="mx-auto max-w-3xl px-4 py-20 sm:px-6 sm:py-28">
		<p class="mb-3 text-sm font-medium uppercase tracking-[0.2em] text-amber-400/80">Strike System</p>
		<h2 class="font-display text-3xl font-semibold text-stone-50 sm:text-4xl">
			Strikes follow the User ID
		</h2>
		<p class="mt-5 text-base leading-relaxed text-stone-400 sm:text-lg">
			Every user has a strike count by User ID. Strikes come from harmful activities like raids,
			scams, phishing, etc. and they do not expire. Permanent unless manually removed.
		</p>
		<div class="mt-10 grid gap-8 sm:grid-cols-2">
			<div>
				<p class="text-amber-300">Minor</p>
				<p class="mt-1 text-stone-400">1-5 strikes</p>
			</div>
			<div>
				<p class="text-amber-300">Major</p>
				<p class="mt-1 text-stone-400">1-10 strikes</p>
			</div>
		</div>
		<p class="mt-10 leading-relaxed text-stone-300">
			At <span class="text-amber-200">10+ strikes</span>, users are automatically removed from every
			server where Astronaut can remove them.
		</p>
		<p class="mt-4 text-sm text-stone-500">
			Reasons are DMed when a strike updates, but reasons are not stored in the bot.
		</p>
	</div>
</section>

<section id="reports" class="section-fade border-t border-amber-500/10 scroll-mt-20">
	<div class="mx-auto max-w-3xl px-4 py-20 sm:px-6 sm:py-28">
		<p class="mb-3 text-sm font-medium uppercase tracking-[0.2em] text-amber-400/80">Reports</p>
		<h2 class="font-display text-3xl font-semibold text-stone-50 sm:text-4xl">
			Report members when something slips through
		</h2>
		<p class="mt-5 text-base leading-relaxed text-stone-400 sm:text-lg">
			Non-blacklisted users can report members. You'll be asked for the user (must be in the
			server), a reason, and whether the violation happened in the reporting channel.
		</p>
		<p class="mt-8 leading-relaxed text-stone-300">
			Reports go to authorized CCR Clan members and include reporter and reported user info, the
			reason, and extras like screenshots. If the violation was in-channel, a transcript is
			uploaded.
		</p>
		<p class="mt-8 text-sm text-stone-500">
			If action is taken, the reporter is not notified and the reported user is never told who
			reported them.
		</p>
	</div>
</section>

<style>
	.font-display {
		font-family: 'Syne', sans-serif;
	}

	.brand-mark {
		font-family: 'Syne', sans-serif;
		line-height: 1.15;
	}

	.hero-content {
		animation: hero-enter 1.1s cubic-bezier(0.22, 1, 0.36, 1) both;
	}

	.brand-gold {
		display: inline-block;
		padding-bottom: 0.1em;
		--shine-x: 0%;
		color: #f59e0b;
		background-image: linear-gradient(
			90deg,
			#92400e 0%,
			#b45309 10%,
			#d97706 18%,
			#f59e0b 28%,
			#fde68a 35%,
			#f59e0b 42%,
			#d97706 46%,
			#92400e 50%,
			#b45309 60%,
			#d97706 68%,
			#f59e0b 78%,
			#fde68a 85%,
			#f59e0b 92%,
			#d97706 96%,
			#92400e 100%
		);
		background-size: 200% 100%;
		background-position: var(--shine-x) 50%;
		-webkit-background-clip: text;
		background-clip: text;
		-webkit-text-fill-color: transparent;
		animation: brand-shine 3.2s linear infinite;
	}

	.starfield {
		background: radial-gradient(ellipse 120% 80% at 50% 100%, #1a1208 0%, #0c0a09 45%, #050403 100%);
	}

	.nebula {
		position: absolute;
		inset: 0;
		background:
			radial-gradient(ellipse 60% 40% at 70% 20%, rgba(245, 158, 11, 0.12), transparent 70%),
			radial-gradient(ellipse 50% 35% at 20% 60%, rgba(180, 83, 9, 0.08), transparent 65%);
	}

	.horizon {
		position: absolute;
		inset: auto 0 0;
		height: 40%;
		background: linear-gradient(to top, rgba(245, 158, 11, 0.06), transparent);
	}

	.stars {
		position: absolute;
		inset: 0;
		background-repeat: repeat;
	}

	.stars-a {
		background-image:
			radial-gradient(1.5px 1.5px at 10% 20%, rgba(253, 230, 138, 0.9), transparent),
			radial-gradient(1px 1px at 30% 65%, rgba(255, 255, 255, 0.7), transparent),
			radial-gradient(1.5px 1.5px at 55% 15%, rgba(253, 230, 138, 0.8), transparent),
			radial-gradient(1px 1px at 75% 40%, rgba(255, 255, 255, 0.55), transparent),
			radial-gradient(1px 1px at 90% 70%, rgba(253, 230, 138, 0.7), transparent),
			radial-gradient(1.5px 1.5px at 45% 85%, rgba(255, 255, 255, 0.5), transparent),
			radial-gradient(1px 1px at 15% 45%, rgba(253, 230, 138, 0.6), transparent),
			radial-gradient(1px 1px at 65% 55%, rgba(255, 255, 255, 0.65), transparent);
		background-size: 320px 320px;
		animation: drift 80s linear infinite, twinkle 4s ease-in-out infinite alternate;
		opacity: 0.85;
	}

	.stars-b {
		background-image:
			radial-gradient(1px 1px at 20% 30%, rgba(255, 255, 255, 0.5), transparent),
			radial-gradient(1.5px 1.5px at 40% 10%, rgba(253, 230, 138, 0.55), transparent),
			radial-gradient(1px 1px at 60% 75%, rgba(255, 255, 255, 0.45), transparent),
			radial-gradient(1px 1px at 80% 25%, rgba(253, 230, 138, 0.5), transparent),
			radial-gradient(1.5px 1.5px at 5% 80%, rgba(255, 255, 255, 0.4), transparent);
		background-size: 420px 420px;
		animation: drift 120s linear infinite reverse, twinkle 5.5s ease-in-out infinite alternate-reverse;
		opacity: 0.6;
	}

	.section-fade {
		animation: section-in 0.9s ease both;
		animation-timeline: view();
		animation-range: entry 0% cover 30%;
	}

	@keyframes hero-enter {
		from {
			opacity: 0;
			transform: translateY(1.5rem);
		}
		to {
			opacity: 1;
			transform: translateY(0);
		}
	}

	@keyframes brand-shine {
		to {
			--shine-x: 100%;
		}
	}

	@keyframes drift {
		from {
			background-position: 0 0;
		}
		to {
			background-position: 320px 160px;
		}
	}

	@keyframes twinkle {
		from {
			opacity: 0.45;
		}
		to {
			opacity: 0.95;
		}
	}

	@keyframes section-in {
		from {
			opacity: 0.35;
			transform: translateY(0.75rem);
		}
		to {
			opacity: 1;
			transform: translateY(0);
		}
	}

	@media (prefers-reduced-motion: reduce) {
		.hero-content,
		.stars-a,
		.stars-b,
		.section-fade {
			animation: none;
		}
	}
</style>

<script lang="ts">
	import { onMount } from 'svelte';

	// Data for "In the Media"
	const mediaItems = [
		{
			title: "Kiwi firm designs low-cost, fast-build house",
			source: "RNZ",
			link: "#"
		},
		{
			title: "How a $335k fast-build home aims to tackle NZ's housing crisis",
			source: "NZ Herald",
			link: "#"
		},
		{
			title: "Affordable house impresses global judges",
			source: "ArchitectureNZ",
			link: "#"
		},
		{
			title: "New design offers hope for first home buyers",
			source: "Stuff",
			link: "#"
		}
	];

	// Data for "How it works"
	const steps = [
		{
			number: "01",
			title: "Find a site",
			desc: "Ensure your site is suitable and has connections for electricity, water and wastewater/stormwater (or a design for on-site disposal). Obtain a site survey and get geotechnical information."
		},
		{
			number: "02",
			title: "Choose your builder",
			desc: "Each Living House must be constructed by a Licensed Building Practitioner (LBP). You select your own builder."
		},
		{
			number: "03",
			title: "Purchase our detailed design package/plan",
			desc: "Our drawings, specification and engineering calculations come with a MultiProof approval, ready for submitting as part of your Building Consent. You will also receive a Builder's Manual, construction schedule and partner supplier contacts including access to preferential rates we've negotiated with our partner supplier network. The design package includes a one-to-two-hour online consultation for your builder (or builders if tendering out to a few different builders). It's a chance to meet with the architect prior to pricing so that they understand the concept of the project and how the modular assembly process differs from traditional house building. There is no additional cost for this service."
		},
		{
			number: "04",
			title: "Plan your Living House",
			desc: "Select your exterior and interior colour palette and choose your appliances — some additional options are available."
		},
		{
			number: "05",
			title: "Site Specific Consents",
			desc: "Work with a designer and engineer to develop a site specific building consent for foundations and services. You may also need resource consent separate to the building consent. The MultiProof covers the consent for the building itself, but site specific information is required for council applications."
		},
		{
			number: "06",
			title: "Apply for consent",
			desc: "Submit the MultiProof approval certificate, drawings, specifications and supporting documents to your Building Consent Authority (BCA) for a site-specific consent (the MultiProof reduces the time for Council to review your application from 20 days to 10 days). You may also need resource consent. Your builder or an authorised agent may manage this process."
		},
		{
			number: "07",
			title: "Order your Living House modules",
			desc: "Your detailed design package/plans include a unique code to order materials and appliances directly from our supply partners. Your LBP will manage this process for you."
		},
		{
			number: "08",
			title: "Complete foundation work",
			desc: "Once building consent is approved, install services and complete groundwork. When your timber pile foundations are ready, it's time to build."
		},
		{
			number: "09",
			title: "Begin assembly",
			desc: "Your Builder's Manual and schedule provide step-by-step guidance. From this point, your home can be assembled in as little as six weeks."
		}
	];

	// Data for Benefits
	const benefits = [
		{
			title: "Minimum Cost",
			desc: "A more affordable path to homeownership. Ideal for new subdivisions, community housing providers, papakāinga housing, secondary dwellings and home buyers looking for a more accessible option."
		},
		{
			title: "Rapid Construction",
			desc: "A flat-pack build-up system of truck-transportable modules. Designed for fast, simple assembly, the 36 cross-laminated timber modules can be put together by three people in six weeks or less."
		},
		{
			title: "Comfortable Living",
			desc: "Designed for year-round comfort, with a focus on healthy indoor air quality, efficient heating, cooling and ventilation."
		},
		{
			title: "Modern Convenience",
			desc: "Kitchen appliances, hot water, heat pump and solar panel solutions are all included, designed for a comfortable, energy-efficient living experience."
		},
		{
			title: "Climate Positive",
			desc: "The Lever Room, a leading science-based consulting and technology company, comprehensively measured embodied and operational carbon emissions. Their analysis confirmed that the Living House draws down more carbon than it emits."
		}
	];
</script>

<div class="min-h-screen bg-white text-black font-sans selection:bg-black selection:text-white">
	<!-- Header -->
	<header class="px-6 py-8 md:px-12 flex flex-col md:flex-row justify-between items-start md:items-center gap-4">
		<a href="/" class="text-5xl md:text-7xl font-bold tracking-tighter leading-none">Living House</a>
		<p class="text-lg md:text-xl max-w-md md:text-right font-medium leading-tight">
			Low cost, fast build, climate positive houses designed by RTA Studio.
		</p>
	</header>

	<!-- Hero Image -->
	<section class="w-full h-[60vh] md:h-[80vh] overflow-hidden">
		<img 
			src="https://images.unsplash.com/photo-1523217582562-09d0def993a6?q=80&w=2680&auto=format&fit=crop" 
			alt="Living House Exterior" 
			class="w-full h-full object-cover"
		/>
	</section>

	<!-- Introduction -->
	<section class="px-6 py-24 md:px-12 max-w-7xl mx-auto">
		<h1 class="text-5xl md:text-8xl font-bold tracking-tighter mb-12 leading-[0.9]">
			Houses that give<br>more than<br>they take
		</h1>
		
		<div class="max-w-2xl">
			<h2 class="text-3xl md:text-4xl font-bold tracking-tight mb-8">
				A warm, healthy, affordable home built with cross-laminated timber.
			</h2>
			<button class="border border-black rounded-full px-8 py-3 text-sm font-medium hover:bg-black hover:text-white transition-colors">
				About us
			</button>
		</div>
	</section>

	<!-- Diagrams / Features Section -->
	<section class="px-6 md:px-12 max-w-7xl mx-auto space-y-32 mb-32">
		<!-- Block 1 -->
		<div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
			<div class="aspect-[4/3] relative p-8">
				<!-- SVG Diagram Placeholder: Roof -->
				<svg viewBox="0 0 400 300" fill="none" stroke="currentColor" stroke-width="1.5" class="w-full h-full text-gray-800">
					<path d="M50 150 L200 50 L350 150" />
					<path d="M50 150 L50 250 L350 250 L350 150" />
					<path d="M200 50 L200 250" stroke-dasharray="4 4" />
					<path d="M50 150 L200 250" stroke-opacity="0.2" />
					<path d="M350 150 L200 250" stroke-opacity="0.2" />
					<rect x="100" y="100" width="200" height="100" transform="rotate(-10 200 150)" stroke-opacity="0.5" />
				</svg>
			</div>
			<div class="space-y-6">
				<h3 class="text-4xl md:text-5xl font-bold tracking-tight">Available now!</h3>
				<p class="text-sm leading-relaxed max-w-md">
					We're not traditional builders or developers — we've designed a highly efficient way to build.
				</p>
				<p class="text-sm leading-relaxed max-w-md">
					For a purchase price of $10,000, you'll receive detailed drawings and specifications complete with a MultiProof approval certificate and exclusive access to preferential rates we have negotiated on building modules, cladding, joinery, heating and ventilation products, and premium appliances from our respected industry supply partners.
				</p>
				<button class="border border-black rounded-full px-8 py-3 text-sm font-medium hover:bg-black hover:text-white transition-colors mt-4">
					Find out more
				</button>
			</div>
		</div>

		<!-- Block 2 -->
		<div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
			<div class="aspect-[4/3] relative p-8">
				<!-- SVG Diagram Placeholder: Structure -->
				<svg viewBox="0 0 400 300" fill="none" stroke="currentColor" stroke-width="1.5" class="w-full h-full text-gray-800">
					<path d="M50 200 L150 150 L250 200 L150 250 Z" />
					<path d="M150 150 L150 100" />
					<path d="M50 200 L50 150 L150 100" />
					<path d="M250 200 L250 150 L150 100" />
					<path d="M150 250 L150 200" stroke-dasharray="4 4" />
					<rect x="200" y="180" width="150" height="80" stroke-opacity="0.5" />
					<path d="M200 180 L250 150" />
				</svg>
			</div>
			<div class="space-y-6">
				<h3 class="text-4xl md:text-5xl font-bold tracking-tight">Available now!</h3>
				<p class="text-sm leading-relaxed max-w-md">
					We're not traditional builders or developers — we've designed a highly efficient way to build.
				</p>
				<p class="text-sm leading-relaxed max-w-md">
					For a purchase price of $10,000, you'll receive detailed drawings and specifications complete with a MultiProof approval certificate and exclusive access to preferential rates we have negotiated on building modules, cladding, joinery, heating and ventilation products, and premium appliances from our respected industry supply partners.
				</p>
				<button class="border border-black rounded-full px-8 py-3 text-sm font-medium hover:bg-black hover:text-white transition-colors mt-4">
					Find out more
				</button>
			</div>
		</div>

		<!-- Block 3 -->
		<div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
			<div class="aspect-[4/3] relative p-8">
				<!-- SVG Diagram Placeholder: Exploded View -->
				<svg viewBox="0 0 400 300" fill="none" stroke="currentColor" stroke-width="1.5" class="w-full h-full text-gray-800">
					<rect x="50" y="150" width="100" height="100" />
					<rect x="160" y="120" width="100" height="100" />
					<rect x="270" y="90" width="100" height="100" />
					<path d="M150 200 L160 170" stroke-dasharray="2 2" />
					<path d="M260 170 L270 140" stroke-dasharray="2 2" />
					<text x="50" y="280" font-size="10" fill="currentColor">Pre-made structural timber modules</text>
				</svg>
			</div>
			<div class="space-y-6">
				<h3 class="text-4xl md:text-5xl font-bold tracking-tight leading-none">
					85 m²<br>3 Bedrooms<br>1 Bathroom
				</h3>
				<p class="text-xs text-gray-500 max-w-md">
					Pre-made structural timber modules are delivered to site and efficiently slot together to reduce cost, waste and build time.
				</p>
			</div>
		</div>

		<!-- Block 4 -->
		<div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
			<div class="aspect-[4/3] relative p-8">
				<!-- SVG Diagram Placeholder: Frame -->
				<svg viewBox="0 0 400 300" fill="none" stroke="currentColor" stroke-width="1.5" class="w-full h-full text-gray-800">
					<path d="M50 100 L350 100 L350 250 L50 250 Z" />
					<line x1="150" y1="100" x2="150" y2="250" />
					<line x1="250" y1="100" x2="250" y2="250" />
					<path d="M50 100 L200 50 L350 100" />
				</svg>
			</div>
			<div class="space-y-6">
				<h3 class="text-4xl md:text-5xl font-bold tracking-tight leading-none">
					85 m²<br>3 Bedrooms<br>1 Bathroom<br>$335,000*
				</h3>
				<p class="text-sm leading-relaxed max-w-md">
					Partnering with architects <a href="#" class="underline">RTA Studio</a> and other industry leaders, we've transformed house building into a streamlined system that three people can assemble in just six weeks or less — the time it took to build our prototype — for a cost of approximately $335,000*
				</p>
				<button class="border border-black rounded-full px-8 py-3 text-sm font-medium hover:bg-black hover:text-white transition-colors mt-4">
					See the cost breakdown
				</button>
				<p class="text-xs text-gray-500">*Estimated construction cost for house only</p>
			</div>
		</div>
	</section>

	<!-- Color Options Section -->
	<section class="w-full bg-blue-50/50 relative mb-32">
		<div class="w-full h-[60vh] md:h-[80vh] relative">
			<img 
				src="https://images.unsplash.com/photo-1512917774080-9991f1c4c750?q=80&w=2670&auto=format&fit=crop" 
				alt="House Exterior Color Options" 
				class="w-full h-full object-cover"
			/>
			<div class="absolute bottom-12 left-1/2 -translate-x-1/2 bg-white px-6 py-2 rounded-full flex items-center gap-4 shadow-lg">
				<div class="flex gap-2">
					<div class="w-6 h-6 rounded-full bg-[#3d4c53] border border-gray-200"></div>
					<div class="w-6 h-6 rounded-full bg-[#5d4037] border border-gray-200"></div>
					<div class="w-6 h-6 rounded-full bg-[#455a64] border border-gray-200"></div>
					<div class="w-6 h-6 rounded-full bg-[#d7ccc8] border border-gray-200"></div>
				</div>
				<span class="text-sm font-medium border-l border-gray-300 pl-4">Exterior & Interior Colour Options</span>
			</div>
		</div>
	</section>

	<!-- Fence Image Section -->
	<section class="w-full h-[50vh] mb-32 overflow-hidden">
		<img 
			src="https://images.unsplash.com/photo-1621847468516-1ed5d0df56fe?q=80&w=2574&auto=format&fit=crop" 
			alt="Exterior Fence Detail" 
			class="w-full h-full object-cover"
		/>
	</section>

	<!-- Interior Benefits Section -->
	<section class="px-6 md:px-12 max-w-7xl mx-auto mb-32">
		<h2 class="text-4xl md:text-6xl font-bold tracking-tight mb-12">
			Light, generous, warm, cheerful homes.
		</h2>
		<div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
			<div class="aspect-[4/5] bg-gray-100 overflow-hidden">
				<img 
					src="https://images.unsplash.com/photo-1556912172-45b7abe8d7e1?q=80&w=2670&auto=format&fit=crop" 
					alt="Interior Kitchen" 
					class="w-full h-full object-cover"
				/>
			</div>
			<div class="space-y-8">
				{#each benefits as benefit}
					<div class="border-t border-gray-200 pt-4">
						<h3 class="font-bold text-lg mb-2">{benefit.title}</h3>
						<p class="text-sm leading-relaxed text-gray-700">{benefit.desc}</p>
					</div>
				{/each}
			</div>
		</div>
	</section>

	<!-- Floorplan Section -->
	<section class="px-6 md:px-12 max-w-7xl mx-auto mb-32">
		<h2 class="text-4xl md:text-5xl font-bold tracking-tight mb-4">Floorplan</h2>
		<p class="text-sm max-w-2xl mb-12">
			At 85m², the Living House is compact but not tiny. The floorplan is organised around a 4m stud height. Each of the 3 bedrooms and the bathroom is a generous 11.9m² and the combined kitchen and living area 28.3m².
		</p>
		
		<div class="w-full border-2 border-black p-8 relative">
			<div class="text-center font-bold text-xl mb-4">11.39m</div>
			<div class="flex">
				<div class="w-12 h-full flex items-center justify-center font-bold text-xl -rotate-90 absolute left-0 top-1/2 -translate-y-1/2">7.59m</div>
				<!-- SVG Floorplan -->
				<svg viewBox="0 0 800 500" fill="none" stroke="black" stroke-width="2" class="w-full h-auto">
					<!-- Outer Walls -->
					<rect x="50" y="50" width="700" height="400" />
					<!-- Inner Walls -->
					<line x1="300" y1="50" x2="300" y2="450" />
					<line x1="500" y1="50" x2="500" y2="450" />
					<line x1="50" y1="250" x2="300" y2="250" />
					<line x1="500" y1="250" x2="750" y2="250" />
					<!-- Doors/Windows indications -->
					<rect x="280" y="230" width="40" height="40" fill="white" stroke="none" />
					<path d="M280 250 A 30 30 0 0 1 310 220" stroke="black" stroke-width="1" />
					
					<!-- Labels -->
					<text x="150" y="150" text-anchor="middle" font-size="14" stroke="none" fill="black">Bedroom 1</text>
					<text x="150" y="350" text-anchor="middle" font-size="14" stroke="none" fill="black">Bedroom 2</text>
					<text x="400" y="250" text-anchor="middle" font-size="14" stroke="none" fill="black">Living / Dining</text>
					<text x="625" y="150" text-anchor="middle" font-size="14" stroke="none" fill="black">Bedroom 3</text>
					<text x="625" y="350" text-anchor="middle" font-size="14" stroke="none" fill="black">Bathroom</text>
				</svg>
			</div>
		</div>
	</section>

	<!-- Design Section -->
	<section class="px-6 md:px-12 max-w-7xl mx-auto mb-32">
		<h2 class="text-4xl md:text-5xl font-bold tracking-tight mb-12">Design</h2>
		<div class="grid grid-cols-1 md:grid-cols-2 gap-8">
			<div class="space-y-2">
				<div class="aspect-[3/4] overflow-hidden">
					<img 
						src="https://images.unsplash.com/photo-1518780664697-55e3ad937233?q=80&w=2565&auto=format&fit=crop" 
						alt="Living House exterior in ColorSteel" 
						class="w-full h-full object-cover"
					/>
				</div>
				<p class="text-xs text-gray-500">Living House exterior in ColorSteel®</p>
			</div>
			<div class="space-y-2">
				<div class="aspect-[3/4] overflow-hidden">
					<img 
						src="https://images.unsplash.com/photo-1616594039964-408359566a05?q=80&w=2670&auto=format&fit=crop" 
						alt="Bedroom showing Cross-laminated timber wall panels" 
						class="w-full h-full object-cover"
					/>
				</div>
				<p class="text-xs text-gray-500">Bedroom showing Cross-laminated timber wall panels. Each bedroom is 11.9 m².</p>
			</div>
		</div>
	</section>

	<!-- In the Media -->
	<section class="px-6 md:px-12 mb-32 w-full overflow-hidden">
		<h2 class="text-4xl md:text-5xl font-bold tracking-tight mb-12 max-w-7xl mx-auto">In the Media</h2>
		<!-- Horizontal Scroll Container -->
		<div class="flex overflow-x-auto gap-6 pb-8 px-6 md:px-12 -mx-6 md:-mx-12 scrollbar-hide">
			{#each mediaItems as item}
				<a href={item.link} class="flex-shrink-0 w-80 md:w-96 border border-black p-6 flex flex-col justify-between h-64 hover:bg-gray-50 transition-colors group">
					<h3 class="text-2xl font-bold leading-tight group-hover:underline decoration-2 underline-offset-4">{item.title}</h3>
					<div class="flex justify-between items-end">
						<span class="font-medium">{item.source}</span>
						<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-external-link"><path d="M15 3h6v6"/><path d="M10 14 21 3"/><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/></svg>
					</div>
				</a>
			{/each}
		</div>
	</section>

	<!-- How it works -->
	<section class="px-6 md:px-12 max-w-7xl mx-auto mb-32">
		<div class="grid grid-cols-1 lg:grid-cols-2 gap-16">
			<!-- Left: Sticky Title + Image/Video -->
			<div class="relative lg:sticky lg:top-12 h-fit self-start">
				<h2 class="text-5xl md:text-7xl font-bold tracking-tighter mb-8 leading-none">How it works</h2>
				<div class="aspect-video relative overflow-hidden group cursor-pointer bg-gray-100">
					<img 
						src="https://images.unsplash.com/photo-1504307651254-35680f356dfd?q=80&w=2670&auto=format&fit=crop" 
						alt="Construction Timelapse" 
						class="w-full h-full object-cover"
					/>
					<div class="absolute inset-0 flex items-center justify-center">
						<button class="bg-white/90 px-6 py-2 rounded-full text-sm font-bold flex items-center gap-2 hover:bg-white transition-colors shadow-sm">
							<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="currentColor" stroke="none" class="text-black"><polygon points="5 3 19 12 5 21 5 3"/></svg>
							Watch the build timelapse
						</button>
					</div>
				</div>
			</div>

			<!-- Right: Steps List -->
			<div class="space-y-12 lg:pt-32">
				<div class="mb-8">
					<h3 class="font-bold text-xl mb-4">Process</h3>
					<p class="text-sm leading-relaxed text-gray-700">
						Our 3-bedroom home system optimises materials, streamlines suppliers and requires only a small team for fast, straightforward assembly — saving you time, effort and resources. Here are the key steps.
					</p>
				</div>

				{#each steps as step}
					<div class="flex gap-6 border-t border-gray-100 pt-8 first:border-0 first:pt-0">
						<div class="flex-shrink-0 w-10 h-10 rounded-full border border-black flex items-center justify-center font-bold text-sm bg-white">
							{step.number}
						</div>
						<div>
							<h4 class="font-bold text-lg mb-2">{step.title}</h4>
							<p class="text-sm leading-relaxed text-gray-700">{step.desc}</p>
						</div>
					</div>
				{/each}

				<div class="pt-8">
					<button class="border border-black rounded-full px-8 py-3 text-sm font-medium hover:bg-black hover:text-white transition-colors">
						Find out more
					</button>
				</div>
			</div>
		</div>
	</section>

	<!-- Pricing Cards -->
	<section class="px-6 md:px-12 max-w-7xl mx-auto mb-32 grid grid-cols-1 md:grid-cols-[1fr_2fr] gap-8">
		<!-- Logo Mark -->
		<div class="hidden md:flex items-end justify-start">
			<svg viewBox="0 0 100 100" class="w-48 h-48" fill="none" stroke="black" stroke-width="8">
				<path d="M10 50 L50 10 L90 50" stroke-linecap="square" />
				<path d="M20 50 L20 90 L80 90 L80 50" stroke-linecap="square" />
			</svg>
		</div>

		<div class="space-y-8">
			<!-- Card 1 -->
			<div class="border border-black p-8 flex flex-col md:flex-row justify-between items-start md:items-end gap-6">
				<div class="space-y-4 max-w-lg">
					<h3 class="text-2xl font-bold">Purchase Plans</h3>
					<p class="text-sm text-gray-700">
						To build your Living House you'll first need to purchase our detailed design package which includes plan drawings, specifications and engineering calculations.
					</p>
					<a href="#" class="inline-flex items-center text-sm underline font-medium">
						<svg class="w-4 h-4 mr-1" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 18l6-6-6-6"/></svg>
						What's included
					</a>
				</div>
				<div class="text-right w-full md:w-auto flex flex-col items-end gap-4">
					<div class="text-right">
						<div class="font-bold text-xl">$10,000 incl. gst</div>
					</div>
					<button class="bg-black text-white rounded-full px-8 py-3 text-sm font-medium hover:bg-gray-800 transition-colors w-full md:w-auto">
						Enquire to purchase
					</button>
				</div>
			</div>

			<!-- Card 2 -->
			<div class="border border-black p-8">
				<h3 class="text-2xl font-bold mb-6">Construction Costs</h3>
				<div class="flex flex-col md:flex-row justify-between items-start md:items-center gap-6 border-b border-gray-200 pb-6 mb-6">
					<div class="flex gap-8 text-sm">
						<div>
							<span class="text-gray-500 block text-xs">Floor Area</span>
							<span class="font-bold">85 m²</span>
						</div>
						<div>
							<span class="text-gray-500 block text-xs">Bedrooms</span>
							<span class="font-bold">3</span>
						</div>
						<div>
							<span class="text-gray-500 block text-xs">Bathroom</span>
							<span class="font-bold">1</span>
						</div>
					</div>
				</div>
				<div class="flex flex-col md:flex-row justify-between items-center gap-4">
					<a href="#" class="inline-flex items-center text-sm underline font-medium">
						<svg class="w-4 h-4 mr-1" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 18l6-6-6-6"/></svg>
						See the cost breakdown
					</a>
					<div class="font-bold text-xl">$335,000 incl. gst</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Footer -->
	<footer class="px-6 md:px-12 py-12 border-t border-gray-100 flex flex-col md:flex-row justify-between items-end gap-8 text-xs text-gray-500">
		<div class="space-y-1">
			<div>©2025</div>
			<div>The Living House New Zealand</div>
		</div>
		<div class="flex flex-wrap gap-8 text-black font-medium">
			<a href="#" class="hover:underline">About</a>
			<a href="#" class="hover:underline">FAQs</a>
			<a href="#" class="hover:underline">Download Brochure</a>
			<a href="#" class="hover:underline">Instagram</a>
			<a href="#" class="hover:underline">Contact</a>
		</div>
	</footer>
</div>

<style>
	/* Hide scrollbar for horizontal scrolling area */
	.scrollbar-hide::-webkit-scrollbar {
		display: none;
	}
	.scrollbar-hide {
		-ms-overflow-style: none;
		scrollbar-width: none;
	}
</style>


<script>

	import '../../../assets/global-styles.css';

	import Logo from '$lib/LogoBody.svelte';
	import TitleVideo from '$lib/TitleVideo.svelte';
    import TitlePage from '$lib/TitlePage.svelte';
	import AuthorDate from '$lib/AuthorDate.svelte';
	import ImageSingle from '$lib/ImageSingle.svelte';
	import GraphicSingle from '$lib/GraphicSingle.svelte';
	import GraphicsMultiples from '$lib/GraphicMultiples.svelte';
	import Footer from '$lib/Footer.svelte';
	import ScrollyImages from "$lib/ScrollyImages.svelte";
	import LineBreakMiniTransitMap from '$lib/LineBreakMiniTransitMap.svelte';
	import Password from '$lib/Password.svelte';
	import Recommendation from '$lib/Recommendation.svelte';
	import LogoBody from '$lib/LogoBody.svelte';
	
	import BoilerPlate from '$lib/BoilerPlate.svelte';

	import GraphicCompare from '$lib/GraphicCompare.svelte';
	
	import Footnote from '$lib/Footnote.svelte';
	import Footnotes from '$lib/Footnotes.svelte';
	import { createFootnoteStore } from '$lib/footnoteUtils';
    import HamburgerMenu from '$lib/HamburgerMenu.svelte';

	const footnoteStore = createFootnoteStore();
	const { footnotes, addFootnote } = footnoteStore;

	const fns = [
		'Projections from the Ontario Ministry of Finance, “Population projections,” August 1, 2025, <a href="https://data.ontario.ca/dataset/population-projections" target="_blank">URL</a>. ',
		'See also Clara Turner et al., Land Use Planning to Mitigate Climate Change in the Greater Golden Horseshoe: An Analysis of Potential Scenarios (Institute on Municipal Finance and Governance, 2024), <a href="https://utoronto.scholaris.ca/server/api/core/bitstreams/972d111e-8f09-46d7-89d5-57ec3b69f0e1/content" target="_blank">URL</a>. ',
		'The availability of free or low-cost parking has also been linked with higher rates of car ownership and driving around transit stations. See for example Michael Manville, “Bundled Parking and Vehicle Ownership: Evidence from the American Housing Survey,” Journal of Transport and Land Use 10, no. 1 (2017), <a href="https://doi.org/10.5198/jtlu.2016.730" target="_blank">DOI</a>; Daniel G. Chatman, “Does TOD Need the T?: On the Importance of Factors Other Than Rail Access,” Journal of the American Planning Association 79, no. 1 (2013): 17–31, <a href="https://doi.org/10.1080/01944363.2013.791008" target="_blank">DOI</a>. '
	];

	const credits = [
		{ role:"Research", names:"Emily Farrar, Hoda Touma, Shoshanna Saxe, Marianne Hatzopoulou"},
		{ role:"Additional writing", names:"Anika Reisha Taboy, Kathryn Exon Smith"},
		{ role:"Data visualization", names:"Jeff Allen, Mia Wang"},
		{ role:"Web development", names:"Mieko Yao, Jeff Allen"}
	]

</script>


<svelte:head>

	<title>TOD - Decarbonization | School of Cities</title>

	<meta name="description" content="Decarbonizing Transport through Land Use and Policy Change" />
	<meta name="author" content="School of Cities">
	<meta rel="canonical" href="https://schoolofcities.github.io/tod-canada/research/decarbonization">

	<meta property="og:title" content="TOD - Decarbonization" />
	<meta property="og:description" content="Decarbonizing Transport through Land Use and Policy Change" />
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://schoolofcities.github.io/tod-canada/research/decarbonization" />
	<meta property="og:image" content="https://raw.githubusercontent.com/schoolofcities/tod-canada/main/static/web-assets/research/decarbonization/thumbnail.png" />
	<meta property="og:locale" content="en_CA">

	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content="TOD - Decarbonization" />
	<meta name="twitter:description" content="Decarbonizing Transport through Land Use and Policy Change" />
	<meta name="twitter:site" content="https://schoolofcities.github.io/tod-canada/research/decarbonization" />
	<meta name="twitter:image" content="https://raw.githubusercontent.com/schoolofcities/tod-canada/main/static/web-assets/research/decarbonization/thumbnail.png" /> 

	<meta name="citation_title" content="TOD - Decarbonization">
	<meta name="citation_author" content="Emily Farrar">
	<meta name="citation_author" content="Marianne Hatzopoulou">
	<meta name="citation_author" content="Hoda Touma"> 
	<meta name="citation_publication_date" content="2026/04">
	<meta name="citation_journal_title" content="School of Cities">
	<!-- <meta name="citation_pdf_url" content="https://schoolofcities.utoronto.ca/research-paper.pdf"> -->
	<!-- <meta name="citation_abstract_html_url" content="https://schoolofcities.github.io/research/"> -->

</svelte:head>



<main>

	<Password correctPassword="meowmeowcat"></Password>

	<TitlePage
		title="Decarbonizing Transport through Land Use and Policy Change"
		type="Research"
		bgType="Video"
		url="/tod-canada/web-assets/research/decarbonization/decarbonization-title.mp4"
		videoSpeed={0.67}
		videoOpacity={0.8}
		titleFontColour="var(--brandWhite)"
		subtitleFontColour="var(--brandWhite)"
		logoType = 'White'
		secondLogo = 'PositiveZero'
	/>

	<HamburgerMenu pageType="research"/>

	<div class="caption-container" style="padding-left: 10px; overflow: hidden; margin-top: -5px; opacity: 0.65; max-width: 320px;">
		<p>
			<span class="caption-source">Video source: Storyblocks</span>
		</p>
	</div>

	<div class="text" style="margin-top: 80px">

		<AuthorDate
			credits={credits} date="March 2026"
		/>

	</div>

	

	<div class="text">
		<h1>
			The big picture  
		</h1>

		<p>
			In Canadian cities, travelling by car is still the dominant mode, and transportation is a major and rising source of greenhouse gas emissions. The way cities grow – sprawling out or densifying near existing transit – will determine the climate impacts of population growth. 
		</p>

		<p>
			ur research examines the potential for growth management strategies, particularly TOD, to lower passenger transport emissions. It asks whether directing growth to transit-rich areas meaningfully reduces vehicle travel and emissions, and whether TOD alone is sufficient or must be complemented by other policy measures.
		</p>

		<BoilerPlate pageType="Research"/>
		
		<h1>
			Methodology and approach
		</h1>

		<p>
			Our study uses the Greater Toronto and Hamilton Area (GTHA) as a case study of how different patterns of future housing growth could shape travel behaviour and transportation emissions by 2031. The GTHA is one of the fastest growing urban areas in Canada, with a projected regional population of 8.77 million by 2031, an increase of 1.7 million residents compared to 2016.<Footnote id={addFootnote(fns[0])}/>  Understanding what factors influence transportation emissions in this region has implications for cities across Canada. 
		</p>

	</div>

	<GraphicSingle
		svg1080={"../web-assets/research/decarbonization/pop-density-1080.svg"}
		svg720={"../web-assets/research/decarbonization/pop-density-720.svg"}
		svg360={"../web-assets/research/decarbonization/pop-density-360.svg"}
	/>

	<div class="text">

		<p>
			We developed a modelling framework that links population growth, travel demand, and greenhouse gas (GHG) emissions, which allowed us to evaluate a series of “what if?” urban densification strategies.  
		</p>

		<h2>
			Projecting where people live
		</h2>

		<p>
			We developed a model to look at how neighbourhoods have grown since 2016 and extend those patterns forward to 2031. We called this the “business-as-usual” (BAU) scenario: an estimate of how the population might continue to distribute itself across the region with no interventions. 
		</p>

		<p>
			We then created alternative scenarios that change where new residents are allowed or encouraged to settle. For example, one scenario placed more growth around major transit stations, while another directed growth toward already dense, central neighbourhoods. In each case, the total number of new residents remained the same; only the location of growth changed. 
		</p>

	</div>

	<GraphicCompare 
		images={[
			{
				svg1080: "../web-assets/research/decarbonization/growth-bau-1080.svg",
				svg720: "../web-assets/research/decarbonization/growth-bau-720.svg",
				svg360: "../web-assets/research/decarbonization/growth-bau-360.svg",
				caption: "",
				source: "",
				altText: "",
				buttonLabel: "Business as usual"
			},
			{
				svg1080: "../web-assets/research/decarbonization/growth-s1-1080.svg",
				svg720: "../web-assets/research/decarbonization/growth-s1-720.svg",
				svg360: "../web-assets/research/decarbonization/growth-s1-360.svg",
				caption: "",
				source: "",
				altText: "",
				buttonLabel: "Scenario 1: Sprawl"
			},
			{
				svg1080: "../web-assets/research/decarbonization/growth-s2-1080.svg",
				svg720: "../web-assets/research/decarbonization/growth-s2-720.svg",
				svg360: "../web-assets/research/decarbonization/growth-s2-360.svg",
				caption: "",
				source: "",
				altText: "",
				buttonLabel: "Scenario 2: Infill"
			},
			{
				svg1080: "../web-assets/research/decarbonization/growth-s3-1080.svg",
				svg720: "../web-assets/research/decarbonization/growth-s3-720.svg",
				svg360: "../web-assets/research/decarbonization/growth-s3-360.svg",
				caption: "",
				source: "",
				altText: "",
				buttonLabel: "Scenario 3: TOD 800m"
			},
			{
				svg1080: "../web-assets/research/decarbonization/growth-s4-1080.svg",
				svg720: "../web-assets/research/decarbonization/growth-s4-720.svg",
				svg360: "../web-assets/research/decarbonization/growth-s4-360.svg",
				caption: "",
				source: "",
				altText: "",
				buttonLabel: "Scenario 4: TOD 500m"
			},
			{
				svg1080: "../web-assets/research/decarbonization/growth-s5-1080.svg",
				svg720: "../web-assets/research/decarbonization/growth-s5-720.svg",
				svg360: "../web-assets/research/decarbonization/growth-s5-360.svg",
				caption: "",
				source: "",
				altText: "",
				buttonLabel: "Scenario 5: TOD 500m DT"
			},
			{
				svg1080: "../web-assets/research/decarbonization/growth-s6-1080.svg",
				svg720: "../web-assets/research/decarbonization/growth-s6-720.svg",
				svg360: "../web-assets/research/decarbonization/growth-s6-360.svg",
				caption: "",
				source: "",
				altText: "",
				buttonLabel: "Scenario 6: High density growth"
			}
		]}
	/>

	<div class="text">

		<p>
			Finally, we modelled the effect of combining dense development with policies that limit vehicle ownership, either for new or existing residents. While the geographic scenarios focus on the effects of densification, this part of the analysis examines hypothetical scenarios: how overall outcomes might change if policy measures were introduced to encourage lower car dependence.  
		</p>

		<h2>
			Modelling daily travel across the region 
		</h2>

		<p>
			Once we had a map of where people would live in each scenario, we estimated how these choices would affect travel. 
		</p>

		<p>
			For this, we used the <a href="https://tmg.utoronto.ca/doc/1.6/gtamodel/index.html" target="_blank">GTAModel</a> developed by the University of Toronto’s <a href="https://tmg.utoronto.ca/doc/1.6/gtamodel/index.html" target="_blank">Travel Modelling Group</a>. It is an activity-based travel model that simulates daily schedules for every person in the region (e.g. for school, work, errands, etc.) and converts those activities into trips by car, transit, walking, or cycling. These trips are then assigned to the region’s road and transit networks so we can see how travel speeds and mode change based on where people settle within the region. For future years, we included major transit lines already under construction (such as the Ontario Line) so the model reflects the network expected to be in place by 2031.  
		</p>

		<h2>
			Estimating transportation emissions 
		</h2>

		<p>
			To understand the GHG implications of the scenarios, we calculated GHG emissions from both passenger vehicles and buses. We combined travel model outputs with emissions data from the US Environmental Protection Agency <a href="https://www.epa.gov/moves/latest-version-motor-vehicle-emission-simulator-moves" target="_blank">MOVES model</a> to estimate how much carbon is emitted on each road segment in each scenario.  
		</p>

		<p>
			<a href="../web-assets/research/decarbonization/TOD and Decarbonization - Full Methodology and Findings.pdf" target="_blank">Click here for a more detailed discussion of the methodology. </a>
		</p>

		<h1>
			What we found
		</h1>

		<p>
			Comparing the 2016 baseline with BAU growth and optimized scenarios reveals substantial variation in travel behaviour and GHG emissions. While land use patterns matter, the results consistently show that growth management alone is insufficient to offset the transportation impacts of rapid population growth without corresponding transportation system changes.  
		</p>

		<h2>
			Densification does not automatically lead to lower emissions – but it helps 
		</h2>

		<p>
			Daily regional transportation emissions vary widely across scenarios. The 2016 baseline produces roughly 28,300 metric tons of CO2 per day, which increases to over 35,000 metric tons per day under the 2031 BAU scenario. All of the denser development patterns result in lower emissions than the BAU scenario, but still substantially higher than 2016 levels. Development in a sprawl pattern results in the worst outcomes, with emissions growing at a much faster pace than the population, highlighting the risk associated with dispersed, auto-oriented growth.<Footnote id={addFootnote(fns[1])}/> 
		</p>

	</div>

	<GraphicSingle
		svg720={"../web-assets/research/decarbonization/ghg-land-use-total-720.svg"}
		svg360={"../web-assets/research/decarbonization/ghg-land-use-total-360.svg"}
	/>

	<div class="text">

		<h2>
			High-quality transit matters more than transit proximity 
		</h2>

		<p>
			Our analysis reveals a sobering reality: all future growth scenarios led to worse outcomes for transit users compared to the 2016 baseline, with average trip times increasing regardless of where new residents settled. This happened because transit infrastructure saw little expansion under our scenarios – only the addition of the Ontario Line, Eglinton Crosstown, and Finch LRT – while the region added approximately 1.1M new residents.  
		</p>

		<p>
			When transit is overcrowded and slow, people will drive even if they live next to a subway station. This finding fundamentally shapes everything else. Across most scenarios, regional mode share remained surprisingly stable. BAU and TOD scenarios exhibit similar rates of driving, transit use, and walking, typically differing by only two to three percentage points. Even when new residents move right next to transit stations in walkable neighbourhoods, the overcrowded transit system cannot deliver competitive travel times compared to driving. As a result, even under TOD growth, most residents still chose to drive, concentrating congestion and emissions in the downtown core.<Footnote id={addFootnote(fns[2])}/>  
		</p>

		<h2>
			Substantially lowering emissions requires limiting vehicle ownership 
		</h2>

		<p>
			Growth management alone, without complementary policies, cannot deliver absolute emission reductions in a growing region. The only way to lower emissions below the 2016 baseline is a combination of high-density growth, zero car ownership among new residents, and electrification of the bus fleet. 
		</p>

	</div>

	<GraphicSingle
		svg720={"../web-assets/research/decarbonization/mode-share-scenario-720.svg"}
		svg360={"../web-assets/research/decarbonization/mode-share-scenario-360.svg"}
	/>

	<div class="text">

		<p>
			The only scenarios that achieved substantial mode shift (a 10%+ reduction in driving) were those in which we artificially prevented new residents from owning cars or went further and prevented the entire population from acquiring additional vehicles. Under these scenarios, people shifted to walking, transit, carpooling, and ride-hailing services. Without these constraints, TOD alone did not meaningfully reduce auto reliance at the regional scale.  
		</p>

		<p>
			<a href="../web-assets/research/decarbonization/TOD and Decarbonization - Full Methodology and Findings.pdf" target="_blank">See the full analysis here.</a>
		</p>
		
		<h1>
			Key conclusions and policy recommendations 
		</h1>

		<p>
			While concentrating growth near transit reduces emissions relative to sprawl, outcomes depend more on transit service quality, network capacity, and vehicle ownership patterns than on proximity to stations alone. When transit becomes overcrowded or slow, auto use persists even in highly transit-accessible locations.     
		</p>

		<p>
			Our findings highlight that meaningful transportation decarbonization requires coordinated action across land use, transportation investment, and vehicle policy. Compact growth can reduce emissions intensity, but absolute reductions depend on coordinated systems and incentives.  
		</p>

		<div class="quote" style="padding-top: 30px; padding-bottom: 20px;">
			<p>
				TOD can support lower-emissions travel, but only when land use, transit investment, vehicle policy, and vehicle technology are aligned. 
			</p>
		</div>

		<Recommendation count=1 title="Increase transit investment before or alongside densification "/>

		<p>
			TOD or other densification strategies must be paired with early and sustained investment in transit infrastructure and operations. This includes expanding service frequency, improving reliability, increasing vehicle and station capacity, and accelerating the electrification of bus fleets. Without these investments, population growth risks degrading transit performance, reducing its competitiveness with driving, and undermining the emissions benefits of TOD. 
		</p>

		<Recommendation count=2 title="Integrate demand management with land use planning"/>

		<p>
			Land use planning should be reinforced with demand management tools that reduce the convenience and attractiveness of driving. Parking maximums, congestion pricing, and curb space reallocation can discourage car use, while investments in walking, cycling, and shared mobility networks improve first- and last-mile access to transit. These measures can help translate compact urban form into sustained mode shift.  
		</p>

		<Recommendation count=3 title="Reduce car ownership and decarbonize travel "/>

		<p>
			Limiting vehicle ownership is critical to achieving large reductions in driving, particularly in transit-rich areas. Policies that increase the cost of owning and operating vehicles can help shift household decisions away from car ownership. Such measures should be paired with strategies that accelerate the transition to zero-emission vehicles. Even with strong TOD and transit investment, cleaner vehicles remain essential to reducing emissions from trips that cannot be shifted to sustainable modes.  
		</p>	
		
	</div>


	<div class="text">

		<div class="line-break"></div>

	</div>

	<Footnotes footnotes={footnotes} />

	<div class="text">
		<div class="line-break"></div>
		<LogoBody/>
		<div class="line-break"></div>
	</div>



</main>

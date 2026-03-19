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

	const footnoteStore = createFootnoteStore();
	const { footnotes, addFootnote } = footnoteStore;

	const fns = [
		'Karen Chapple and Anastasia Loukaitou-Sideris, Transit-oriented displacement or community dividends?: Understanding the effects of smarter growth on communities (MIT Press, 2019).',
		'Peter Marcuse, “Gentrification, abandonment, and displacement: Connections, causes, and policy responses in New York City,” in Washington University Journal of Urban & Contemporary Law 28 (1985), 195.',
		'More than 70 stations opened during this time period, but a few stations were not included in our analysis because data were unavailable.',
		'Statistics Canada, “Longitudinal Administrative Databank (LAD),” 2025, <a href="https://www23.statcan.gc.ca/imdb/p2SV.pl?Function=getSurvey&SDDS=4107" target="_blank">URL</a>. At the time of writing, 2022 were the most recent data available.'
	];

	const credits = [
		{ role:"Research", names:"Jeff Allen, Karen Chapple, Amir Forouhar "},
		{ role:"Additional writing", names:"Kathryn Exon Smith, Anika Reisha Taboy"},
		{ role:"Data visualization", names:"Isabeaux Graham"},
		{ role:"Web development", names:"Mieko Yao, Jeff Allen"}
	]

</script>



<svelte:head>

	<title>TOD - Displacement | School of Cities</title>

	<!-- <meta name="description" content="Repository of design and web components for building data stories, visualizations, maps, and other custom web projects" />
	<meta name="author" content="School of Cities">
	<meta rel="canonical" href="https://schoolofcities.github.io/design-components/">

	<meta property="og:title" content="Design Components" />
	<meta property="og:description" content="Repository of design and web components for building data stories, visualizations, maps, and other custom web projects" />
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://schoolofcities.github.io/design-components/" />
	<meta property="og:image" content="https://raw.githubusercontent.com/schoolofcities/design-components/main/static/web-card.png" />
	<meta property="og:locale" content="en_CA">

	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content="Design Components" />
	<meta name="twitter:description" content="Repository of design and web components for building data stories, visualizations, maps, and other custom web projects" />
	<meta name="twitter:site" content="https://schoolofcities.github.io/design-components/" />
	<meta name="twitter:image" content="https://raw.githubusercontent.com/schoolofcities/design-components/main/static/web-card.png" /> 

	<meta name="citation_title" content="Design Components">
	<meta name="citation_author" content="Author Name 1">
	<meta name="citation_author" content="Author Name 2">
	<meta name="citation_author" content="Author Name 3"> -->
	<meta name="citation_publication_date" content="2025/09/23">
	<meta name="citation_journal_title" content="School of Cities">
	<!-- <meta name="citation_pdf_url" content="https://schoolofcities.utoronto.ca/research-paper.pdf"> -->
	<!-- <meta name="citation_abstract_html_url" content="https://schoolofcities.github.io/design-components/"> -->

</svelte:head>



<main>

	<Password correctPassword="meowmeowcat"></Password>

	<!-- <TitleVideo
		title="Embodied Carbon in Different Development Patterns and Built Forms "
		subtitle=""
		titletype="RESEARCH"
		video="/tod-canada/research/embodied-carbon/skylineVideo.mp4"
		videoSpeed={0.67}
		videoOpacity={0.8}
		titleFontColour="var(--brandWhite)"
		subtitleFontColour="var(--brandWhite)"
		logoType = 'White';
	/> -->
	<TitlePage
		title="Past and Projected Transit-Induced Displacement in Canada "
		type="Research"
		bgType="Video"
		url="/tod-canada/web-assets/research/embodied-carbon/toronto-contruction-4k-SBV-302197434-HD.mp4"
		videoSpeed={0.67}
		videoOpacity={0.8}
		titleFontColour="var(--brandWhite)"
		subtitleFontColour="var(--brandWhite)"
		logoType = 'White';
	/>

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
			Many new transit stations are located in neighbourhoods that have concentrations of lower-income residents<Footnote id={addFootnote(fns[0])}/>￼ New transit lines can improve mobility and accessibility to destinations while lowering greenhouse gas emissions, particularly when paired with the intensification of land surrounding station areas. However, these accessibility improvements can have unintended consequences if rising rents and housing values force the most vulnerable residents to leave. This study examines patterns of residential displacement and exclusion following the opening of new transit stations in Canadian cities, with a focus on impacts on low-income residents. 
		</p>

		<BoilerPlate pageType="Research"/>
		
		<h1>
			Methodology and approach
		</h1>

		<p>
			Residential displacement is a situation in which current residents are forced out of neighbourhoods or have fewer options within them. 
		</p>
		<p>
			This may be <span style="border-bottom: 4px solid var(--brandYellow); font-family: InterBold">direct displacement</span> (when housing is demolished for new transit construction), but is most often  <span style="border-bottom: 4px solid var(--brandYellow); font-family: InterBold">indirect displacement</span>, when property prices and rents increase without policy protections. Along with these, researchers also consider  <span style="border-bottom: 4px solid var(--brandRed); font-family: InterBold">exclusionary displacement</span>, when new residents are unable to move into neighbourhoods because of price increases or a lack of suitable housing stock.<Footnote id={addFootnote(fns[1])}/> 
		</p>
		<p>
			To measure displacement around transit stations, first we identified every major rail transit station that opened in Canada between 1990 and 2016, including subway/metro, light rail, and regional rail. For these 70 station areas, we used historical census data to understand how many and what types of dwellings were built within 800 metres of the station over a 10-year period, the five years before and after the stations opened.<Footnote id={addFootnote(fns[2])}/> 
		</p>

		<h2>
			Historical analysis
		</h2>
		
		<p>
			We used the Longitudinal Administrative Databank (LAD) to track how many low-income residents moved in and out of transit station areas. The LAD is a 20% annual sample dataset of tax filers across Canada and includes the postal code of each household alongside tax-filing information<Footnote id={addFootnote(fns[3])}/> We mapped changes in postal codes to analyze whether residents moved in or out of station areas over the 10-year period, and compared these moving rates with moving rates in each station’s Census Metropolitan Area (CMA) for the same period. Since our analysis focuses on low-income residents, we used the Low-Income Measure variable within the LAD dataset to measure the movements of this population.  
		</p>

		<p>
			We used this historical data to create a statistical model that estimates the likelihood of residents to move away from a transit station area based on their individual demographic and socioeconomic characteristics as well as changes in the built environment changes (e.g. building mixed-use developments or a larger number of 2- and 3-bedroom units). 
		</p>

		<h2>
			Case study scenario analysis
		</h2>

		<p>
			We applied our statistical model to 15 hypothetical scenarios across the five TOD case study areas we identified for this project (Cooksville, Northfield, Arbutus, McKernan-Belgravia, and Panama) to measure the potential impact on low-income resident mobility. For each case we examined what would occur with: 

		</p>

		<ul>
			<li>No new development </li>
			<li>The current development trajectory</li>
			<li>Optimized development of complete communities </li>
		</ul>

		<p>
			Click here for a more detailed discussion of the methodology. 
		</p>

		<h1>
			What we found
		</h1>

		<p>
			Studying the movements of low-income residents allowed us to draw some broad conclusions about station areas across the country. If low-income residents moved out of station areas at above-average rates, this signalled displacement. If they moved out at similar or below-average rates, this indicated that the area was remaining relatively affordable. We determined the relative inclusivity or exclusivity of new station areas by measuring the rates of low-income residents moving in. We found a consistent overall pattern of heightened displacement and reduced in-migration over the 1990-2016 period. These trends persisted in our forward-looking scenario analysis of case study station areas. 
		</p>

		<h2>
			Lower-income residents are more likely to leave new station areas 
		</h2>

	</div>

	<GraphicSingle
		svg720={"../web-assets/research/displacement/total-move-away720.svg"}
		svg360={"../web-assets/research/displacement/total-move-away-360.svg"}
	/>

	<div class="text">

		<p>
			Between 1990 and 2016, low-income residents were about 10% more likely to leave neighbourhoods with a new transit station than comparable areas in the same CMA without one. This trend has increased in recent years (since 2010) and is more pronounced in areas with new subway stations versus LRT or regional rail.
		</p>

	</div>

	<GraphicSingle
		svg720={"../web-assets/research/displacement/move-away-chart720.svg"}
		svg360={"../web-assets/research/displacement/move-away-chart360.svg"}
	/>

	<div class="text">

		<p>
			Via multivariate models, income was by far the most important predictor of moving out of a station area. Other demographic variables like age, gender, and family composition all showed more minor effects. 
		</p>

		<h2>
			New station areas are more exclusive than other neighbourhoods 
		</h2>

	</div>

	<GraphicSingle
		svg720={"../web-assets/research/displacement/total-move-in720.svg"}
		svg360={"../web-assets/research/displacement/total-move-in-360.svg"}
	/>

	<div class="text">

		<p>
			Where new stations have opened, the residents who move into the station area are about 15% less likely to be low-income compared with those relocating to other parts of the CMA. This was particularly true in the major cities of Montreal, Vancouver, and Toronto, where much of the new housing built near transit stations since 2000 has been owner-occupied condominiums, which are generally less accessible to lower-income households. In contrast, there were more low-income in-movers near LRT stations, possibly because these have less of an impact on land values and housing prices, at least in the context of Edmonton and Calgary. More recent station openings have also attracted more low-income households, at rates comparable to the rest of the CMA. This may be tied to local market conditions or may be a positive effect of more inclusive housing policies in these areas. 
		</p>

	</div>

	<GraphicSingle
		svg720={"../web-assets/research/displacement/move-in-chart720.svg"}
		svg360={"../web-assets/research/displacement/move-away-chart360.svg"}
	/>

	<div class="text">

		<h2>
			All new development in case study station areas is associated with displacement – but mixed-use areas fare better 
		</h2>

		<p>
			Across the five case studies, development was associated with higher levels of displacement for low-income households than for other residents – regardless of what type of dwellings were built (number of bedrooms, number of stories, etc.). More significant policy interventions are required to ensure these areas remain affordable so households can stay in place.  
		</p>

		<p>
			In our simulated scenarios, low-income households were about 5% more likely to move away than residents who were not low-income. Turnover of the low-income population ranged between 7% and 9% per year in these areas. The “optimized” scenarios, which in each case included more intentional mixed-use development and a greater mix of dwelling types, resulted in less out-migration of low-income households. However, nearly all cases showed more displacement from new development, indicating that policies must explicitly address displacement risk in these areas. 
		</p>

		<h1>
			Key conclusions and policy recommendations 
		</h1>

		<p>
			We find that, on average, when new transit stations open in Canada, low-income residents are more likely to be displaced and station areas tend to become more exclusive than before. While these outcomes vary by city and by transit system type, a consistent national pattern emerges: low-income residents are 10% more likely to move out of station areas, and 15% less likely to move in. Mixed-use development shows some potential to temper these effects, but policy intervention is needed in addition to changes in built form.   
		</p>

		<Recommendation count=1 title="Support a greater variety of building types and unit sizes to mitigate displacement impacts"/>

		<p>
			Integrating a greater mix of uses and dwelling types within station areas, as in the optimized case study scenarios, was linked with lower out-migration of low-income households. Ensuring residents have options at varying sizes, numbers of bedrooms, and affordability levels can allow them to stay within the area, and present options to a greater number of potential in-movers. 
		</p>

		<Recommendation count=2 title="Use policy interventions to protect and preserve affordable housing"/>

		<p>
			While diversifying development is helpful, municipalities must establish intentional policy interventions to prevent displacement from station areas. These include efforts to preserve existing affordable housing and to require, incentivize, or directly support the construction of new affordable units within station areas. Without these interventions, new development near transit is likely to continue contributing to displacement, even in mixed-use contexts.  
		</p>

		<Recommendation count=3 title="Prioritize purpose-built rental developments near transit stations"/>

		<p>
			In addition to policy protections, municipalities should guide the type of housing delivered in station areas. Favouring purpose-built rental over condominium development can provide more stable, long-term housing options for low- and moderate-income households. Condominiums are more likely to drive price increases and limit access for lower-income residents. 
		</p>	
		
		<!-- <div class="quote" style="padding-top: 70px;">
			<p>
				Design choices can reduce the embodied GHG in a building by 50% or more.  
			</p>
		</div> -->
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

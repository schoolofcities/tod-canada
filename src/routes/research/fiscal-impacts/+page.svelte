<script>

	import '../../../assets/global-styles.css';
	import { display } from "mathlifier";

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
	
	import Footnote from '$lib/Footnote.svelte';
	import Footnotes from '$lib/Footnotes.svelte';
	import { createFootnoteStore } from '$lib/footnoteUtils';
    import HamburgerMenu from '$lib/HamburgerMenu.svelte';
    import GraphicMultiples from '$lib/GraphicMultiples.svelte';

	const footnoteStore = createFootnoteStore();
	const { footnotes, addFootnote } = footnoteStore;

	const fns = [
		'Karen Chapple and Anastasia Loukaitou-Sideris, <i>Transit-oriented displacement or community dividends?: Understanding the effects of smarter growth on communities</i> (MIT Press, 2019).',
		'Peter Marcuse, “Gentrification, abandonment, and displacement: Connections, causes, and policy responses in New York City,” in Washington University Journal of Urban & Contemporary Law 28 (1985), 195.',
		'More than 70 stations opened during this time period, but a few stations were not included in our analysis because data were unavailable.',
		'Statistics Canada, “Longitudinal Administrative Databank (LAD),” 2025, <a href="https://www23.statcan.gc.ca/imdb/p2SV.pl?Function=getSurvey&SDDS=4107" target="_blank">URL</a>. At the time of writing, 2022 were the most recent data available.'
	];

	const credits = [
		{ role:"Research", names:"Alex Hempel"},
		{ role:"Additional writing", names:"Kathryn Exon Smith"},
		{ role:"Data visualization", names:"Jeff Allen"},
		{ role:"Web development", names:"Mieko Yao, Jeff Allen"},
		{ role:"Additional contributors", names:"An Pham, Anika Reisha Taboy"}
	]

</script>



<svelte:head>

	<title>TOD - Fiscal Impacts | School of Cities</title>

	<meta name="description" content="Fiscal Impacts of Transit-Oriented Development" />
	<meta name="author" content="School of Cities">
	<meta rel="canonical" href="https://schoolofcities.github.io/tod-canada/research/fiscal-impacts">

	<meta property="og:title" content="TOD - Fiscal Impacts" />
	<meta property="og:description" content="Fiscal Impacts of Transit-Oriented Development" />
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://schoolofcities.github.io/tod-canada/research/fiscal-impacts" />
	<meta property="og:image" content="https://raw.githubusercontent.com/schoolofcities/tod-canada/main/static/web-assets/research/fiscal-impacts/thumbnail.png" />
	<meta property="og:locale" content="en_CA">

	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content="TOD - Fiscal Impacts" />
	<meta name="twitter:description" content="Fiscal Impacts of Transit-Oriented Development" />
	<meta name="twitter:site" content="https://schoolofcities.github.io/tod-canada/research/fiscal-impacts" />
	<meta name="twitter:image" content="https://raw.githubusercontent.com/schoolofcities/tod-canada/main/static/web-assets/research/fiscal-impacts/thumbnail.png" /> 

	<meta name="citation_title" content="TOD - Fiscal Impacts">
	<meta name="citation_author" content="Alex Hempel">
	<meta name="citation_publication_date" content="2026/04">
	<meta name="citation_journal_title" content="School of Cities">
	<!-- <meta name="citation_pdf_url" content="https://schoolofcities.utoronto.ca/research-paper.pdf"> -->
	<!-- <meta name="citation_abstract_html_url" content="https://schoolofcities.github.io/design-components/"> -->

</svelte:head>



<main>

	<Password correctPassword="meowmeowcat"></Password>

	<TitlePage
		title="Fiscal Impacts of Transit-Oriented Development"
		type="Research"
		bgType="Video"
		url="/tod-canada/web-assets/research/fiscal-impacts/skytrain-high-rise.mp4"
		videoSpeed={0.67}
		videoOpacity={0.8}
		titleFontColour="var(--brandWhite)"
		subtitleFontColour="var(--brandWhite)"
		logoType = 'White';
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
			Municipal governments often face uncertainty about the fiscal impacts of large development projects, particularly transit-oriented development (TOD). While new development expands the property tax base and generates development-related revenues, it also requires additional infrastructure investment and municipal services.  
		</p>

		<p>
			This research evaluates the fiscal impacts of development across five case study station areas in Canadian municipalities: Arbutus (Vancouver), Cooksville (Mississauga), McKernan-Belgravia (Edmonton), Northfield (Waterloo), and Panama (Brossard). The station areas represent a range of TOD typologies, from moderate densification of existing neighbourhoods to large-scale development of underutilized land. Within each station area, we evaluate scenarios that vary the scale of development, unit sizes, and infrastructure investments.  
		</p>

		<p>
			The objective of our analysis is to estimate whether these developments generate net revenues or costs for municipal governments.  
		</p>

		<BoilerPlate pageType="Research"/>

		<h1>
			Methodology and approach  
		</h1>

		<p>
			Municipal fiscal impacts can be divided into two broad categories: capital impacts and operating impacts. 
		</p>

		<ul>
			<li>
				    <strong>Capital impacts</strong> reflect the up-front infrastructure required to support development. These costs may include investments in schools, community centres, libraries, and other public facilities. Municipalities typically finance these investments in part through development charges (DCs) and related fees paid by developers, and in part through government transfers and accumulated reserves. 
			</li>
			<li>
				   	<strong>Operating impacts</strong> reflect the ongoing revenues and costs associated with serving new residents. Revenues primarily come from property taxes and municipal service fees, while costs include the operating expenditures required to maintain municipal services such as transportation, policing, parks, and administration.  
			</li>
		</ul>

		<p>
			Because capital costs occur once, while operating revenues occur annually, this analysis converts capital impacts into annualized equivalents by depreciating them over a 40-year period. This allows us to compare capital and operating impacts on a consistent basis.  
		</p>

		<!-- This was rendering weirdly for me, and I couldn't fix, so just made a quick image -->
		<!-- {@html display(`Net~Total~Annual~Impact = Net~Operating~Impact + \\frac{Net~Capital~Impact}{Time~Horizon}`)} -->

		</div>

		<GraphicSingle
			svg720={"../web-assets/research/fiscal-impacts/formula-720.svg"}
			svg360={"../web-assets/research/fiscal-impacts/formula-360.svg"}
		/>

		<div class="text">

		<p>
			The analysis also illustrates how these fiscal impacts could evolve over time on a cash basis. We determined each municipality’s construction capacity by using CMHC’s Starts and Completions survey, a ten-year average of housing starts, and modelled two speeds of construction. In the faster version, we assume the construction capacity is equal to the historical averages. In the slower version, since construction activity would likely not be entirely dedicated to the proposed TODs in each municipality, we assumed that the construction capacity is half the average. This allows us to project a timeline of financial impacts that takes into account both the scale of development in each station area and the likely speed of construction. This approach considers only the fiscal impact of development within the station area and does not take into account development that would have occurred in the absence of the TOD (which would have had its own fiscal costs and benefits), or the fiscal outcomes of TOD versus more dispersed growth.
		</p>

		<p>
			<a href="../web-assets/research/fiscal-impacts/Fiscal Impacts - Full methodology and findings.pdf" target="_blank">Click here for a more detailed discussion of the methodology.</a>
		</p>

		<h1>
			What we found 
		</h1>

		<p>
			Our findings show that TOD generally generates positive long-term fiscal impacts, though upfront capital costs, development charge frameworks, and construction timing can create short-term pressures. 
		</p>

		<h2>
			Most TOD scenarios generate positive operating fiscal impacts
		</h2>

		<p>
			The net impact of the new TOD across most cases is positive – sometimes very positive. Once fully built out, many of the proposed developments generate more annual revenue than they cost municipalities in operating expenditures. One reason is that new housing units tend to have higher property values than older housing,<Footnote id={addFootnote(fns[0])}/> which results in above-average property tax revenue relative to the cost of municipal services. However, results vary across municipalities and depend on local property values, tax rates, and municipal expenditures per capita. There may also be additional benefits to capital expenditures, such as schools or community centres drawing from beyond the TOD, which are not accounted for here.
		</p>

		<p>
			In almost all cases, the optimized scenarios generated higher operating revenues than the current trajectory, indicating that TODs that balance housing needs with the infrastructure and services that make complete communities make fiscal sense. In the case where municipal revenues are lower (Northfield), the optimized case has less property tax from commercial space and more infrastructure to maintain (including roads and community facilities) – but the increase in jobs may generate more revenues for other orders of government in the form of income tax. The negative impact in the current trajectory for Edmonton is caused by the anticipated lower-than-average assessment values (and therefore lower property tax revenues) of small infill units combined with the city’s relatively high average municipal spending per person to maintain its current sprawling footprint.
		</p>
	</div>

	<GraphicMultiples 
		svgPaths={[
			"../web-assets/research/fiscal-impacts/net-revenue-360.svg",
			"../web-assets/research/fiscal-impacts/net-capital-costs-360.svg"
		]}/>

	<!-- <GraphicSingle
		svg720={"../web-assets/research/fiscal-impacts/net-revenue-720.svg"}
		svg360={"../web-assets/research/fiscal-impacts/net-revenue-360.svg"}
	/>

	<GraphicSingle
		svg720={"../web-assets/research/fiscal-impacts/net-capital-costs-720.svg"}
		svg360={"../web-assets/research/fiscal-impacts/net-capital-costs-360.svg"}
	/> -->

	<GraphicSingle
		svg720={"../web-assets/research/fiscal-impacts/net-total-720.svg"}
		svg360={"../web-assets/research/fiscal-impacts/net-total-360.svg"}
	/>

	<div class="text">

		<h2>
			Capital costs vary widely across municipalities 
		</h2>

		<p>
			While operating impacts are generally positive, capital impacts differ substantially depending on the level of infrastructure required. In some station areas, development charge revenues exceed the estimated infrastructure costs, generating a positive capital balance for municipalities. In other cases, infrastructure investments exceed development charge revenues, resulting in a capital shortfall.  
		</p>

		<p>
			These differences are driven by both the scale and design of the TOD and institutional differences in development charge systems across provinces. Provinces such as Ontario and British Columbia have relatively high development charges on new construction, which generate significant municipal revenue. Municipalities in other provinces, including in Alberta and Quebec, rely much less on development charge revenue and instead depend more heavily on property tax revenues. In addition, projects in areas with ample existing infrastructure require less capital investment than those located in relatively underdeveloped areas.  
		</p>

	</div>

	<GraphicSingle
		svg720={"../web-assets/research/fiscal-impacts/summary-table-720.svg"}
		svg360={"../web-assets/research/fiscal-impacts/summary-table-360.svg"}
	/>

	<GraphicSingle
		svg720={"../web-assets/research/fiscal-impacts/dc-revenue-720.svg"}
		svg360={"../web-assets/research/fiscal-impacts/dc-revenue-360.svg"}
	/>

	<div class="text">
		<h2>
			Timing of cost and revenue impacts may be misaligned  
		</h2>

		<p>
			Municipal budgets must balance on a cash basis, which can lead to jumps in a single year when a project is committed to. Provincial accounting standards, in contrast, require accrual-based reporting, which spreads out the budget impact as the asset depreciates over time. On a cash basis, some scenarios are initially cash-flow negative when large upfront capital costs are not fully covered by development charge revenues. This represents a trade-off, as reducing development charges may encourage more development but municipalities need to find a way to cover these upfront costs where anticipated property tax revenues are lower. In these cases, municipalities may need to draw on reserve funds or seek additional support from provincial or federal governments to cover the shortfall. Nearly all scenarios become cash-flow positive in the medium term.  
		</p>

		<p>
			On an accrual basis, nearly all TOD scenarios generate a positive net fiscal impact, although some are close to breaking even. Station areas in British Columbia and Ontario, where fiscal impacts are generally more positive, generate between $40 million and $100 million in accrued net revenue each year. The developments in Alberta and Quebec produce much smaller impacts, both in total and on a per-unit basis. This suggests that the fiscal impact of TODs depends strongly on the local institutional and market context.  
		</p>

		<h2>
			Construction capacity strongly affects municipal finance dynamics  
		</h2>

		<p>
			Construction capacity varies significantly across municipalities in these scenarios, which affects the timing of fiscal impacts. Historical housing start data indicate that some municipalities are capable of building new housing at much faster rates than others. Based on these historical construction rates, we developed projected timelines to build out each TOD scenario, which showed substantial variation across locations.  
		</p>

	</div>

	<GraphicSingle
		svg720={"../web-assets/research/fiscal-impacts/development-speed-720.svg"}
		svg360={"../web-assets/research/fiscal-impacts/development-speed-360.svg"}
	/>

	<div class="text">

		<p>
			These timelines demonstrate that construction capacity can significantly affect how quickly municipalities benefit from TOD, particularly when infrastructure investments occur upfront. Developments that are net-positive on the capital budget can generate immediate fiscal benefits, while those that are net-negative may initially create cash-flow pressures. Faster rates of construction also mean that the full fiscal benefits of development are realized sooner. 
		</p>

		<p>
			Another interpretation of this is that it may simply take longer to realize full development of these scenarios – potentially decades. In Mississauga’s case, for example, a full build out of the proposed infrastructure and dwelling units proposed in the Cooksville TOD would take 10-25 years, without additional efforts to speed up construction. This can lead to a disconnect in timing between when the capital investments are paid for and when the development charge revenue is received.  
		</p>
	</div>

	<GraphicSingle
		svg720={"../web-assets/research/fiscal-impacts/annual-revenue-720.svg"}
		svg360={"../web-assets/research/fiscal-impacts/annual-revenue-360.svg"}
	/>

	<div class="text">
		<p>
			<a href="../web-assets/research/fiscal-impacts/Fiscal Impacts - Full methodology and findings.pdf" target="_blank">See the full analysis here.</a>
		</p>
	</div>

	<!-- graph -->

	<div class="text">
		<h1>
			Key conclusions and policy recommendations 
		</h1>

		<p>
			Overall, the analysis suggests that TODs can generate positive fiscal outcomes for municipalities. In most cases, the TODs lead to greater revenues than costs and when they do not, they are only marginally negative and only due to the up-front costs. As a result, one could conclude that “growth is paying for growth” for the most part. 
		</p>

		<p>
			Local context appears to matter more for overall fiscal outcomes than specific design features within the scenarios. TODs located in areas with higher property values and larger development charges tend to generate substantial municipal revenue, particularly when they are built in areas that require relatively little additional infrastructure. Differences across scenarios within each proposed TOD appear to play a smaller role in determining overall fiscal impacts, although some variation remains.  
		</p>

		<Recommendation count=1 title="For lower upfront costs, build near existing infrastructure  "/>

		<p>
			Case studies which were largely adding density to areas with existing public infrastructure – including new roads, schools, and municipal facilities – had substantially lower capital costs, particularly in the early stage of development. While development charges may cover these investments, high development costs may deter or reduce the scale of development, particularly in tight markets. Most TODs benefit from some existing infrastructure, but densifying where infrastructure exists but is underused – for example, in neighbourhoods whose populations have declined – can lower costs. At the larger municipal scale, building where extensive new infrastructure is required, such as in greenfield zones surrounding cities, not only contributes to urban sprawl but will take much longer to break even – and if development is low-density, may not ever do so. 
		</p>

		<Recommendation count=2 title="Front-load development to achieve greater operating revenues sooner"/>

		<p>
			Since the majority of new TODs produce net positive operating revenues from property taxes and municipal service fees (potentially including more transit revenues), achieving substantial build-out sooner allows municipalities to benefit from these revenue flows earlier. Encouraging faster development through incentives such as streamlined regulations, lower taxes, or reduced development charges may make sense if the added density is sufficient. 
		</p>

		<p>
			The findings also suggest a connection between higher development charges and fewer housing starts, indicating that development charges may decrease the probability of construction. Thus, while fiscal outcomes are theoretically better in places with higher development charges that cover capital costs, in practice these may contribute to a policy environment that prevents the desired level of construction from ever being realized, particularly in challenging markets. These results highlight an important trade-off between fiscal contributions and the likelihood that projects will actually be built. While TODs can generate substantial fiscal benefits, policy environments must ensure that development projects remain financially viable for both developers and, longer-term, for municipalities. 
		</p>

		<Recommendation count=3 title="Optimize infrastructure investments"/>

		<p>
			Canada’s high infrastructure costs make new investments significant financial liabilities for municipalities. Identifying which investments are required and their costs is an inexact science, but also offers an opportunity. Learning from national and international best practices and delivering infrastructure projects in a cost-effective way is crucial in making large development projects successful. 
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

<style>
	:global(math) {
		font-size: 19px !important;
	}
</style>
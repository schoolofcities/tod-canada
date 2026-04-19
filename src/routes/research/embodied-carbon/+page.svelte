<script>

	import '../../../assets/global-styles.css';

	import AuthorDate from '$lib/AuthorDate.svelte';
	import BoilerPlate from '$lib/BoilerPlate.svelte';
	import Footnote from '$lib/Footnote.svelte';
	import Footnotes from '$lib/Footnotes.svelte';
	import { createFootnoteStore } from '$lib/footnoteUtils';
	import GraphicCompare from '$lib/GraphicCompare.svelte';
	import GraphicSingle from '$lib/GraphicSingle.svelte';
	import HamburgerMenu from '$lib/HamburgerMenu.svelte';
	import LogoBody from '$lib/LogoBody.svelte';
	import Recommendation from '$lib/Recommendation.svelte';
	import TitlePage from '$lib/TitlePage.svelte';

	const footnoteStore = createFootnoteStore();
	const { footnotes, addFootnote } = footnoteStore;

	const fns = [
		'Zujian Huang et al., “Life-Cycle Carbon Emissions (LCCE) of Buildings: Implications, Calculations, and Reductions,” <i>Engineering</i> 35 (2024): 115–139, <a href="https://doi.org/10.1016/j.eng.2023.08.019" target="_blank">DOI</a>.',
		'Gursans Guven et al., “A Construction Classification System Database for Understanding Resource Use in Building Construction,” <i>Scientific Data</i> 9, no. 1 (2022): 42, <a href="https://doi.org/10.1038/s41597-022-01141-8" target="_blank">DOI</a>; Keagan Hudson Rankin et al., “Embodied GHG of Missing Middle: Residential Building Form and Strategies for More Efficient Housing,” <i>Journal of Industrial Ecology</i> 28, no. 3 (2024): 455–68, <a href="https://doi.org/10.1111/jiec.13461" target="_blank">DOI</a>.',
		'Keagan H. Rankin and Shoshanna Saxe, “A Future Growth Model for Building More Housing and Infrastructure with Less Embodied Greenhouse Gas,” <i>Environmental Science & Technology</i> 58, no. 25 (2024): 10979–90, <a href="https://doi.org/10.1021/acs.est.4c02070" target="_blank">DOI</a>.',
		'Rankin and Saxe, “A Future Growth Model.”',
		'Aldrick Arceo et al., “Material Intensity in Single-Family Dwellings: Variability between Locations, Functional Unit and Drivers of Material Use in Toronto, Perth, and Luzon,” <i>Resources, Conservation and Recycling</i> 188 (January 2023): <a href="https://doi.org/10.1016/j.resconrec.2022.106683" target="_blank">DOI</a>; Rankin et al., “Embodied GHG of Missing Middle.”',
		'Avery Hoffer et al., “Does Height Matter? The Embodied Impacts of Tallness, Slab Thickness, Building Code and Design Tranches,” preprint, <i>Research Square</i>, February 12, 2025, <a href="https://doi.org/10.21203/rs.3.rs-6001700/v1" target="_blank">DOI</a>. ',
		'Arceo et al., “Material Intensity in Single-Family Dwellings”; Rankin et al., “Embodied GHG of Missing Middle.”',
		'KPMB Lab, <i>Embodied Carbon Values in Common Insulation Materials</i> (2021), <a href="https://www.kpmb.com/wp-content/uploads/2021/04/KPMB-LAB_Embodied-Carbon-in-Insulation.pdf" target="_blank">URL</a>.',
		'Gianluca Grazieschi et al., “Embodied Energy and Carbon of Building Insulating Materials: A Critical Review,” <i>Cleaner Environmental Systems</i> 2 (June 2021): <a href="https://doi.org/10.1016/j.cesys.2021.100032" target="_blank">DOI</a>.'

	];

	const credits = [
		{ role:"Research", names:"Letzai Ruiz, Santiago Zuluaga Mayorga, Keagan H. Rankin, Shoshanna Saxe"},
		{ role:"Additional writing", names:"Anika Reisha Taboy, Kathryn Exon Smith"},
		{ role:"Data visualization", names:"Mia Wang, Jeff Allen"},
		{ role:"Web development", names:"Mieko Yao, Jeff Allen"}
	]

</script>



<svelte:head>

	<title>TOD - Embodied Carbon | School of Cities</title>

	<meta name="description" content="Embodied Greenhouse Gas Emissions in Transit-Oriented Development Scenarios" />
	<meta name="author" content="School of Cities">
	<meta rel="canonical" href="https://schoolofcities.github.io/tod-canada/research/embodied-carbon/">

	<meta property="og:title" content="TOD - Embodied Carbon" />
	<meta property="og:description" content="Embodied Greenhouse Gas Emissions in Transit-Oriented Development Scenarios" />
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://schoolofcities.github.io/tod-canada/research/embodied-carbon/" />
	<meta property="og:image" content="https://raw.githubusercontent.com/schoolofcities/tod-canada/main/static/web-assets/research/embodied-carbon/thumbnail.png" />
	<meta property="og:locale" content="en_CA">

	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content="TOD - Embodied Carbon" />
	<meta name="twitter:description" content="Embodied Greenhouse Gas Emissions in Transit-Oriented Development Scenarios" />
	<meta name="twitter:site" content="https://schoolofcities.github.io/tod-canada/research/embodied-carbon/" />
	<meta name="twitter:image" content="https://raw.githubusercontent.com/schoolofcities/tod-canada/main/static/web-assets/research/embodied-carbon/thumbnail.png" /> 

	<meta name="citation_title" content="TOD - Embodied Carbon">
	<meta name="citation_author" content="Author Name 1">
	<meta name="citation_author" content="Author Name 2">
	<meta name="citation_author" content="Author Name 3"> 
	<meta name="citation_publication_date" content="2026/04">
	<meta name="citation_journal_title" content="School of Cities">
	<!-- <meta name="citation_pdf_url" content="https://schoolofcities.utoronto.ca/research-paper.pdf"> -->
	<!-- <meta name="citation_abstract_html_url" content="https://schoolofcities.github.io/design-components/"> -->

</svelte:head>



<main>

	<TitlePage
		title="Embodied Greenhouse Gas Emissions in Transit-Oriented Development Scenarios"
		type="Research"
		bgType="Video"
		url="/tod-canada/web-assets/research/embodied-carbon/toronto-contruction-4k-SBV-302197434-HD.mp4"
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
			Development has embodied greenhouse gas (GHG) impacts throughout its life cycle, including the emissions generated through upstream processes such as raw material extraction, manufacturing, transportation to site, and onsite energy use during construction.<Footnote id={addFootnote(fns[0])}/> This research quantifies the embodied GHG emissions from proposed development in <a href="/tod-canada/case-study/overview" target="_blank">five Canadian case study scenarios developed by the Infrastructure Institute</a>, comparing a scenario that reflects current development patterns (the <span style="border-bottom: 4px solid var(--brandMedBlue); font-family: InterBold">current trajectory</span>) in each case with a more mixed-use scenario that focuses on building complete communities around transit stations (<span style="border-bottom: 4px solid var(--brandMedGreen); font-family: InterBold">optimized scenario</span>). 
		</p>
		<p>	
			Because the majority of embodied GHG emissions occur during material manufacturing for construction, well before buildings are operational, they have immediate climate impacts. The following examples demonstrate how planning decisions shape the carbon impacts of urban growth. They also highlight opportunities to increase density while reducing emissions to help address both the climate and housing crises. 
		</p>
		
		<BoilerPlate pageType="Research"/>
		
		<h1>
			Methodology and approach
		</h1>

		<p>
			This study draws on a <a href="https://www.nature.com/articles/s41597-022-01141-8" target="_blank">University of Toronto database</a> that tracks the materials used in residential buildings and their associated embodied GHG emissions.<Footnote id={addFootnote(fns[1])}/> We used it to simulate the embodied GHG emissions of new buildings under both the current trajectory and optimized scenarios, capturing variation across individual buildings and development patterns. 
		</p>
		<p>
			We made some key assumptions to define the scope and boundaries of the embodied GHG estimates: 
		</p>
		<ul>
			<li>
				We calculated <strong>building embodied emissions</strong> based on unit counts and building types in each scenario, following the methodology of Rankin and Saxe, which covers all major construction-related processes, including structural, architectural, mechanical, electrical, and plumbing elements.<Footnote id={addFootnote(fns[2])}/> As such, the analysis captures a defined subset of embodied carbon emissions associated with upfront construction activities (A1-A5) and does not include operational emissions or later life cycle stages such as use and end-of-life processes.  
			</li>
			<li>
				We calculated <strong>road infrastructure emissions</strong> using the same methodology. For scenarios with new roads, we used detailed data on road types and layouts of existing roads to estimate emissions from asphalt, concrete, and granular materials, which we then used to determine GHG intensity per unit of road. 
			</li>
			<li>
				We divided total scenario emissions by the expected population growth to calculate the <strong>per capita GHG footprint</strong> of each scenario.
			</li>
			<li>
				We accounted for <strong>projected reductions in material emission intensity over time</strong> by year of construction, reflecting expected improvements in material manufacturing. Our projections do not assume full decarbonization in line with industry net-zero goals as there is not currently a demonstrated viable path to net-zero in Canada. 
			</li>
			<li>
				We illustrated the influence of <strong>family size</strong> (number of people living together) on the results through a sensitivity analysis of embodied GHG per capita by average unit occupancy of newly built units. 
			</li>
		</ul>
		
	</div>

	<GraphicSingle
		svg720={"../web-assets/research/embodied-carbon/embodied-carbon-graphic-720.svg"}
		svg360={"../web-assets/research/embodied-carbon/embodied-carbon-graphic-360.svg"}
	/>

	<div class="text">

		<p>
			<a href="../web-assets/research/embodied-carbon/Embodied Greenhouse Gas Emissions - Full Methodology and Findings.pdf" target="_blank">Click here for a more detailed discussion of the methodology.</a> 
		</p>

		<h1>What we found</h1>

		<p>
			Our analysis indicates that optimized, mixed-use scenarios generally result in lower or comparable total embodied GHG emissions, with unit size, occupancy levels, and building materials being important considerations. 
		</p>

		

		<h2>
			The optimized, complete community scenarios yield similar or lower total embodied carbon emissions 
		</h2>

		<p>
			Across the five station areas, optimized scenarios result in total embodied carbon emissions that are either comparable to or lower than the current trajectory. This suggests that designing station areas with a mix of physical and social infrastructure to build complete communities in addition to housing does not inherently produce greater embodied emissions.  
		</p>

	</div>

	<GraphicSingle
		svg720={"../web-assets/research/embodied-carbon/ghg-total-720.svg"}
		svg360={"../web-assets/research/embodied-carbon/ghg-total-360.svg"}
	/>

	<div class="text">

		<p>
			The number of developments alone is not the primary driver of embodied carbon. Instead, the type of buildings and the number of people they can house is key. Infill development near transit and existing infrastructure accommodates more people while avoiding the additional land consumption and infrastructure required by more dispersed growth.  
		</p>

		<p>
			Cooksville features the greatest gap between the two scenarios. Despite including more buildings, the optimized scenario would produce total emissions roughly 24% lower than the current trajectory because these buildings house more people per unit.  
		</p>

		<p>
			This shows that TOD can support meaningful densification without increasing total embodied carbon and, in some cases, even reduce it. Without denser or infill development, the default form of housing is sprawl elsewhere, which generates much higher emissions.  
		</p>

		<h2>
			Unit occupancy strongly influences per capita embodied emissions 
		</h2>

		<p>
			The optimized scenarios result in significantly lower emissions per capita where average occupancy – the number of people living in each unit – increases. 
		</p>

	</div>

	<GraphicSingle
		svg720={"../web-assets/research/embodied-carbon/ghg-per-capita-720.svg"}
		svg360={"../web-assets/research/embodied-carbon/ghg-per-capita-360.svg"}
	/>

	<div class="text">

		<p>			
			Cooksville shows the largest difference between scenarios, in part because this case explicitly focused on including larger, more family-friendly units in the optimized scenario. Per capita emissions decline from 20.9 tonnes of GHG emissions per person in the current trajectory to 14.1 tonnes per person when larger units were included in the optimized scenario, reflecting a substantial increase in average occupancy (1.35 vs. 1.9 people per unit). We observed similar reductions in Arbutus and McKernan-Belgravia, where the optimized scenarios also increase occupancy through changes in unit mix.  
		</p>

	</div>

	<GraphicSingle
		svg720={"../web-assets/research/embodied-carbon/occupancy-sensitivity-720.svg"}
		svg360={"../web-assets/research/embodied-carbon/occupancy-sensitivity-360.svg"}
	/>

	<div class="text">

		<p>
			In contrast, where occupancy remains unchanged, per capita emissions show little-to-no difference between scenarios. In Northfield, for example, both scenarios maintain an average of 1.6 people per unit, resulting in nearly identical per capita emissions. Panama follows the same pattern.  
		</p>

		<p>
			These findings indicate that occupancy levels have a strong influence on per capita embodied GHG emissions, highlighting the importance of unit mix and household size in reducing the carbon impacts of urban growth – though this impact is reversed if large units are underoccupied. 
		</p>

		<p>
			Click below to view summary statistics by station area.
		</p>

	</div>

	<GraphicCompare 
		images={[
			{
				svg720: "../web-assets/research/embodied-carbon/summary-arbutus-720.svg",
				svg360: "../web-assets/research/embodied-carbon/summary-arbutus-360.svg",
				caption: "",
				source: "",
				altText: "",
				buttonLabel: "Arbutus"
			},
			{
				svg720: "../web-assets/research/embodied-carbon/summary-cooksville-720.svg",
				svg360: "../web-assets/research/embodied-carbon/summary-cooksville-360.svg",
				caption: "",
				source: "",
				altText: "",
				buttonLabel: "Cooksville"
			},
			{
				svg720: "../web-assets/research/embodied-carbon/summary-mb-720.svg",
				svg360: "../web-assets/research/embodied-carbon/summary-mb-360.svg",
				caption: "",
				source: "",
				altText: "",
				buttonLabel: "McKernan-Belgravia"
			},
			{
				svg720: "../web-assets/research/embodied-carbon/summary-northfield-720.svg",
				svg360: "../web-assets/research/embodied-carbon/summary-northfield-360.svg",
				caption: "",
				source: "",
				altText: "",
				buttonLabel: "Northfield"
			},
			{
				svg720: "../web-assets/research/embodied-carbon/summary-panama-720.svg",
				svg360: "../web-assets/research/embodied-carbon/summary-panama-360.svg",
				caption: "",
				source: "",
				altText: "",
				buttonLabel: "Panama"
			},
		]}
	/>

	<div class="text">

		<h2>
			Timing of construction shapes per capita benefits of TOD 
		</h2>

		<p>
			The GHG intensity of construction materials is expected to decrease over time,<Footnote id={addFootnote(fns[3])}/> which affects the relative emissions performance of different development scenarios. Sensitivity analyses for Cooksville, Arbutus, and McKernan-Belgravia show that the optimized scenario has the largest difference from the current trajectory under 2025 conditions. However, this gap narrows as construction is delayed further into the future. As material production becomes less carbon-intensive, embodied emissions decline across all scenarios, lowering per capita emissions overall while also shrinking the relative advantage of the more mixed-use development scenarios. 
		</p>

	</div>

	<GraphicSingle
		svg720={"../web-assets/research/embodied-carbon/year-sensitivity-720.svg"}
		svg360={"../web-assets/research/embodied-carbon/year-sensitivity-360.svg"}
	/>

	<div class="text">

		<p>
			This creates a timing trade-off: although building later would lower emissions in absolute terms (assuming construction material manufacturing does in fact decarbonize), delaying development exacerbates current housing shortages. Advancing projects sooner – particularly in denser developments near transit – helps preserve the per capita emissions advantage associated with higher occupancy and efficient land use, while still contributing to near-term supply.  
		</p>

		<p>
			It is important to note that this sensitivity analysis assumes that all buildings for each scenario are built in the same year. In practice, this is unlikely given that large multi-unit buildings are often multi-year endeavours and will not all be built simultaneously.  
		</p>

		<p>
			<a href="../web-assets/research/embodied-carbon/Embodied Greenhouse Gas Emissions - Full Methodology and Findings.pdf" target="_blank">See the full analysis here.</a> 
		</p>

		<div class="quote" style="padding-top: 40px; padding-bottom: 40px;">
			<p>
				Well-designed TOD can deliver schools, retail, and community services alongside higher-density housing – supporting quality of life while still meeting climate targets.  
			</p>
		</div>

		<h1>
			Key conclusions and policy recommendations 
		</h1>

		<p>
			Our analysis shows that “optimized” complete community scenarios – characterized by a mix of building forms and integrated physical and social infrastructure – generally result in lower or comparable total embodied GHG emissions compared to current trajectories of development in the same geographies.  
		</p>

		<p>
			A critical factor influencing per capita embodied GHG is the mix of unit types and bedroom counts: scenarios with a higher share of family-oriented units and higher average occupancy rates tend to have lower per capita emissions. Improvements in material manufacturing and other key design choices can also be made to maximize building efficiency.  
		</p>

		<Recommendation count=1 title="Optimize building layouts for efficiency"/>

		<p>
			Building design and layout is a critical lever for reducing embodied GHG emissions because it maximizes how efficiently the spaces are used. Planning policies should encourage a diverse housing mix near transit, particularly larger units that support higher occupancy and more efficient use of materials per resident. Larger units can reduce embodied emissions by lowering the ratio of kitchens, bathrooms, and common spaces per resident. Improving floor plate efficiency can reduce material use: spaces like hallways use as much material as living areas but provide less utility, so more efficient layouts can lower per-unit embodied GHGs. 
		</p>

		<Recommendation count=2 title="Optimize structural and architectural design to reduce material use"/>

		<p>
			Avoiding underground parking construction is the most powerful opportunity to reduce building embodied GHG emissions in mid- and high-rise buildings specifically.<Footnote id={addFootnote(fns[4])}/> Floor slabs are another major source of embodied emissions. Aligning structural columns vertically from floor to floor improves efficiency, allowing for thinner slabs and less concrete, which lowers a building’s embodied carbon footprint.<Footnote id={addFootnote(fns[5])}/> 
		</p>

		<Recommendation count=3 title="Support low-carbon material manufacturing "/>

		<p>
			Over time, embodied GHG outcomes will also depend on improvements in material manufacturing. Governments can accelerate this transition by setting embodied carbon benchmarks for new construction, incentivizing the use of low-carbon materials through procurement policies, and supporting innovation and scaling of low-emission building materials. Material decarbonization is a key long-term climate strategy for the construction sector. Insulation is often the second-largest source of embodied GHGs in a building after concrete, making material choice particularly important.<Footnote id={addFootnote(fns[6])}/> Avoiding fossil-fuel-based products like extruded polystyrene and expanded polystyrene can reduce emissions.<Footnote id={addFootnote(fns[7])}/> Low-carbon alternatives already on the market include glass wool or stone wool.<Footnote id={addFootnote(fns[8])}/>   
		</p>	
		
		<div class="quote" style="padding-top: 70px;">
			<p>
				Design choices can reduce the embodied GHG in a building by 50% or more.  
			</p>
		</div>
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

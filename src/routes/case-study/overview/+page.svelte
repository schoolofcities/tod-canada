<script>

	import '../../../assets/global-styles.css'; 
	import LogoBody from '$lib/LogoBody.svelte';
	import Footnote from '$lib/Footnote.svelte';
	import Footnotes from '$lib/Footnotes.svelte';
	import { createFootnoteStore } from '$lib/footnoteUtils';
    // import CaseStudyCard from '$lib/CaseStudyCard.svelte';

	const footnoteStore = createFootnoteStore();
	const { footnotes, addFootnote } = footnoteStore;

	const fns = [
		'Ewing, 1999; Blainey and Evens, 2011; Guerra and Cervero, 2012'
	];
</script>




<svelte:head>

	<title>TOD Case Studies | School of Cities</title>

</svelte:head>



<main>
	<div class="text">
		<h1>Case studies</h1>

		<p>
			The <a href="https://schoolofcities.utoronto.ca/" target="_blank">School of Cities</a> and the <a href="https://infrastructureinstitute.ca/" target="_blank">Infrastructure Institute</a> have produced a series of five case studies to identify different kinds of transit-oriented development (TOD) across Canada and to explore the opportunities and trade-offs involved in creating thriving communities near transit.
		</p>

		<p>
			In each case, we explored two scenarios: 
		</p>

		<ul>
			<li>
				<strong>The current trajectory</strong>: a projection of what kinds of development are being proposed in the area, projected out 20-30 years along the same patterns 
			</li>

			<li>
				<strong>The optimized scenario</strong>: an alternative that imagines policy and design changes to address common TOD challenges 
			</li>
		</ul>

		<p>
			Each case presents a different archetype of a station area and suggests recommendations based on Canadian and international best practices in building complete communities near transit in order to provide policy-makers with evidence and tools that support decisions on infrastructure investments. 
		</p>

		<h2>
			Five distinct station areas 
		</h2>

		<p>
			We examined the following case study areas: 
		</p>

		<!-- <CaseStudyCard 
			title="Arbutus Station"
			location="Vancouver, British Columbia"
			description="The Arbutus case focuses on displacement risk, with the optimized scenario preserving existing older low- and mid-rise housing stock where possible and concentrating new development along the major commercial corridor of Broadway. It also plans for modest, affordable infill in surrounding neighbourhoods and an increase in essential public services to keep pace with the increase in population."
			keyQuestion="Key question: How can we preserve the best features of established neighbourhoods ensure that housing remains affordable while increasing density around transit?"
			image="../web-assets/case-study/cooksville/cooksville-scenario1.png"/> -->

		<ul>
			<li>
				<a href="./arbutus" target="_blank">Arbutus Station</a>, Vancouver, British Columbia
			</li>
			<ul>
				<li>
					Key question: How can we preserve the best features of established neighbourhoods ensure that housing remains affordable while increasing density around transit? 
				</li>
				<li>
					The Arbutus case focuses on displacement risk, with the optimized scenario preserving existing older low- and mid-rise housing stock where possible and concentrating new development along the major commercial corridor of Broadway. It also plans for modest, affordable infill in surrounding neighbourhoods and an increase in essential public services to keep pace with the increase in population. 
				</li>
			</ul>

			<li>
				<a href="./cooksville" target="_blank">Cooksville Station</a>, Mississauga, Ontario
			</li>
			<ul>
				<li>
					Key question: How can we build complete, family-friendly communities while managing flood risk? 
				</li>
				<li>
						In Cookville, the optimization focuses on building larger units with more bedrooms and social infrastructure, including schools and gathering spaces, which allows reductions in building heights and more human-scaled street fronts. The area’s flood risk is addressed by reducing impermeable surfaces and weaving green corridors and parks through the site to double as flood protection. 
				</li>
			</ul>

			<li>
				<a href="./mckernan-belgravia" target="_blank">McKernan-Belgravia Station</a>, Edmonton, Alberta
			</li>
			<ul>
				<li>
					Key question: How can we build infill in a mature community with strategic infrastructure investments to support high-capacity transit ridership? 
				</li>
				<li>
					The optimized scenario in the mature neighbourhood of McKernan-Belgravia foregrounds mid-rise development along major corridors and next to the station, including commercial uses, rather than lower-density infill dispersed through neighbourhoods. It also prioritizes infrastructure that allows more connectivity through the station area for active transportation and transit users. 
				</li>
			</ul>

			<li>
				<a href="./northfield" target="_blank">Northfield Station</a>, Waterloo, Ontario 
			</li>
			<ul>
				<li>
					Key question: How can we transform industrial land into a vibrant community that attracts – and keeps – jobs and talent?  
				</li>
				<li>
					As Northfield Station transitions from industrial land to a more mixed-use area, the optimized scenario preserves retail and employment uses alongside proposed residential development to drive transit ridership. It breaks down existing large parcels into a finer-grained network of smaller blocks with linear parks, open spaces, and stronger connections to the station for pedestrians and cyclists. 
				</li>
			</ul>

			<li>
				<a href="./panama" target="_blank">Panama Station</a>, Brossard, Quebec 
			</li>
			<ul>
				<li>
					Key question: How can we transform a suburban terminal into a complete, transit-oriented community through strategic development, civic infrastructure investment, and inclusive planning? 
				</li>
				<li>
					At Panama Station, the optimized scenario takes a strong city vision to create a new downtown on the site and adds more civic infrastructure in the form of playgrounds, schools, and services to support the area’s multicultural community. Several outdoor plazas and parks accompany mid-rise density throughout the station area.     
				</li>
			</ul>
		</ul>

		<h2>
			Why these stations? 
		</h2>

		<p>
			TOD takes many forms in Canada, and these station areas represent this diversity: some are in dense, urban areas, while others are in smaller cities or emerging regions. Together, the case studies represent distinct archetypes of transit station areas with varying urban forms and demographic profiles and offer lessons that can be applied broadly to similar neighbourhoods across the country.  
		</p>

		<p>
			We considered the following variables when selecting the stations and station areas: 
		</p>

		<ul>
			<li>
				Location on a rapid, frequent, fixed transit line (i.e., light or heavy rail) 
			</li>
			<li>
				Representing a variety of geographies and jurisdictions across Canada 
			</li>
			<li>
				A mix of established (&lt;10 years), recent (&gt;10 years), and planned stations
			</li>
			<li>
				Differing demographic mix and levels of density in station areas 
			</li>
			<li>
				Existing levels of multimodal accessibility  
			</li>
			<li>
				Differing age and type of urban forms 
			</li>
			<li>
				Availability of parcel data 
			</li>
		</ul>

		<h2>
			Our methods and approach 
		</h2>

		<p>
			We defined the station area as an 800-metre radius around the transit station, consistent with commonly accepted guidance suggesting a 10-minute walk at average pace.<Footnote id={addFootnote(fns[0])}/>
		</p>

		<p>
			To calculate demographics, we combined open-source data from the 2021 census with proprietary data from Environics Analytics DemoStats, which are updated annually. The demographic data includes population counts, housing data, basic demographic information, and commuting data. 
		</p>

		<p>
			We used the Measuring Main Streets methodology to go beyond housing and consider the elements necessary for a complete community – such as spaces for care services, community, recreation, local retail, and mobility. We then identified high‑potential opportunity sites for additional residential and commercial uses, drawing on the four site types outlined in CUI's <a href="https://canurb.org/wp-content/uploads/Remaking-Main-Streets.pdf" target="_blank">Remaking Main Streets report</a> (vacant, not optimal, low-density, and anchor), and assessed opportunities to add new housing through adaptive re-use, intensification, small-scale context-specific development, and new tower construction. We 3D-modelled the scenarios using base data on the existing built form from publicly available open data sources to build out the base file. It is important to note that all station area renderings are conceptual and should not be interpreted as specific guidance for individual properties. Renderings were created in 2025 and may not reflect more recent proposals. 
		</p>
	</div>

	<Footnotes footnotes={footnotes} />

	<div class="text">
		<div class="line-break"></div>
		<p>
			Based at the University of Toronto, the School of Cities is a multidisciplinary hub for urban research, education, and engagement creating new and just ways for cities and their residents to thrive. The School supports scholars, practitioners, and community members to co-create new understandings, policies, and practices and fosters opportunity, insight, and knowledge exchange with a global reach. 
		</p>

		<p>
			This work is part of the <a href="https://housing-infrastructure.canada.ca/rki-irc/index-eng.html" target="_blank">Research Knowledge Initiative</a> program from <a href="https://housing-infrastructure.canada.ca/index-eng.html" target="_blank">Housing, Infrastructure and Communities Canada</a>
		</p>
		<LogoBody/>
		<div class="line-break"></div>
	</div>


</main>


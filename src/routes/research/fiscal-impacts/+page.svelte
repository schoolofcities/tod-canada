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
	
	import Footnote from '$lib/Footnote.svelte';
	import Footnotes from '$lib/Footnotes.svelte';
	import { createFootnoteStore } from '$lib/footnoteUtils';
    import HamburgerMenu from '$lib/HamburgerMenu.svelte';

	const footnoteStore = createFootnoteStore();
	const { footnotes, addFootnote } = footnoteStore;

	const fns = [
		'Karen Chapple and Anastasia Loukaitou-Sideris, Transit-oriented displacement or community dividends?: Understanding the effects of smarter growth on communities (MIT Press, 2019).',
		'Peter Marcuse, “Gentrification, abandonment, and displacement: Connections, causes, and policy responses in New York City,” in Washington University Journal of Urban & Contemporary Law 28 (1985), 195.',
		'More than 70 stations opened during this time period, but a few stations were not included in our analysis because data were unavailable.',
		'Statistics Canada, “Longitudinal Administrative Databank (LAD),” 2025, <a href="https://www23.statcan.gc.ca/imdb/p2SV.pl?Function=getSurvey&SDDS=4107" target="_blank">URL</a>. At the time of writing, 2022 were the most recent data available.'
	];

	const credits = [
		{ role:"Research", names:"Alex Hempel"},
		{ role:"Additional writing", names:"Kathryn Exon Smith"},
		{ role:"Data visualization", names:"Jeff Allen"},
		{ role:"Web development", names:"Mieko Yao, Jeff Allen"}
	]

</script>



<svelte:head>

	<title>TOD - Fiscal Impacts | School of Cities</title>

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
		title="Fiscal Impacts of Transit Oriented Development"
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

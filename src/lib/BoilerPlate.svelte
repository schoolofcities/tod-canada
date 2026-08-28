
<script>
	export let pageType = "CaseStudy" // Research

	let boilerPlate = '';

	if (pageType === "CaseStudy") {
		boilerPlate = '<p>    This is one of five case studies produced by the Infrastructure Institute and the School of Cities to identify different kinds of transit-oriented development across Canada and to explore the opportunities and trade-offs involved in creating thriving communities near transit. In each case, we examine current plans and patterns of growth and project what that community might look like in 20-30 years if development continues in this way (the “current trajectory”). We then present an alternative, “optimized” scenario that imagines changes that could address common challenges. We are guided by a focus on the identified principles of high-quality TOD: density, a diverse mix of land uses, and high-quality design (the “3Ds”).</p><p>Our station area renderings are hypothetical exercises to understand what development looks like in different kinds of urban settings based on existing zoning and community plans. They are not intended to be prescriptive guidance for specific properties or neighbourhoods. The models explore what is possible – what current research suggests are effective ways to add the residential density and supporting infrastructure that makes great communities. But communities must be planned by and for the people that live in them. We offer this analysis to spark discussion about what’s possible.</p>';
	} else if (pageType === "CaseStudyFR") {
		boilerPlate = '<p>Il s’agit de l’une des cinq études de cas réalisées par l’Infrastructure Institute et la School of Cities cherchant à identifier différents types d’aires TOD à travers le Canada et à explorer les opportunités et les compromis liés à la création de communautés dynamiques à proximité de transports en commun. Dans chaque cas, nous examinons les plans actuels et les modèles de croissance, puis nous projetons à quoi pourrait ressembler cette communauté dans 20 à 30 ans si son développement se poursuivait de cette manière (l’ « évolution actuelle »). Nous présentons ensuite un scénario alternatif « optimisé » qui envisage des changements susceptibles de relever les défis courants. Nous nous appuyons pour cela sur les principes d’une aire TOD considéré de haute qualité : la densité, la mixité des usages du sol et une conception de haute qualité (les « 3D » en anglais: density, diverse mix of land uses, high-quality design).</p><p>Nos rendus de la zone autour de la station constituent des exercices hypothétiques visant à comprendre à quoi pourrait ressembler le projet dans différents types de contextes urbains, sur la base du zonage et des plans communautaires existants. Ils ne sont pas destinés à servir de lignes directrices contraignantes pour des propriétés ou des quartiers spécifiques. Ces modèles explorent les possibilités qui existent – ce que les études actuelles suggèrent comme étant des moyens efficaces d’augmenter la densité résidentielle et de mettre en place les infrastructures nécessaires à la création de communautés de qualité. Mais les communautés doivent être planifiées par et pour les personnes qui y vivent. Nous proposons cette analyse afin de susciter une réflexion sur ce qui est possible.</p>';
	} else if (pageType === "Research") {
		boilerPlate = '<p>This research brief is one of six produced by the <a href="https://schoolofcities.utoronto.ca/" target="_blank">School of Cities</a> to understand the benefits and trade-offs of building density near transit. Using case studies and data from across Canada, each brief examines how different forms of transit-oriented development (TOD) affect a core urban issue, such as municipal finances, displacement, equity, or greenhouse gas emissions. </p><p>This work is part of the <a href="https://housing-infrastructure.canada.ca/rki-irc/index-eng.html" target="_blank">Research Knowledge Initiative</a> program from <a href="https://housing-infrastructure.canada.ca/index-eng.html" target="_blank">Housing, Infrastructure and Communities Canada</a> and developed in partnership with the <a href="https://canurb.org/" target="_blank">Canadian Urban Institute</a>.</p>';
	} else {
		boilerPlate = "<p>meow</p>";
	}

</script>




<div>
	{@html boilerPlate}
</div>




<style>
	div {
		margin-top: 50px;
		border-radius: 25px;
		background-color: rgb(0, 0, 0, 0.03);
		padding: 30px;
	}

	p {
		padding: 0px;
		margin: 0px;
		font-family: PoppinsRegular;
		line-height: 27px;;
		font-size: 16px;
	}

	p :global(a) {
        font-family: inherit;
    }

	@media (max-width: 500px) {
		div {
			padding: 20px;
		}
		p {
			font-size: 12px;
			line-height: 21px;
		}
	}

</style>

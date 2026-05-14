
<script>
	export let pageType = "CaseStudy" // Research

	let boilerPlate = '';

	if (pageType === "CaseStudy") {
		boilerPlate = '<p>    This is one of five case studies produced by the Infrastructure Institute and the School of Cities to identify different kinds of transit-oriented development across Canada and to explore the opportunities and trade-offs involved in creating thriving communities near transit. In each case, we examine current plans and patterns of growth and project what that community might look like in 20-30 years if development continues in this way (the “current trajectory”). We then present an alternative, “optimized” scenario that imagines changes that could address common challenges. We are guided by a focus on the identified principles of high-quality TOD: density, a diverse mix of land uses, and high-quality design (the “3Ds”).</p><p>Our station area renderings are hypothetical exercises to understand what development looks like in different kinds of urban settings based on existing zoning and community plans. They are not intended to be prescriptive guidance for specific properties or neighbourhoods. The models explore what is possible – what current research suggests are effective ways to add the residential density and supporting infrastructure that makes great communities. But communities must be planned by and for the people that live in them. We offer this analysis to spark discussion about what’s possible.</p>';
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

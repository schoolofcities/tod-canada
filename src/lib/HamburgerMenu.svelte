<script>

	import "../assets/global-styles.css";  
	import { onMount } from "svelte";
    // import { tick } from 'svelte';

	export let iconColour = "black";
    export let contents = [];
    export let menuColour = "#e2e2e2"
    export let textColour = "black";
    export let pageType = "caseStudy"

    let opened = false;
    let menu;

    let xColour = iconColour;
    $: xColour = opened ? "black" : iconColour;
    
    function handleKeydown(e) {
        if (e.key === 'Escape') {
            opened = false;
            document.querySelector('.hamburger-container')?.focus();
        }
    }

    function triggerMenu() {
        opened = !opened;

        // if (opened) {
        //     await tick();
        //     const firstLink = document.querySelector('#menu-content a');
        //     firstLink?.focus();
        // }
    }
    function urlFormat(text) {
        return text.trim().toLowerCase()
            .normalize('NFD').replace(/[\u0300-\u036f]/g, '')
            .replace(/[^a-z0-9\s-]/g, '')
            .replace(/\s+/g, '-')
            .replace(/-+/g, '-')
            .replace(/^-|-$/g, '');
    }
    

    function handleHashNavigation() {
        opened = false;
        const hash = decodeURIComponent(window.location.hash.slice(1));
        const headings = document.querySelectorAll('h1');
        const match = [...headings].find(h => urlFormat(h.textContent) === hash);
        match?.scrollIntoView({ behavior: 'smooth', block: 'start' });
    }

    onMount(() => {
        menu = document.getElementById("menu");
        let r = document.querySelector(':root');
        
        r.style.setProperty('--menuColour', menuColour);
        r.style.setProperty('--iconColour', iconColour);

        if (contents.length == 0) {
            let headers = Array.from(document.getElementsByTagName("h1"));
            console.log(headers);
            headers.forEach(element => {
                if (!element.classList.contains("title-text")) {
                    contents.push({item_id: urlFormat(element.textContent), menu_entry: element.textContent})
                }
            })

            window.addEventListener('DOMContentLoaded', handleHashNavigation);
            window.addEventListener('hashchange', handleHashNavigation);
        }

        
        const title = document.querySelector('.title-container'); 
        let hamburger = document.getElementsByClassName("hamburger-container")[0];

        const observer = new IntersectionObserver(([entry]) => {
        if (entry.isIntersecting) {
            hamburger.classList.add("title");
            if (pageType != "caseStudy") iconColour = "white";
        } else {
            if (pageType != "caseStudy") iconColour = "black";
            hamburger.classList.remove("title");
        }
        });

        observer.observe(title);
    }) 

</script>


<div>
    <button
        class="hamburger-container"
        class:opened
        class:has-background={iconColour == "black"}
        on:click={triggerMenu}
        aria-label="Navigation Menu"
        aria-expanded={opened}
        aria-controls="menu-content"
        on:keydown={handleKeydown}>
        <svg 
            class="icon"
            height="5.6rem"
            width="7rem"
            viewBox="0 0 215.2673 163.80329">

            <rect fill={xColour} class="bar top" x="0" y="0" width="215" height="23" rx="12" />

            <!-- middle bar -->
            <rect fill={xColour} class="bar middle" x="0" y="75" width="215" height="23" rx="12" />

            <!-- bottom bar -->
            <rect fill={xColour} class="bar bottom" x="0" y="150" width="215" height="23" rx="12" />
        
        </svg>
    </button>

    <div class="menu" 
        style:height="100vh"
        style:background-color={menuColour}
        class:opened
        >
        {#if opened}
            <nav id="menu-content">
                <a href="#top" style:color={textColour}>Title</a>

                {#each contents as content}
                    <a href={`#${content.item_id}`} 
                    style:color={textColour} 
                    on:click={() => {
                        opened = false;
                    }}>{content.menu_entry}</a>
                {/each}
            </nav>
        {/if}
    </div>

</div>



<style>
    .hamburger-container {
        width: fit-content;
        height: fit-content;
        cursor:pointer;
        border: none;
        background-color: rgb(0,0,0,0);
        position: fixed;
		z-index: 100;
        top: 15rem;
        right: 15rem;
        transition: background-color 200ms ease 300ms;
        border-radius: 50%;   
    }

    :global(.hamburger-container.title) {
        transition: background-color 0ms;
    }

    .hamburger-container.opened {
        transition: background-color 0ms;
    }

    .hamburger-container.has-background {
        background-color: white;
    }

    .hamburger-container.has-background.opened {
        background-color: rgb(0,0,0,0);
    }

    .icon {
        overflow: visible;
        margin: 3px 0px 1px 0px;
    }

    .bar {
        transform-box: fill-box;
        transform-origin: center;
        transition:
            transform 300ms cubic-bezier(0.4, 0, 0.2, 1),
            opacity 200ms ease;
    }

    .hamburger-container.opened .bar.top {
    transform: translateY(75px) rotate(45deg) ;
    }

    .hamburger-container.opened .bar.middle {
    opacity: 0;
    }

    .hamburger-container.opened .bar.bottom {
    transform: translateY(-75px) rotate(-45deg) ;
    }

    .menu {
        width: 25vw;
        right: 0;
        bottom: 0;
        transform: translateX(25vw);
        transition: transform 300ms cubic-bezier(0.4, 0, 0.2, 1);
        z-index: 25;
        position: fixed;
        display: flex;
        align-items: center;
    }

    .menu.opened {
        transform: translateX(0vw);
    }

    #menu-content {
        margin-left: 10%;
    }

    a {
        color: black;
        font-size: 6rem;
        font-family: PoppinsSemiBold;
        display: block;
        padding-bottom: 7rem;
        text-decoration: none;
    }

    a:hover {opacity: 60%;}

    @media (max-aspect-ratio: 5/6) {
        .menu {
            width: 100vw;
            transform: translateX(100vw);
        }
    }
    

</style>
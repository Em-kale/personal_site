<script>
   import './styles.css';
    import GithubLogo from '/src/lib/icons/github-mark-white.svelte'
    import LinkedinLogo from '/src/lib/icons/linkedin-logo-svgrepo-com.svelte'
    import { afterUpdate} from 'svelte' 
    
    let titleClass="desktop-title" 
    let subtitleClass="desktop-subtitle"  
    afterUpdate(() => {
        const isMobile = window.matchMedia("(max-width: 700px)")
        if(isMobile.matches){
             titleClass = "mobile-title";
             subtitleClass = "mobile-subtitle";
        }
    })
   </script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section >
	<h1 class={titleClass}>Emmitt Luhning </h1>
    <h2 class={subtitleClass}>Software developer, hacker, alleged android</h2>    
    <div class="icon-container"> 
        <a target="__blank" href="https://www.github.com/Em-kale"> 
            <GithubLogo className="github-logo"/>
        </a>
        <a target="__blank" href="https://www.linkedin.com/in/emmittl/">
            <LinkedinLogo className="linkedin-logo"/>
    </a>
    </div>
</section>

<style>
    section {
        display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}
    .icon-container{
        margin: 200px 0px 0px 0px; 
    }
    .mobile-subtitle{
        font-size: 30px;
        font-weight: 500px;
        font-family: 'primus';
        width: 100%;
        margin: 10px 0px 0px 15px;
    }
    .desktop-subtitle{
        font-size: 30px;
        font-weight: 500px;
        font-family: 'primus';
        width: 100%;
        margin: 10px 0px 0px 15px;
    }
    .desktop-title{
        margin: 0px; 
        font-size:90px;
        font-weight: 900px;
        font-family: 'primus';
        width: 100%;
	}
    .mobile-title{
        margin: 0px; 
        font-size:55px;
        font-weight: 900px;
        font-family: 'primus';
        width: 100%;
	}
</style>

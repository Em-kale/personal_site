<script>
   import './styles.css';
    import GithubLogo from '/src/lib/icons/github-mark-white.svelte'
    import LinkedinLogo from '/src/lib/icons/linkedin-svgrepo-com.svelte'
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section >
	<h1>Emmitt Luhning </h1>
    <h2>Software developer, hacker, alleged android</h2>    
    <div class="icon-container">
    <a href="https://www.github.com/Em-kale"> 
        <GithubLogo className="github-logo"/>
    </a>
    <a href="https://www.github.com/Em-kale">
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
        align-items: "center";
    } 
    h2{
        font-size: 30px;
        font-weight: 500px;
        font-family: 'primus';
        width: 100%;
        margin: 10px 0px 0px 15px;
        }
	h1 {
        margin: 0px; 
        font-size:90px;
        font-weight: 900px;
        font-family: 'primus';
        width: 100%;
	}
</style>

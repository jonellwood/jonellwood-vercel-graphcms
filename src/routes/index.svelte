<script>
  import { fade } from 'svelte/transition'
  import { onMount } from 'svelte';

  let visible = false;
  onMount(() => visible = true), setTimeout(() => visible = false, 5000);

</script>

<main>

  {#if visible}
	<!-- <div class="centered" out:fly="{{y: -20, duration: 800}}"> -->
	<div class="intro" out:fade="{{delay: 25, duration: 800}}">
		{#each 'ellwood' as char, i}
			<span
				in:fade="{{delay: 1000 + i * 150, duration: 800}}"
			>{char}</span>
		{/each}
	</div>
{/if}

{#if !visible}
<div class="about">
  <h1>About</h1>
  <div class=wrapper>
    <div class="bord-right">
      <p>Hi I'm me. nice to meet you!</p>
    </div>
    <div class="bord-right">
      Name: Jon Ellwood <br/>
      Location: Charleston, SC <br/>
      Likes: Long walks in a blizzard <br/>
      Github: <a href="https://github.com/jonellwood">Jon Ellwood</a> <br/>
      Email: <a href="mailto:jonellwood@gmail.com">jonellwood at gmail dot com</a> <br/>
    </div>
    <div class="bord-left">
      Education: School of Hard Knocks
    </div>
  </div>
</div>


<h2>Skills</h2>
  <div class="skills-logos">
    <img src="https://res.cloudinary.com/drwfft7zs/image/upload/v1628773478/jonellwood%20dot%20dev/FEWD_yzodhk.png" alt="W3cx Front End Developer">
    <img src="https://res.cloudinary.com/drwfft7zs/image/upload/v1629488190/jonellwood%20dot%20dev/CSS3_logo_utk4a6.png" alt="CSS 3">
    <img src="https://res.cloudinary.com/drwfft7zs/image/upload/v1629488190/jonellwood%20dot%20dev/react_logo_kmlil5.png" alt="React">
    <img src="https://res.cloudinary.com/drwfft7zs/image/upload/v1629488190/jonellwood%20dot%20dev/HTML5_rt1eap.png" alt="HTML">
    <img src="https://res.cloudinary.com/drwfft7zs/image/upload/v1629488190/jonellwood%20dot%20dev/NOdeJs2_lgge51.png" alt="Node J S">
    <img src="https://res.cloudinary.com/drwfft7zs/image/upload/v1629488190/jonellwood%20dot%20dev/JavaScript_logo_eohbre.png" alt="JavaScript">
    <img src="https://res.cloudinary.com/drwfft7zs/image/upload/v1629488190/jonellwood%20dot%20dev/GraphQL_tfsi70.png" alt="graph q l">
    <img src="https://res.cloudinary.com/drwfft7zs/image/upload/v1629488189/jonellwood%20dot%20dev/gatsby2_zwot9z.png" alt="Gatsby - the software not the guy">
    <img src="https://res.cloudinary.com/drwfft7zs/image/upload/v1629488189/jonellwood%20dot%20dev/wordpress_cuyybz.png" alt="Word Press">
    <img src="https://res.cloudinary.com/drwfft7zs/image/upload/v1629488189/jonellwood%20dot%20dev/512px-Svelte_Logo.svg_ahioh7.png" alt="Svelte">

  </div>

  <h2 class="silly">Silly</h2>
    <div>
      <p class="silly">Something Silly goes here</p>
    </div>
{/if}
</main>

<style>
 main{
   font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
 }

 .intro{
   font-size: 20vw;
   position: absolute;
   left: 50%;
   top: 50%;
   transform: translate(-50%, -50%);
   font-family: "Overpass";
   letter-spacing: 0.12rem;
   color: #ffc600;
   -webkit-text-stroke-width: 4px;
   -webkit-text-stroke-color: #4969e1;
   font-weight: 400;
 }
 h1{
   font-size: 3em;
   text-align: center;
   background-color: #4969e1;
   /* margin-left: 20px;
   margin-right:20px; */
   margin-bottom: 0px;
   color: white;
 }
 h2{
   font-size: 3em;
   text-align: center;
   /* margin-left: 20px;
   margin-right:20px; */
   margin-bottom: 0px;
 }
 .wrapper{
   /* margin-left: 20px;
   margin-right:20px; */
   display: grid;
   grid-template-columns: 1fr 1fr 1fr;
   background-color: #4969e1;
   font-size: large;
   padding: 20px;
   line-height: 1.75;
   text-align: center;
 }
 .bord-right{
 border-right: 2px solid black;
 }
 .skills-logos {
   display: grid;
   grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
   margin-left: auto;
   margin-right: auto;
 }
 .skills-logos img{
   margin-left: auto;
   margin-right: auto;
   margin-top: 15px;
   margin-bottom: 15px;
 }
 img{
   width: 100px;
 }
 @media (max-width: 680px) {
  .skills-logos {
   grid-template-columns: 1fr 1fr 1fr;
  }
  }
.silly{
  background-color: #097504;
  margin-bottom: 0;
}

</style>


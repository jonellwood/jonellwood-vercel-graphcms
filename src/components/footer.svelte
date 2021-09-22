

<footer>
    <span class="generic">Generic Front End Solutions you can probably just do yourself.</span>
  
    <span class="siteInfo">Site built with Sveltekit and GraphCMS</span>
    <span class="copywrite">©️ Jon Ellwood 2021</span>
  </footer>
  
  <style>
    footer{
      position: absolute;
      bottom: 0;
      width: 100%;
      display: grid;
      grid-template-rows: 2fr 1fr 1fr;
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
      gap: 15px;
      text-align: center;
      align-items: center;
    }
    .generic{
      font-size: x-large;
      font-family: 'Courier New', Courier, monospace;
    }
    .siteInfo{
      font-size: smaller;
    }
  
    .copywrite{
      padding-bottom: 15px;
    }
    @media (max-width: 680px) {
      .generic{
        display: none;
      }
      .siteInfo{
        display: none;
      }
      .copywrite{
        padding-bottom: 0px;
      }
    }
  </style>
  
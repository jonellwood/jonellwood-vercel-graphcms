<nav>
    <a href="/">Home</a>
    <a href="/projects">Projects</a>
    <a href="/outside">Outside</a>
  </nav>
  
  <style>
    nav{
      margin: 0;
      padding: 0;
      display: flex;
      justify-self: end;
      font-size: 2rem;
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
      -webkit-text-stroke-width: 1px;
     -webkit-text-stroke-color: #4969e1;
    }
    a:hover{
      text-shadow: 2px 2px 3px yellow;
      /* box-shadow: 2px 2px 3px yellow; */
      transition: all 0.5s ease .5s;
    }
    a{
      padding: 1rem 2rem;
      display: flex;
      align-items: center;
      position: relative;
      text-transform: lowercase;
      font-weight: 500;
      font-size: 1em;
      background: none;
      border: 0;
      text-decoration: none;
      color: black;
      cursor: pointer;
      /* transform: skew(-20deg); */
    }
    @media (max-width: 700px) {
        a {font-size: 10px;
        padding: 0 10px;
      }
    }
    a:before {
      content: '';
      width: 2px;
      height: 100%;
      left: 0;
      position: absolute;
      transform: skew(20deg);
      top: 0;
      bottom: 0;
    }
    a:before{
      height: 2px;
        background: red;
        content: '';
        width: 0;
        position: absolute;
        transform: translateX(-50%);
        transition: width 0.4s;
        transition-timing-function: cubic-bezier(1, -0.65, 0, 2.31);
        left: 50%;
        margin-top: 2rem;
    }
    a:hover,
    a:focus {
      outline: none;
      text-decoration: none;
      transform: skew(-20deg);
      transition: all 0.5s ease .075s;
    }
  </style>
  
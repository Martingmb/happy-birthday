<style>
	p {
  color: #FFFF82;
}

#board {
  font-family: Century Gothic, CenturyGothic, AppleGothic, sans-serif;
  transform: perspective(300px) rotateX(25deg);
  transform-origin: 50% 100%;
  text-align: justify;
  position: absolute;
  margin-left: -9em;
  font-weight: bold;
  overflow: hidden;
  font-size: 350%;
  height: 50em;
  width: 18em;
  bottom: 0;
  left: 50%;
}

#board:after {
  position: absolute;
  content: ' ';
  bottom: 60%;
  left: 0;
  right: 0;
  top: 0;
}

#content {
  animation: scroll 100s linear 14s;
  position: absolute;
  top: 100%;
}

#title, #subtitle {
  text-align: center;
}

@keyframes scroll {
    0% {
        top: 100%;
    }
    100% {
        top: -170%;
    }
}
</style>

<div id="board">  
  <div id="content">
    <p id="title">Episode XXIV</p>
    <p id="subtitle">THE CHOSEN ONE</p>
    <br>
    <p>Exciment and happiness has engulfed the Galaxy as a special day has come.</p>  
		<p>Today on the 14th of June the galaxy celebrates the JEDI KNIGHT Reny.</p>
		<p>She is celebrated for being an awesome, caring and kind friend.</p>
		<p>During this special day, I wish her the very best, for I know she will continue to inspire, help and 
			be an impactful person to others.</p>   
		<p>I'll always treasure our friendship, for the years that passed and the many ones to come...</p> 
  </div>  
</div>
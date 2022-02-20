---
layout: date
title: "Jacqueline and our new normal"
background: "C8A2C8"
textColor: "153266"
buttonColor: "E6E6FA"
buttonTextColor: "153266"
---

# The text changed, Jacqueline

Yeah there's more to read now. And it's gonna get sappy for a sec.

I'm really enjoying talking to you even though we don't get to overlap much. Life's kinda fucked for you right now and it's not fair, but I'm glad to be able to share in some of it and hopefully make some moments a little better. Also you're kind of a badass sexy consultant Saudi princess and like you will absolutely persevere the shit out of this.

Okay.

Onto the good stuff.

It's almost time for some screaming about Shaina. Some decimation of Danielle. Some slamming of Shake. 

**Visit this page from your laptop at 7pm \~~Arabian Time~~ on Sunday, 2/20**

<div id="container">
<h2 id="title">Hot cyber date begins in...</h2>
<div id="countdown">
    <ul>
      <li><div id="days"></div>days</li>
      <li><div id="hours"></div>Hours</li>
      <li><div id="minutes"></div>Minutes</li>
      <li><div id="seconds"></div>Seconds</li>
    </ul>
</div>

<script>
  let params = `scrollbars=no,resizable=yes,status=no,location=no,toolbar=no,menubar=no,
width=400,height=600,left=0,top=0`;

function go() {
  window.open('https://facetime.apple.com/join#v=1&p=zKw/JXs7Eey0Mpqq9oWKQA&k=jIRj_XUR3aAK0a1wfEGfGF3hkz2s2luvS_h9Mnqva_Y&l=Hot%20date', 'Cyberdate', params);
  setTimeout(3000, () => {
    window.location = "";
  })
}
</script>

<div id="instructions" style="display:none;">
  <h3>Okay so this one is kinda complicated</h3>
  <ol>
  <li> First <button onclick="go()">CLICK THIS</button> for FaceTime </li>
  <li> Second <a target="_blank" href="https://chrome.google.com/webstore/detail/netflix-party/oocalimimngaihdkbihfgmpkcpnmlaoa?hl=en">DOWNLOAD THIS</a></li>
  <li> Finally <a href="https://redirect.teleparty.com/join/eab78206634950fb">GO HERE</a> and then click the TP icon</li>
  </ol>
</div>
</div>



<script>
// Set the date we're counting down to
var countDownDate = new Date("2022-02-20T19:00:00+03:00").getTime();
// var countDownDate = new Date("2022-01-22T08:07:00+03:00").getTime();

// Update the count down every 1 second
var x = setInterval(function() {

  // Get today's date and time
  var now = new Date().getTime();

  // Find the distance between now and the count down date
  var distance = countDownDate - now;

  // Time calculations for days, hours, minutes and seconds
  var days = Math.floor(distance / (1000 * 60 * 60 * 24));
  var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
  var seconds = Math.floor((distance % (1000 * 60)) / 1000);

    document.getElementById("days").innerText = days,
    document.getElementById("hours").innerText = hours,
    document.getElementById("minutes").innerText = minutes,
    document.getElementById("seconds").innerText = seconds;

  // If the count down is finished, write some text
  if (distance < 0) {
    clearInterval(x);
    document.getElementById("countdown").innerHTML = "";
    document.getElementById("title").innerText = "Hot cyber date begins NOW!"
    document.getElementById("instructions").style.display = "inline-block";
  }
}, 1000);
</script>

<style>
  #container {
  margin: 0 auto;
  text-align: center;
}

#instructions {
  display: inline-block;
  margin: 0 auto;
  text-align: left;
}

#container #title {
  font-weight: normal;
  letter-spacing: .125rem;
  text-transform: uppercase;
}

#countdown li {
  display: inline-block;
  font-size: 1.5em;
  list-style-type: none;
  padding: 1em;
  text-transform: uppercase;
}

li div {
  display: block;
  font-size: 4.5rem;
  margin-bottom: 1.5rem;
}

.confetti-button {
  display: inline-block;
  font-size: 1em;
  padding: 1em 2em;
  -webkit-appearance: none;
  appearance: none;
  background-color: #B01C1C;
  color: #EEE;
  border-radius: 4px;
  border: none;
  cursor: pointer;
  position: relative;
  transition: transform ease-in 0.1s, box-shadow ease-in 0.25s;
  box-shadow: 0 2px 25px rgba(238,38,37, 0.5);
    animation-iteration-count: infinite;

}

.confetti-button:focus { outline: 0; }

.confetti-button:before, .confetti-button:after {
  position: absolute;
  content: '';
  display: block;
  width: 140%;
  height: 100%;
  left: -20%;
  z-index: -1000;
  transition: all ease-in-out 0.5s;
  background-repeat: no-repeat;

}

.confetti-button:before {
  display: none;
  top: -75%;
  background-image: radial-gradient(circle, #EE2625 20%, transparent 20%), radial-gradient(circle, transparent 20%, #EE2625 20%, transparent 30%), radial-gradient(circle, #EE2625 20%, transparent 20%), radial-gradient(circle, #EE2625 20%, transparent 20%), radial-gradient(circle, transparent 10%, #EE2625 15%, transparent 20%), radial-gradient(circle, #EE2625 20%, transparent 20%), radial-gradient(circle, #EE2625 20%, transparent 20%), radial-gradient(circle, #EE2625 20%, transparent 20%), radial-gradient(circle, #EE2625 20%, transparent 20%);
  background-size: 10% 10%, 20% 20%, 15% 15%, 20% 20%, 18% 18%, 10% 10%, 15% 15%, 10% 10%, 18% 18%;
}

.confetti-button:after {
  display: none;
  bottom: -75%;
  background-image: radial-gradient(circle, #EE2625 20%, transparent 20%), radial-gradient(circle, #EE2625 20%, transparent 20%), radial-gradient(circle, transparent 10%, #EE2625 15%, transparent 20%), radial-gradient(circle, #EE2625 20%, transparent 20%), radial-gradient(circle, #EE2625 20%, transparent 20%), radial-gradient(circle, #EE2625 20%, transparent 20%), radial-gradient(circle, #EE2625 20%, transparent 20%);
  background-size: 15% 15%, 20% 20%, 18% 18%, 20% 20%, 15% 15%, 10% 10%, 20% 20%;
}

.confetti-button:active {
  transform: scale(0.9);
  background-color: #e60074;
  box-shadow: 0 2px 25px rgba(255, 0, 130, 0.2);
}

.confetti-button.animate:before {
  display: block;
  animation: topBubbles ease-in-out 0.75s forwards;
    animation-iteration-count: infinite;

}

.confetti-button.animate:after {
  display: block;
  animation: bottomBubbles ease-in-out 0.75s forwards;
    animation-iteration-count: infinite;

}
 @keyframes
topBubbles {  0% {
 background-position: 5% 90%, 10% 90%, 10% 90%, 15% 90%, 25% 90%, 25% 90%, 40% 90%, 55% 90%, 70% 90%;
}
 50% {
 background-position: 0% 80%, 0% 20%, 10% 40%, 20% 0%, 30% 30%, 22% 50%, 50% 50%, 65% 20%, 90% 30%;
}
 100% {
 background-position: 0% 70%, 0% 10%, 10% 30%, 20% -10%, 30% 20%, 22% 40%, 50% 40%, 65% 10%, 90% 20%;
 background-size: 0% 0%, 0% 0%, 0% 0%, 0% 0%, 0% 0%, 0% 0%;
}
}
@keyframes
bottomBubbles {  0% {
 background-position: 10% -10%, 30% 10%, 55% -10%, 70% -10%, 85% -10%, 70% -10%, 70% 0%;
}
 50% {
 background-position: 0% 80%, 20% 80%, 45% 60%, 60% 100%, 75% 70%, 95% 60%, 105% 0%;
}
 100% {
 background-position: 0% 90%, 20% 90%, 45% 70%, 60% 110%, 75% 80%, 95% 70%, 110% 10%;
 background-size: 0% 0%, 0% 0%, 0% 0%, 0% 0%, 0% 0%, 0% 0%;
}
}
</style>



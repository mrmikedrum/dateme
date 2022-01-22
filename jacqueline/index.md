---
layout: date
title: "Jacqueline, try 2"
background: "C8A2C8"
textColor: "153266"
buttonColor: "E6E6FA"
buttonTextColor: "153266"
---

# Hi again Jacqueline,

We return to the scene of the crime. 

You flew to another country. I didn't. So now here we are, on the internet.

I would sure like to date you. So let's do that on Sunday. We can get all fancied up and make it a thing. You can vicariously share in some of my wine even though it'll be like 9am. Gonna be a grand old time.

So here's the gimmick: I've got a countdown. What's at the end? Dunno. I mean, don't get your hopes up too high. I did this in a day okay.

**Visit this page from your phone at 7pm \~~Arabian Time~~ on Sunday, 1/23**

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

<a class="button" id="link" style="display:none;" href="https://facetime.apple.com/join#v=1&p=zKw/JXs7Eey0Mpqq9oWKQA&k=jIRj_XUR3aAK0a1wfEGfGF3hkz2s2luvS_h9Mnqva_Y&l=Hot%20date">Join my hot date</a>
</div>


<script>
// Set the date we're counting down to
var countDownDate = new Date("2022-01-23T18:00:00+03:00").getTime();
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
    document.getElementById("title").innerText = "Hot date begins NOW!"
    document.getElementById("link").style.display = "inline";
  }
}, 1000);
</script>

<style>
    #container {
  margin: 0 auto;
  text-align: center;
}

#container #title {
  font-weight: normal;
  letter-spacing: .125rem;
  text-transform: uppercase;
}

    li {
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
</style>



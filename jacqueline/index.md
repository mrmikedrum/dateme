---
layout: date
title: "Jacqueline, our time has come"
background: "C8A2C8"
textColor: "153266"
buttonColor: "E6E6FA"
buttonTextColor: "153266"
---

# It's finally happening, Jacqueline

TWO MONTHS LATER, our time has come. Covid couldn't stop this. International work trips couldn't stop this. Me saying Fuck You after asking you to tell me to go to sleep couldn't stop this. 

The real test. Do we hate each other? Is love truly ~~blind~~ possible through long distance snapchat?

We're gonna get some sushi in you. But I assume you're gonna be miserable with jet lag and life commitments upon coming home for the first time in two months... so rather than have some completely unromantic logistical conversations, we're gonna leave that up to the magic of your custom website to help you pick a time. The website will let me know what you picked ✨

<form id="date">
<div class="middle">
  <h1>Pick your date</h1>
  <label>
  <input type="radio" name="date" value="2022-03-13" checked/>
  <div class="box">
    <span>Sunday March 13</span>
  </div>
</label>

  <label>
  <input type="radio" name="date" value="2022-03-14" />
  <div class="box">
    <span>Monday March 14</span>
  </div>
</label>

  <label>
  <input type="radio" name="date" value="2022-03-15" />
  <div class="box">
    <span>Tuesday March 15</span>
  </div>
</label>

<h1>Pick your time</h1>
  <label>
  <input type="radio" name="time" value="5pm" checked/>
  <div class="box">
    <span>5pm</span>
  </div>
</label>

  <label>
  <input type="radio" name="time" value="6pm" />
  <div class="box">
    <span>6pm</span>
  </div>
</label>

  <label>
  <input type="radio" name="time" value="7pm" />
  <div class="box">
    <span>7pm</span>
  </div>
</label>
</div>
</form>


---

We're going here. I'll pick you up.

<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d26990.360550731788!2d-110.93045932686508!3d32.263595631818326!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x86d66fb469015361%3A0xefa5ce2a74487dc6!2sTakamatsu!5e0!3m2!1sen!2sus!4v1647099688854!5m2!1sen!2sus" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy"></iframe>

<script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>

<script>

  function getCheckedValue( groupName ) {
    var radios = document.getElementsByName( groupName );
    for( i = 0; i < radios.length; i++ ) {
        if( radios[i].checked ) {
            return radios[i].value;
        }
    }
    return null;
}

const instance = axios.create({
  timeout: 1000,
  headers: {'Authorization': 'Bearer keybGPgYPaQmoLF7T'} //yeah I know I just put this in the clear it's gonna get invalidated in a day okay
});

const form = document.getElementById("date");

// set initial state

instance.get('https://api.airtable.com/v0/appP324ZYPLEeJcj4/Jacqueline%20Dates/rechzY0b5xmY9yMES').then(resp => {
  console.log(resp.data)
  if(!!resp.data.fields) {
    form.elements["date"].value = resp.data.fields["Start date"];
    form.elements["time"].value = resp.data.fields["time"];
  } else {
    alert('shit. something went wrong. tell mike.')
  }
}, err => {
  alert('shit. something went wrong. tell mike this: ' + err.message)
})

// change state with form events

form.addEventListener('change', (event) => {
  instance.patch('https://api.airtable.com/v0/appP324ZYPLEeJcj4/Jacqueline%20Dates/rechzY0b5xmY9yMES', {
      "fields": {
        "Name": "Takamatsu",
        "Start date": getCheckedValue("date"),
        "time": getCheckedValue("time")
      }
  })
});
</script>

<style>

.middle {
  width: 100%;
  text-align: center;
}
.middle h1 {
  font-family: "Inter", sans-serif;
  color: #fff;
}
.middle input[type=radio] {
  display: none;
}
.middle input[type=radio]:checked + .box {
  background-color: #E6E6FA;
}
.middle input[type=radio]:checked + .box span {
  color: 153266;
  transform: translateY(35px);
}
.middle input[type=radio]:checked + .box span:before {
  transform: translateY(0px);
  opacity: 1;
}
.middle .box {
  width: 200px;
  height: 100px;
  background-color: #fff;
  transition: all 250ms ease;
  will-change: transition;
  display: inline-block;
  text-align: center;
  cursor: pointer;
  position: relative;
  font-family: "Inter", sans-serif;
  font-weight: 900;
}
.middle .box:active {
  transform: translateY(10px);
}
.middle .box span {
  position: absolute;
  transform: translate(0, 40px);
  left: 0;
  right: 0;
  transition: all 300ms ease;
  font-size: 1.5em;
  user-select: none;
  color: #007e90;
}
.middle .box span:before {
  font-size: 1.2em;
  font-family: FontAwesome;
  display: block;
  transform: translateY(-80px);
  opacity: 0;
  transition: all 300ms ease-in-out;
  font-weight: normal;
  color: white;
}
.middle .front-end span:before {
  content: "";
}
.middle .back-end span:before {
  content: "";
}
.middle p {
  color: #fff;
  font-family: "Inter", sans-serif;
  font-weight: 400;
}
.middle p a {
  text-decoration: underline;
  font-weight: bold;
  color: #fff;
}
.middle p span:after {
  content: "";
  font-family: FontAwesome;
  color: yellow;
}
</style>



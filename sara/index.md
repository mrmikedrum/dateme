---
layout: date
title: Princess Sara's Birthday
---

# It's your birthday, Princess Sara

Let's get some fuckin soup in you. Just let me know when and where.

<form id="date">
<div class="middle">
  <h1>Pick your place</h1>
  <label>
  <input type="radio" name="place" value="Delivery" checked/>
  <div class="box">
    <span>Delivery</span>
  </div>
</label>

  <label>
  <input type="radio" name="place" value="Mike's" />
  <div class="box">
    <span>Visit</span>
  </div>
</label>


<h1>Pick your time</h1>
  <label>
  <input type="radio" name="time" value="12pm" checked/>
  <div class="box">
    <span>12pm</span>
  </div>
</label>

  <label>
  <input type="radio" name="time" value="5pm" />
  <div class="box">
    <span>5pm</span>
  </div>
</label>

  <label>
  <input type="radio" name="time" value="6pm" />
  <div class="box">
    <span>6pm (Delivery only)</span>
  </div>
</label>
</div>
</form>

<div class="demo-wrap">
  <img
    class="demo-bg"
    src="{{ '/assets/img/soup.jpeg' | relative_url }}"
    alt=""
  >
</div>

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
  timeout: 10000,
  headers: {'Authorization': 'Bearer keybGPgYPaQmoLF7T'} //yeah I know I just put this in the clear it's gonna get invalidated in a day okay
});

const form = document.getElementById("date");

// set initial state

instance.get('https://api.airtable.com/v0/appP324ZYPLEeJcj4/Sara%20date/rechaQELbn7ef8A99').then(resp => {
  console.log(resp.data)
  if(!!resp.data.fields) {
    form.elements["place"].value = resp.data.fields["Place"];
    form.elements["time"].value = resp.data.fields["Time"];
  } else {
    alert('shit. something went wrong. tell mike.')
  }
}, err => {
  alert('shit. something went wrong. tell mike this: ' + err.message)
})

// change state with form events

form.addEventListener('change', (event) => {
  instance.patch('https://api.airtable.com/v0/appP324ZYPLEeJcj4/Sara%20date/rechaQELbn7ef8A99', {
      "fields": {
        "Name": "Birthday",
        "Place": getCheckedValue("place"),
        "Time": getCheckedValue("time")
      }
  })
});
</script>

<style>

.demo-bg {
    z-index: -1;
  opacity: 0.6;
  position: absolute;
  left: 0;
  top: -20px;
  min-width: 100%;
}

.demo-content {
  position: relative;
}

.middle {
  width: 100%;
  text-align: center;
}
.middle h1 {
  font-family: "Inter", sans-serif;
  color: #222;
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



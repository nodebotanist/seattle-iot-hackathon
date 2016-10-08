# Webtask.io

---

# Hey! I'm Kas

* Developer Evangelist at Auth0
* Webtask.io afficionado
* Also pretty good at Auth (OAuth, OIDC, etc.)

![inline](GIFS/nolife.gif)

---

# I'm also a hardware hacker

* In-Progress EE degree
* Tessel open-source committee member
* I wrote a book on JS Robotics

---

# No one wants to spin up a new web server to handle webhooks on a time crunch.

![inline](GIFS/nopenopenope.gif)

---

# That's where we come in

```
var Particle = require('particle-api-js')
var particle = new Particle()
module.exports = function(context, req, res) {
  var particleToken = context.secrets.PARTICLE_ACCESS_TOKEN
  var deviceId = context.secrets.PARTICLE_DEVICE_ID

  var color = context.query.Body || context.query.color || '#000000'

//...color conversion...

  particle.callFunction({ deviceId, name: 'pixels', argument: color, auth: particleToken
  }).then(
    (data) => {
      res.writeHead(200, { 'Content-Type': 'text/html '});
      res.end('Success');
    }
  )
}
```

---

Install the cli and deploy your code, and voila! A webhook URL

```
> npm i -g wt-cli
```

```
> wt create --name SeattleDemo 
	--secret PARTICLE_ACCESS_TOKEN=AUTH_TOKEN 
	--secret PARTICLE_DEVICE_ID=DEVICE_ID 
	webtask.js
```

(Also, did I mention we have a free plan?)

---

# (Text (512) 831-7291 with a color (#663399 or orange, for example))

---

# Stop by if you need assistance with:

* Webtask.io (of course)
* Auth0 
* Hardware debugging (I brought half a lab with me!)
* You can even book a time slot https://slotted.co/sea-int-nodebotanist

---

# Best use of Webtask: this team wins Johnny-Five Inventor's kits and copies of "Learning Javascript Robotics[^1]"

[^1]: Disclaimer: I wrote that book.

---

# TL;DL

* I'm Kas
* Webtask.io is rad
* Ask me about that, hardware, or auth!
* http://seattle.nodebotani.st
* https://slotted.co/sea-int-nodebotanist for appointments
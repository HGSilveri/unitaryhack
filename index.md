---
layout: page
title:
---
<script>
(function () {
  const second = 1000,
    minute = second * 60,
    hour = minute * 60,
    day = hour * 24;
 
  let hack = "May 14, 2021 00:00:00",
    countDown = new Date(hack).getTime(),
    x = setInterval(function () {
      let now = new Date().getTime(),
        distance = countDown - now;
 
      (document.getElementById("days").innerText = Math.floor(distance / day)),
        (document.getElementById("hours").innerText = Math.floor(
          (distance % day) / hour
        )),
        (document.getElementById("minutes").innerText = Math.floor(
          (distance % hour) / minute
        )),
        (document.getElementById("seconds").innerText = Math.floor(
          (distance % minute) / second
        ));
 
      //do something later when date is reached
      if (distance < 0) {
        let headline = document.getElementById("headline"),
          countdown = document.getElementById("countdown"),
          content = document.getElementById("content");
 
        headline.innerText = "WE ARE LIVE! GET HACKING 💛🌴";
        countdown.style.display = "none";
        content.style.display = "block";
 
        clearInterval(x);
      }
      //seconds
    }, 0);
})();
 
</script>

<div class="container">
  <h4 id="headline">The hacking starts in:</h4>
  <div id="countdown">
  <table>
    <tr>
        <td style="font-size:3em"><span id="days"></span></td>
        <td style="font-size:3em"><span id="hours"></span></td>
        <td style="font-size:3em"><span id="minutes"></span></td>
        <td style="font-size:3em"><span id="seconds"></span></td>
    </tr>
    <tr>
      <td>Days</td>
      <td>Hours</td>
      <td>Minutes</td>
      <td>Seconds</td>
    </tr>
    </table>
  </div>
</div>

<figure>
<img style="max-width: 60%;
        height: auto; margin: auto;
  display: block;" src="./assets/logo-date.png" alt="New York" />
<figcaption style="max-width: 60%;
        height: auto; margin: auto;
  display: block;font-size:.8em">
<br>Quantum computing isn’t just unitary, it’s open source!
</figcaption>
</figure>

### The Unitary Fund is proud to host our first quantum open source hackathon with SWAG and BOUNTIES on **May 14-30th**!

- 💰 Over $2K in bounties for tagged issues in quantum open source projects

- 💿 Digital swag for all participants that make approved Pull Requests (PR)s

- 🎁 Random participants that make 1 **quality** Pull Request (PR)s to a participating open source project will receive a [swag pack in the mail!*](./rules.md)

<button style="max-width: 60%;height: auto; margin: auto;display: block;background-color:#ffff00;border-width:0em;font:'Lucida Console', monospace, !default;font-size:2em;" type="button" onclick="location='https://airtable.com/embed/shrTG20PLC5cjVIPr'"><b>SIGN UP HERE!</b></button>

You can find some tips on how to prepare for the hackathon in our [hacker guide](./hacker-guide.md) as well as the [hackathon rules](./rules.md), and you can always ask questions of the Unitary Fund team on our [Discord](http://discord.unitary.fund), and make sure to check out [our code of conduct](CODE_OF_CONDUCT.md).
### Are you a maintainer?

We would love to support your quantum open source project by connecting eager hackers to issues you need help with!
Check out our [maintainer guide](./maintainer-guide.md)

### Thanks to our supporters

- [Unitary Fund](https://unitary.fund/)
- [Xanadu](https://xanadu.ai/)
- [PASQAL](https://pasqal.io/)

#### Support this project🙏

Would you like to help us support more contributors and projects? [Get in touch](mailto:info@unitary.fund?subject=[UnitaryHack]%20Supporting%20You) with us!

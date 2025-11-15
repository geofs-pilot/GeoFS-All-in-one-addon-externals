Failures and fuel: <br/>
-failures: delete original fuel leak, change it to set a global variable to true to trigger fuel leak logic in fuel addon <br/>
-fuel leak logic in fuel addon - additive, including engine burn rate and stuff<br/>
-delete fuel display and move it to info display<br/>
-failures: line 313:     if (this.enabled) { changed to if (this.enabled && !window.flight.recorder.playing && !window.geofs.pause) {<br/>
	-line 103:        if (!system.includes("engine") && !flight.recorder.playing) {<br/>
-hide fail button when flight recorder playing<br/>
-change fail button css to be red, smaller, bottom right corner<br/>
window.failBtn.style.position="fixed";<br/>
window.failBtn.style.right="60px";<br/>
window.failBtn.style.height="36px";<br/>
window.	failBtn.style.bottom="0px";<br/>
window.failBtn.style.border="transparent";<br/>
window.failBtn.style.background="rgb(255,0,0)";<br/>
window.failBtn.style.color="white";<br/>
window.failBtn.style.fontWeight="600";<br/>
window.failBtn.style.fontSize="20px";<br/>
window.failBtn.style.cursor="pointer";<br/>
window.failBtn.style.zIndex="10000",document.body.appendChild(window.failBtn);<br/>
window.failBtn.innerHTML='<button style="position: inherit; right: inherit; height: inherit; top: inherit; border: inherit; background: inherit; color: inherit; font-weight: inherit; fontSize: inherit; cursor: inherit;" onclick="window.openFailuresMenu()">FAIL</button>';<br/>
setInterval(() => {<br/>
if (flight.recorder.playing) {<br/>
   	 failBtn.style.display = "none"<br/>
} else {<br/>
   	 failBtn.style.display = "block"<br/>
}<br/>
}, 100);<br/>
https://github.com/tylerbmusic/GeoFS-Failures/blob/main/userscript.js <br/>
version of userscript.js: June 6 2025 <br/>
https://github.com/geofs-pilot/GeoFS-Fuel <br/>
version of main.js: May 28 2025 <br/>

Flightradar: <br/>
identical files, but needed a file different than user.js <br/>
https://github.com/seabus0316/GeoFS-flightradar/tree/main <br/>
version of user.js: Nov 11 2025 <br/>

Maritime structures: <br/>
fixed spawnHTML() to not break info display <br/>
https://github.com/CementAndRebar/GeoFS-Extra-Maritime-Structures/blob/main/main.js <br/>
version of main.js: 2023 <br/>

Overpowered Engines: <br/>
deleted UI notifications <br/>
removed redundant waitForGeoFS function <br/>
https://github.com/geofs-pilot/geofs-overpowered-engines/blob/main/userscript.js <br/>
version of userscript.js: Nov 13 2025 <br/>

Utilities: <br/>
deleted autobrake function <br/>
https://github.com/tylerbmusic/geofs-utilities/blob/main/userscript.js <br/>
version of userscript.js: Sept 8 2025 <br/>

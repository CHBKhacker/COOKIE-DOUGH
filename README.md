# COOKIE DOUGH

- prevents securly, securly classroom, goguardian, and hapara from working, may work on other extensions
- can be used as a bookmarklet or as a custom search engine (chrome://settings/searchEngines)
- great for if you can't use custom DNS servers or if the chrome://signOut exploit breaks stuff
- adjustable size multiplier

instructions:
1. go to a blocked page (or securly.com for securly (+ classroom), or goguardian.com for goguardian)
2. run the code using a bookmarklet or a custom search engine
3. enter a size multiplier. use 10 for securly (in 2022, may have to be increased in the future)
4. done!

code:
javascript:(e=>{for(var o=32*(parseInt(prompt("Size Multiplier","1"))||1),t=new Date(2e14).toUTCString(),n=location.hostname.split(".").slice(-2).join("."),r=0;r<100;r++)document.cookie=`cd${r}=${encodeURIComponent(btoa(String.fromCharCode.apply(0,crypto.getRandomValues(new Uint8Array(o))))).substring(0,o)};expires=${t};domain=${n};path=/`;alert("OK")})();

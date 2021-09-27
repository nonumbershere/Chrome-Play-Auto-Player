## Install
1) Go to index.js
2) Copy the code
3) Go to Chrome Play
4) Hit F12 or CTRL-SHIFT-I, for Mac its CMD + OPTION + J.
5) Paste the code in the console tab
6) You're done! Check the Help section for commands.

## Help
You can do 'play("fDfD", 100,100,1000)' in the console.
```js
play(sheets,speed,shortspeed,longspeed)
```
![image](https://user-images.githubusercontent.com/64395933/134837610-d863608b-2057-4e31-893f-1934e47e2bab.png)

## Examples
***Fur Elise***
```js
console.log("%cChrome Play Auto Player by Lapide!","color: red; font-size: 50px");var playedNotes=0,maxNotes=0;function isNumeric(e){return"string"==typeof e&&(!isNaN(e)&&!isNaN(parseFloat(e)))}function waitPlay(e,l){setTimeout(function(){" "==!e&&("!"==e?new Audio("../../audio/Digit1-1.mp3").play():"@"==e?new Audio("../../audio/Digit2-2.mp3").play():"#"==e?new Audio("../../audio/Digit3-3.mp3").play():"$"==e?new Audio("../../audio/Digit4-4.mp3").play():"%"==e?new Audio("../../audio/Digit5-5.mp3").play():"^"==e||("&"==e?new Audio("../../audio/Digit6-6.mp3").play():"&"==e?new Audio("../../audio/Digit7-7.mp3").play():"*"==e?new Audio("../../audio/Digit8-8.mp3").play():"("==e?new Audio("../../audio/Digit9-9.mp3").play():")"==e?new Audio("../../audio/Digit0-0.mp3").play():isNumeric(e)?new Audio("../../audio/Digit"+e+".mp3").play():e==e.toLowerCase()?new Audio("../../audio/Key"+e+".mp3").play():new Audio("../../audio/Key"+e+"-"+e+".mp3").play())),++playedNotes,console.log("%cPlayed note: %c"+e,"color: darkblue","color: lightblue"),playedNotes==maxNotes&&console.log("%cFinished!","color: green")},l)}function play(e,l,i,a){var o=l;maxNotes=e.replaceAll("\n"," ").replaceAll(" ","").replaceAll("-","").replaceAll("]","").replaceAll("[","").length;for(var p=e.replaceAll("\n"," ").split(" "),t=0;t<p.length;++t)if("-"==p[t])o+=a,waitPlay(p[t].replaceAll("-",""),o);else if(p[t].startsWith("[")&&p[t].endsWith("]")){for(var n=p[t].replace("[","").replace("]","").split(""),r=0;r<n.length;++r)waitPlay(n[r],o);o+=l}else if(p[t].length>1){for(var u=p[t].replaceAll(" ","").replaceAll(""," ").slice(1,p[t].replaceAll(" ","").replaceAll(""," ").length-1).split(" "),d=0;d<u.length;++d)waitPlay(u[d],o),o+=i;o+=i}else waitPlay(p[t],o),o+=l}

play(`f D f D f a d s [p6] 0 e t u p [3a] 0 u O a [6s] 0 e u
f D f D f a d s [p6] 0 e t u p [3a] 0 W u s a [6p] 0 e
f D f D f a d s [p6] 0 e t u p [3a] 0 u O a [6s] 0 e u
f D f D f a d s [p6] 0 e t u p [3a] 0 W u s a [6p] 0 e t u p [3a] 0 W u s a [6p] 0 e
a s d [8f] w t o g f [5d] w r i f d [6s] 0 e u d s [3a] 0 u u f u f f x
D f D f D f D f D f D f a d s [p6] 0 e t u p [3a] 0 W u s a [6p] f D f D f a d s [p6]
0 e t u p [a7]
0 W u O a [s6]
f D f D f a d s [p6]
0 e t u p [a7]
0 W u O s a [p6]
0 e a s d [f7]
w t o g f [d6]
w r i f d [s5]
0 e u d s [a3]
0 u f u f f x D f D f D f D f D f D f D f a d s [p6]
0 e t u p [a7]
0 W u O a [s6]
f D f D f a d s [p6]
0 e t u p [a7]
0 W u O s a [p6]`,200,100,1000)
```

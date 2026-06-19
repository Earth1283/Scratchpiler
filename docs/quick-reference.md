# Quick Reference

Everything on one page. For detailed explanations, follow the links to the relevant doc.

---

## Script structure

```
on flag { }              // green flag
on click { }             // sprite clicked
on clone { }             // started as a clone
on key "space" { }       // key pressed
on receive "msg" { }     // broadcast received
on backdrop "name" { }   // backdrop switched to
on timer > 10 { }        // timer exceeds value
on loudness > 50 { }     // microphone loudness exceeds value

define blockName(p1, p2) { }   // custom block definition
```

---

## Control flow

```
if condition { }
if condition { } else { }

repeat 10 { }
forever { }
repeat until (condition) { }
while (condition) { }
for [i] from 1 to 10 { }

wait(seconds)
wait until condition

stopAll()
stopThis()
stopOtherScripts()
createClone()
createClone("SpriteName")
deleteClone()
yield()                  // pause one tick (= wait 0)
```

---

## Variables

```
set [x] to value
change [x] by amount
[x] += n    [x] -= n    [x] *= n    [x] /= n

showVariable([x])
hideVariable([x])
```

---

## Lists

```
listAdd(item, [list])
listDelete(index, [list])
listDeleteAll([list])
listInsert(item, index, [list])
listReplace(index, [list], item)
showList([list])
hideList([list])

[list].length()          // number of items
[list].item(index)       // item at 1-based index
[list][i]                // shorthand for .item([i])
[list].contains(value)   // boolean
[list].indexOf(value)    // 1-based index, or 0 if absent
```

---

## Motion

```
move(steps)
turnRight(degrees)
turnLeft(degrees)
setDirection(degrees)    // 0=up 90=right 180=down -90=left
pointTowards("target")   // "_mouse_" or sprite name
goTo(x, y)
goTo("target")
glide(secs, x, y)
glide(secs, "target")
setX(x)   setY(y)
changeX(dx)   changeY(dy)
bounce()
setRotationStyle("all around" | "left-right" | "don't rotate")
goToFront()   goToBack()
moveForward(n)   moveBackward(n)

// Reporters
xPos   yPos   direction
distanceTo("target")
```

---

## Looks

```
say(message)
sayFor(message, secs)
think(message)
thinkFor(message, secs)
switchCostume("name")
nextCostume()
switchBackdrop("name")
switchBackdropAndWait("name")
nextBackdrop()
setSize(percent)
changeSize(amount)
show()   hide()
setEffect("effect", value)    // color fisheye whirl pixelate mosaic brightness ghost
changeEffect("effect", amount)
clearEffects()

// Reporters
size   costumeNum   costumeName
```

---

## Sound

```
play("name")
playUntilDone("name")
stopSounds()
setVolume(percent)
changeVolume(amount)
setSoundEffect("PITCH" | "PAN LEFT/RIGHT", value)
changeSoundEffect("PITCH" | "PAN LEFT/RIGHT", amount)
clearSoundEffects()

// Reporter
volume
```

---

## Events

```
broadcast("message")
broadcastAndWait("message")
```

---

## Sensing

```
touching("_edge_" | "_mouse_" | "SpriteName")  // boolean
key("key name")                                 // boolean
askAndWait("question")
answer       mouseDown      mouseX    mouseY
timer        loudness       size
costumeNum   costumeName    volume
username     daysSince2000
resetTimer()
currentTime("year" | "month" | "date" | "day" | "hour" | "minute" | "second")
distanceTo("target")
xOf("sprite")   yOf("sprite")   directionOf("sprite")
costumeNumOf("sprite")   costumeNameOf("sprite")
sizeOf("sprite")         volumeOf("sprite")
setDragMode("draggable" | "not draggable")
```

---

## Math functions

```
abs(n)       round(n)     floor(n)    ceiling(n)    ceil(n)
sqrt(n)      exp(n)       pow10(n)    ln(n)         log(n)
sin(deg)     cos(deg)     tan(deg)
asin(n)      acos(n)      atan(n)
random(min, max)
clamp(value, min, max)
```

---

## String / operator functions

```
join(str1, str2)
letterOf(index, string)       // 1-based
contains(string, substring)   // boolean
"string".length()
[var].length()
```

---

## Operators

```
+  -  *  /  mod           // arithmetic
<  >  =                   // comparison (no <=, >=, !=)
and  or  not              // boolean
```

---

## Literals

```
42          3.14          -5          // numbers
"hello"                               // strings (double quotes only)
[varName]                             // variable reference
#ff6600                               // hex color
```

---

## Comments

```
// Everything after // is ignored by the compiler
```

---

## Key names (for `on key` and `key()`)

`"space"` `"enter"` `"up arrow"` `"down arrow"` `"left arrow"` `"right arrow"`  
`"a"` through `"z"` &nbsp;&nbsp; `"0"` through `"9"`

---

## Keyboard shortcuts

| Key | Action |
|---|---|
| `Alt+M` | Open / close scratchpiler |
| `Ctrl+Enter` | Compile & inject |
| `Ctrl+S` | Compile & inject |
| `Alt+Shift+F` | Format / auto-indent |
| `Ctrl+Space` | Trigger autocomplete |
| `Esc` | Close overlay |

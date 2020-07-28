# multiprocessing
A rhythm game made with HTML5 and JavaScript.

## Fish Part
> - A fish is swimming through rings.
> - You have to press F when the fish goes through the rings.

## Ball Part
> - Some balls are falling onto the ground.
> - You have to press J when the ball hits the ground.

## Shoot Part
> - A target is approaching to your aim.
> - You have to press D when the target is perfectly aimmed.

## Draw Part
> - I made it but I actually don't know what it is.
> - You have to press K when notes are passing the long line. (Long note available)

# Level Editing
> I made a template .html file so that everyone can create their own levels in the same way as I do.
[template.html](./template.html)

## How to
### To set Audio File
```js
let audioFile = "audio.ogg";
```
> Plays "audio.ogg" as the game starts.

### To set BPM,
```js
['b', 120, 1]
```
> BPM: 120, Offset: 1s

If you want to change it again,
```js
['b', 120, 1], ..., ['b', 180, 1]
```
> BPM: 180, Offset: 1.5s (from the beginning of the audio)

The offset works along the bpm. The default bpm is 60, so you can set it in seconds in the initial setting.

### To add a note,
```js
['n', 0, 10], ['n', 1, 11], ['n', 2, 12], ['n', 3, 13], ['n', 3, 14, 2]
```
> Fish note on 10th beat, Ball note on 11th beat, Shoot note on 12th beat, Draw notes on 13th and 14th~16th beat.

### Add these together,
```js
let crochet = [['b', 120, 1], ['n', 0, 0], ['n', 1, 1], ['n', 3, 2], ['n', 2, 5]];
```

## Gimmick Patterns
High-end users may make some gimmick patterns in their levels.
```js
function gimmick() { // Code before the graphics are completely drawn.
    return false; // return true if you want to disable ignoring notes that might appear later.
}
function lategimmick() { // Code after the graphics are completely drawn.
    // pass;
}
```
You can refer to the gameplay.js file as you make gimmick patterns, but you may not modify it for compability. ~~I appologize because I didn't make enough comments and the fish image is in base64 code :(~~

Soon I will add comments to gameplay.js file, so please wait.

# Song Recommendation
I need free songs that can be used in a game. And it is so hard to find.
Please give me if you know some.
[Recommend](https://forms.gle/gfuV5SA6aCqFhMpTA)

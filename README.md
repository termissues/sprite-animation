## About
Sprite animations are animation clips that will play each Sprite in order to create the animation, much like a <a href="https://en.wikipedia.org/wiki/Flip_book">flipbook</a>.

## Objectives:
- [x] \(Use .png file) Make a Sprite animation with it
- [x] \(Add a dropdown) Make a dropdown and add animation options
- [x] \(Use JavaScript) By using JavaScript make something interesting with animations
- [ ] \(Try new things) Make a web game with Sprite animations

## Animate function()
```js
function animate() {
    ctx.clearRect(0, 0, CANVAS_WIDTH, CANVAS_HEIGHT);
    let position = Math.floor(gameFrame/staggerFrames) % spriteAnimations[playerState].loc.length;
    let frameX = spriteWidth * position;
    let frameY = spriteAnimations[playerState].loc[position].y;
    
    ctx.drawImage(playerImage, frameX, frameY, spriteWidth, spriteHeight, 0, 0, spriteWidth, spriteHeight);
    
    gameFrame++;
    requestAnimationFrame(animate);
};
animate();
```
## Final product

<img src="https://i.imgur.com/i2N0R2Q.png" />

# sample game tutorial

Once the editor loads, you will see a green ``||loops:on start||`` block already in the editor Workspace

### ~avatar avatar

Help info

### ~


### ~hint

#### Hint Title
Help content
alternative hint, alert, reminder, tip
### ~


## ~button /writing-docs/tutorials

NEXT: Tutorials, hyperlink

## ~


``|primary button|``

``||secondary button||``


Set your text variable like this: ``[let txt = "text"]``


## stage one: make a sprite and position it on the screen
make the first sprite and set its position to near the top left corner
```blocks
let mySprite = sprites.create(img`
    . . . . . . . . . . b 5 b . . .
    . . . . . . . . . b 5 b . . . .
    . . . . . . b b b b b b . . . .
    . . . . . b b 5 5 5 5 5 b . . .
    . . . . b b 5 d 1 f 5 d 4 c . .
    . . . . b 5 5 1 f f d d 4 4 4 b
    . . . . b 5 5 d f b 4 4 4 4 b .
    . . . b d 5 5 5 5 4 4 4 4 b . .
    . b b d d d 5 5 5 5 5 5 5 b . .
    b d d d b b b 5 5 5 5 5 5 5 b .
    c d d b 5 5 d c 5 5 5 5 5 5 b .
    c b b d 5 d c d 5 5 5 5 5 5 b .
    c b 5 5 b c d d 5 5 5 5 5 5 b .
    b b c c c d d d 5 5 5 5 5 d b .
    . . . . c c d d d 5 5 5 b b . .
    . . . . . . c c c c c b b . . .
`, SpriteKind.Player)
mySprite.setPosition(21, 20)
```

## stage two


## stage complete
```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Player, function (sprite, otherSprite) {
    music.baDing.playUntilDone()
})
let mySprite = sprites.create(img`
    . . . . . . . . . . b 5 b . . .
    . . . . . . . . . b 5 b . . . .
    . . . . . . b b b b b b . . . .
    . . . . . b b 5 5 5 5 5 b . . .
    . . . . b b 5 d 1 f 5 d 4 c . .
    . . . . b 5 5 1 f f d d 4 4 4 b
    . . . . b 5 5 d f b 4 4 4 4 b .
    . . . b d 5 5 5 5 4 4 4 4 b . .
    . b b d d d 5 5 5 5 5 5 5 b . .
    b d d d b b b 5 5 5 5 5 5 5 b .
    c d d b 5 5 d c 5 5 5 5 5 5 b .
    c b b d 5 d c d 5 5 5 5 5 5 b .
    c b 5 5 b c d d 5 5 5 5 5 5 b .
    b b c c c d d d 5 5 5 5 5 d b .
    . . . . c c d d d 5 5 5 b b . .
    . . . . . . c c c c c b b . . .
`, SpriteKind.Player)
controller.moveSprite(mySprite)
mySprite.setPosition(21, 20)
let mySprite2 = sprites.create(img`
    . . . . . . . . . . . . . . . . 8 6 . . . . . . . . . . . . . . . . . .
    . . . . . . . . . . . 6 6 8 8 8 6 7 8 8 6 . . . . . . . . . . . . . . .
    . . . . . . . . . . . 8 6 6 6 8 7 7 6 8 8 8 6 8 . . . . . . . . . . . .
    . . . . . . . . . . . . 8 6 8 7 7 7 7 6 7 7 6 8 . . . . . . . . . . . .
    . . . . . . . . . 6 8 8 6 6 7 7 7 7 7 7 6 6 8 8 . . . . . . . . . . . .
    . . . . . . . . 6 7 7 6 7 7 7 7 7 7 7 7 7 8 6 6 6 . . . . . . . . . . .
    . . . . . . . . . 6 7 7 6 6 6 7 7 6 7 6 6 6 8 6 8 . . . . . . . . . . .
    . . . . . . . . . . 8 6 6 6 6 7 6 6 7 6 7 7 6 8 8 . . . . . . . . . . .
    . . . . . . . . . 8 6 6 6 6 6 6 6 6 6 6 6 7 7 7 8 . . . . . . . . . . .
    . . . . . . . . 6 6 7 7 6 6 6 6 6 6 6 6 6 6 6 6 7 6 . . . . . . . . . .
    . . . . . . . 6 7 7 6 6 6 6 7 6 6 6 7 7 6 6 6 7 7 7 6 . . . . . . . . .
    . . . . . . 8 8 6 6 6 7 7 7 6 6 7 6 7 7 7 6 6 6 6 8 8 . . . . . . . . .
    . . . . . 6 7 7 6 6 7 7 7 6 6 7 7 6 7 7 7 7 6 6 6 7 6 8 . . . . . . . .
    . . . . 6 7 7 6 6 6 6 6 6 6 7 7 7 6 6 7 7 7 6 6 6 6 7 7 6 . . . . . . .
    . . . . . 8 6 6 7 7 7 6 6 6 7 7 6 6 6 7 6 6 7 7 7 7 6 7 7 6 . . . . . .
    . . . . . . 8 7 7 7 6 6 6 6 6 6 6 6 7 7 7 6 7 7 7 7 7 6 6 8 8 . . . . .
    . . . . 6 8 8 7 7 6 6 7 7 6 6 7 7 6 7 7 7 7 7 7 7 7 7 7 6 7 7 6 . . . .
    . . 8 8 6 6 6 6 6 6 7 7 7 6 7 7 7 7 7 7 7 7 7 7 7 6 6 6 6 6 7 7 8 . . .
    . 8 6 6 6 6 6 6 6 7 7 7 6 6 7 7 6 7 7 7 7 7 6 6 6 6 6 7 7 6 6 6 8 . . .
    . . 8 8 6 7 7 6 6 6 6 6 6 7 7 7 6 7 7 6 7 7 6 6 6 6 6 7 7 7 6 6 6 8 . .
    . . 8 6 7 7 6 6 7 7 6 6 6 6 6 6 6 6 6 6 6 6 6 6 7 7 7 6 6 6 6 6 6 8 . .
    8 8 6 6 6 6 6 7 7 7 6 6 6 6 7 6 6 6 6 6 6 7 7 6 6 7 7 7 6 6 6 6 8 . . .
    6 6 6 8 6 6 6 6 7 6 6 6 7 7 6 6 7 6 7 7 6 7 7 6 6 6 7 7 6 6 6 6 6 8 . .
    8 8 8 6 6 6 6 6 6 6 6 7 7 7 6 7 7 6 7 7 6 6 7 6 6 6 6 6 6 7 7 6 6 6 8 .
    . 8 6 6 6 8 8 6 6 6 6 6 7 6 6 7 7 6 7 7 6 6 6 6 6 6 7 7 6 6 6 6 6 6 6 8
    . 8 6 6 8 8 6 6 6 6 6 6 6 6 6 7 7 6 6 6 6 6 6 7 6 6 7 7 7 6 6 6 6 6 8 8
    . 6 6 8 8 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 7 7 6 6 6 6 6 6 6 8 8 . .
    . . 8 8 6 6 6 8 6 6 6 6 6 6 6 6 6 6 6 7 7 6 6 7 7 7 6 6 6 6 6 6 8 . . .
    . . . 8 6 6 8 8 6 6 6 6 6 6 6 6 6 6 6 7 7 6 6 7 7 7 6 6 6 6 6 6 8 . . .
    . . . 8 6 8 8 6 6 6 8 6 6 6 6 6 6 6 6 7 6 6 6 6 6 6 6 6 6 8 8 8 . . . .
    . . . . 8 8 8 6 6 8 8 6 6 8 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 8 . . . . . .
    . . . . . . 8 6 8 8 6 6 6 8 6 6 6 8 6 6 6 6 8 6 6 6 8 6 8 . . . . . . .
    . . . . . . 8 8 8 6 6 6 8 8 6 6 8 8 6 6 6 8 8 8 6 6 8 8 8 . . . . . . .
    . . . . . . . . 8 8 8 8 8 8 8 6 8 8 8 8 8 c e 8 6 8 . . . . . . . . . .
    . . . . . . . . . . . . . . e 8 8 e 8 8 . e c . 8 . . . . . . . . . . .
    . . . . . . . . . . . . . . . e e e e . . e . . . . . . . . . . . . . .
    . . . . . . . . . . . . . . . c e e f . c e . . . . . . . . . . . . . .
    . . . . . . . . . . . . . . . c e e f c e c . . . . . . . . . . . . . .
    . . . . . . . . . . . . . . . f e e f c e . . . . . . . . . . . . . . .
    . . . . . . . . . . . . . . . f c e e e c . . . . . . . . . . . . . . .
    . . . . . . . . . . . . . . . f f c e e c . . . . . . . . . . . . . . .
`, SpriteKind.Player)

```
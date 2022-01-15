# Music to My Ears

```template
    controller.B.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.startEffect(effects.fire, 2000)
    music.playTone(392, music.beat(BeatFraction.Whole))
    music.playTone(370, music.beat(BeatFraction.Whole))
    music.playTone(330, music.beat(BeatFraction.Whole))
    music.playTone(294, music.beat(BeatFraction.Whole))
    music.playTone(330, music.beat(BeatFraction.Half))
    music.playTone(330, music.beat(BeatFraction.Half))
    })
    controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.startEffect(effects.bubbles, 2000)
    music.playMelody("G F G A - F E D ", 120)
    })
    music.setTempo(65)
    music.setVolume(60)
    forever(function () {
    if (controller.left.isPressed()) {
        music.jumpUp.playUntilDone()
        }
    })
```
This 2 Minute Arcade will walk you through some of the most often used blocks when adding sound to your game.

## Predict 
- Take a look at the code and make a prediction. What will happen?

## Run 
See if you were correct? 

- Switch to the simulator and press press the **A** and **B** buttons. Press the left button as well. 

Was you're prediction correct?

## Investigate 
Now... let's see what happens if you switch out the ``||Music:playUntilDone||`` with ``||Music:play``.

Check out the hint to see how.

Switch to the simulator and press the left button.

```blocks
    forever(function () {
    if (controller.left.isPressed()) {
        \\@highlight
        music.jumpUp.play()
        }
    })
```
## Ouch! Not Music to My Ears
Using the play block will allow another event to interrupt the sound and restart it instantly.

When creating your game, make sure you select the correct block.

## Modify 
Time to change things around. Play around with the parameters and see what happens.
-[] Change the volume. How high or low can you go?
-[] Change the tempo. How high or low can you go?
-[] Change the notes or add some more in the **button B pressed event**.
-[] Try a different melody or make your own in the **button A pressed event**.
-[] See if you can use the up and down buttons to increase and decrease the tempo.

## Make
Now it's your turn!

Make your own music either when the game starts of when any of the controller buttons are pressed.

## Recap 
Yeah! That sounded great!

Let's recap, in this 2 Minute Arcade, we explored how to add sound effects, melodies, and even make our own tunes. We can modify how quickly (tempo) or loudly (volume) our sounds play.

We also learned about the difference between playing a tone or playing it till it's done.

Nice!

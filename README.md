p5.js SceneManager
==================

Scene management in codeguppy.com
---------------------------------

- [codeguppy.com](https://codeguppy.com) is using a modified version of 'p5.SceneManager' library. This allows users to easily create multi-scene programs / sketches / games in codeguppy.com without having to worry about scene management.

[![JavaScript projects](img/creative_projects.png)](https://codeguppy.com)

Library Description
-------------------

p5.js SceneManager helps you create [p5.js](https://github.com/processing/p5.js) sketches with multiple states / scenes.
Each scene is a like a sketch within the main sketch. You focus on creating
the scene like a regular sketch and SceneManager ensure scene switching
routing the main setup(), draw(), mousePressed(), etc. events to the 
appropriate current scene.

Instead of putting all your code in the main setup() and draw() like this:

```JavaScript
function setup() {

}

function draw() {

}
```

... you put each scene code in the setup() and draw() methods of individual Scene classes:

```JavaScript
// Intro scene constructor function
function Intro()
{
    this.setup = function() {
    }

    this.draw = function() {
    }

    this.keyPressed = function() {
        // switch the scene
        this.sceneManager.showScene( Game );
    }
}

// Main games scene constructor function
function Game()
{
    this.setup = function() {
    }

    this.draw = function() {
    }
}
```

The SceneManager will provide you with methods necesary to switch to the appropriate scene and route the main p5.js events to your defined events.

Source Code
-----------

Source code is located in [lib/scenemanager.js](lib/scenemanager.js)


Demo Code
---------

For demo please check sample.html, sample_instance.html and game.html


Online demo
-----------

If you want to play with scenes in an online playground, just go to [codeguppy.com](https://codeguppy.com) code editor.

To see some standalone demonstrations of SceneManager check out the following demos:

- [sample.html](https://mveteanu.github.io/p5.SceneManager/sample.html)
- [sample_instance.html](https://mveteanu.github.io/p5.SceneManager/sample_instance.html)
- [game.html](https://mveteanu.github.io/p5.SceneManager/game.html)


Future development
------------------

The library can be further extended with features such as:
- routing of more / all events to the appropriate scene class
- running of multiple scenes in parallel (overlapped)
- running of multiple scenes in parallel in individual areas of a bigger canvas

If you are interested in these features, please open an issue here on GitHub.


License
-------

[CC BY 2.0](https://creativecommons.org/licenses/by/2.0/)

VMA

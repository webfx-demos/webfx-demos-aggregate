# webfx-demos-aggregate

All WebFX demos aggregated in a single repository.

Once cloned, you need to check out the branches of the different submodules by executing:

```sh
# Our own WebFX demos use directly the "main" branch
cd webfx-demo-colorfulcircles&& git checkout main && cd ..  
cd webfx-demo-demofx&& git checkout main && cd ..  
cd webfx-demo-enzoclocks&& git checkout main && cd ..  
cd webfx-demo-files&& git checkout main && cd ..  
cd webfx-demo-flexbox&& git checkout main && cd ..  
cd webfx-demo-ledclock&& git checkout main && cd ..  
cd webfx-demo-ledpacking&& git checkout main && cd ..  
cd webfx-demo-mandelbrot&& git checkout main && cd ..  
cd webfx-demo-medusaclock&& git checkout main && cd ..  
cd webfx-demo-moderngauge&& git checkout main && cd ..  
cd webfx-demo-mostlyfluid&& git checkout main && cd ..  
cd webfx-demo-particles&& git checkout main && cd ..  
cd webfx-demo-raytracer&& git checkout main && cd ..  
cd webfx-demo-spacefx&& git checkout main && cd ..  
cd webfx-demo-tallycounter&& git checkout main && cd ..

# Those repositories are actually forks from original games, and the WebFX port is in the "webfx" branch
cd webfx-demo-chess && git checkout webfx && cd ..  
cd webfx-demo-fx2048 && git checkout webfx && cd ..  
cd webfx-demo-fooddice && git checkout webfx && cd ..  
cd webfx-demo-jarkanoid && git checkout webfx && cd ..  
cd webfx-demo-memorygame && git checkout webfx && cd ..  
cd webfx-demo-tetris && git checkout webfx && cd ..  
cd LogicSimulator && git checkout webfx && cd ..  
cd RailTheWay && git checkout webfx && cd ..  
cd Retoohs && git checkout webfx && cd ..  
cd Snake && git checkout webfx && cd ..  

# This repository is separate WebFX port made by the author and its branch is "master"
cd webfx-pacman && git checkout master && cd ..  
```

You can build all demos together for the web by executing:

```sh
webfx build -g
```

(if you haven't yet installed the WebFX CLI, please refer to the [docs](https://docs.webfx.dev/#_installing_the_webfx_cli) to install it, or alternatively just type `mvn package -P gwt-compile` to achieve the same result).

You can locate the different generated web files by executing:
```sh
webfx build -gl
```

To run a demo in the browser, you can execute:
```sh
webfx run -g
```
and follow the given instructions.

For example, to run the Tally Counter demo, you need to execute:
```sh
webfx run -g -M webfx-demo-tallycounter-application-gwt
```

This will open the web file in your browser with the `file://` protocol. However, this protocol doesn't allow to play sounds. So for games with sounds, it's better to open the file with the `http://` protocol. To do that, edit the index.html file in your Java IDE, and ask it to open it in the browser. You may want to bookmark all the web files in your IDE.
# webfx-demos-aggregate

All WebFX demos aggregated in a single repository.

Once cloned, you need to move the following game forks to the webfx branch by typing:
```sh
cd webfx-demo-fx2048 && git checkout webfx && cd ..  
cd webfx-demo-fooddice && git checkout webfx && cd ..  
cd webfx-demo-jarkanoid && git checkout webfx && cd ..  
cd webfx-demo-memorygame && git checkout webfx && cd ..  
cd webfx-demo-tetris && git checkout webfx && cd ..  
cd RailTheWay && git checkout webfx && cd ..  
cd Retoohs && git checkout webfx && cd ..  
cd Snake && git checkout webfx && cd ..  
```

You can build all demos together for the web by typing:

```sh
webfx build -g
```

(if you haven't yet installed the WebFX CLI, please refer to the [docs](https://docs.webfx.dev/#_installing_the_webfx_cli) to install it, or alternatively just type `mvn package -P gwt-compile` to achieve the same result).

You can locate the different generated web files by typing:
```sh
webfx build -gl
```

To run a demo in the browser, you can type:
```sh
webfx run -g
```
and follow the given instructions.

For example, to run the Tally Counter demo, you need to type:
```sh
webfx run -g -M webfx-demo-tallycounter-application-gwt
```

This will open the web file in your browser with the `file://` protocol. However, this protocol doesn't allow to play sounds. So for games with sounds, it's better to open the file with the `http://` protocol. To do that, edit the index.html file in your Java IDE, and ask it to open it in the browser. You may want to bookmark all the web files in your IDE.
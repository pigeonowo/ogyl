# OGYL - Onyx Graphics (y?) Library
Build UIs and Graphics on the Web and Desktop(linux/mac) with an abstraction over opengl/webgl.

The rest of the readme is just all my thoughts written down before I went to sleep so it might be messy.
## OpenGL / WebGL Abstraction
The main thing about this library is to give an abstraction layer above OpenGL and WebGL so that you can use 1 API to do graphics on both web and desktop.
There will be structs that represent a Shader, or a Mesh like a Triangle so that you don't have "to deal" with vertex array objects, etc. yourself.
It could look like this:
```c
shader->use_shader()
shader->set_uniform("value", 1)
triangle->draw()
```

## Graphics
If you have Raylib and OpenGL as a Graphics library - OGYL will be right between those 2 in abstraction.
You should still have all the control but have logic capsulated with the relevant data.

## UI
Additionaly there should be a UI library which gives you "elements". Think of them like in HTML or Flutter Widgets.
Here an example out of my head:
```c
some_element()
|> background(.black)
|> margin(2)
|> children(.[
    element_two(),
    element_three(),
])
```

## Onyx - and why?
You cant statically link raylib with wasm so hard to port to the web. I also wanna learn more about opengl, so why not :)
I wanna create this library also as an entry "big project" for the Onyx Community which I love so much.
Onyx has some real potential and I wanna see how I can use it in the Graphics space.
Onyx can run WASM on the host and also in the browser (duh) and has support for linking object files which enables opengl/desktop.

## Contributing
I hope you can see the vision that I am seeing. Contributions are welcome!
I am bored so I will review pull requests pretty fast :)

MUJIN Frontend Programming Challenge
=============

Howdy there candidate! This programming challenge is to help us gauge your frontend software engineering skills during our hiring process. You'll be developing a simple [Backbone](http://backbonejs.org/) app from scratch.

For this challenge, you'll be using Backbone in conjunction with [threejs](http://threejs.org/) to make a simple 3d object viewer and editor. Users should be able to create / edit / update / delete 3d primitives (like boxes, spheres, etc.) in their browser. It'll be similar in function to the [threejs editor](http://threejs.org/editor/) but far less complicated and built with Backbone instead of vanilla javascript.

###Guidelines:

- Fork this repository.
- Complete the challenge, making commits along the way. The components and other things we're looking for are outlined below. You can use any additional dependencies / development tools you want (within reason), but at minimum you have to use Backbone and threejs.
- Deploy your completed application somewhere public on the internet and send us the link when you're done. We recommend [github pages](https://pages.github.com/).

###Major components of the application:

- Renderer
  - Should be a view that wraps the threejs renderer
  - Able to navigate around the 3d environment with a mouse
  - Click on drawables in the renderer and trigger a custom event that the rest of the application responds to
- Drawable
  - Should be a model that represents objects in the scene
  - All changes to model attributes should be immediately reflected in the renderer when they happen
  - Able to change position and orientation of drawable by modifying model attributes. You can choose what attributes you want to use to represent this (could use a 4x4 `matrix` attribute, or separate `translation` / `quaternion` attributes for example).
  - Able to change the color of the drawable by modifying the `color` attribute
  - Able to change various model attributes to change the properties of the dimensions of the geometry depending on the geometry type. So for example, if the drawable is a `box`, able to set the `length`, `width`, and `height`.
    - Geometry types and dimension attributes:
      - `box` (`length`, `width`, `height`)
      - `sphere` (`radius`)
      - `cylinder` (`radius`, `height`)
      - `text` (`message`, `size`, `height`)
      - `torus` (`radius`, `tubeDiameter`)
- Drawable create / delete controls
  - One or more views that allows the creation and deletion of drawables
- Drawable edit controls
  - One or more views that allows the modification of drawable attributes
  - Should be able to edit attributes common to all drawables, as well as attributes that depend on the geometry type of the drawable
  - If a drawable is clicked in the renderer, focus of the controls should change to that drawable

###Other things we're looking for:

Besides fulfilling the basic goal of implementing the components above and creating a working application, there are a few other things we're looking for:
- How clean is your code? Are things organized?
- Is your app filled with a ton of Backbone boilerplate that could have been abstracted elsewhere?
- How DRY are the components you built? Could I easily use them in another application if I wanted to treat them like a library?
- How did you use events to properly decouple things?
- How did you do dependency management? Even though you can get everything done with just Backbone / threejs, imagine if this app were to grow to use 100 dependencies and I wanted to start changing the versions of everything. Would that be easy or hard to do?
- How did you deploy the app? Again we strongly recommend [github pages](https://pages.github.com/) for this project.
- Are your commits easy to read / understand? Are your commit messages short and to the point?
- Did you use any sort of module loader? Did you protect things from polluting the global namespace?
- Are there any performance bottlenecks?

Best of luck and feel free to email me or Rosen with any questions!
